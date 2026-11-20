# [TUBER 프로젝트(Claude)] ep2 v3 전체 재생성과 재편집 (claude → tuber)

- 상태: open
- 요청: 팩 v3로 E01~E12(18회)를 생성하고, 브라우저 스레드가 만든 E13~E24(17회)와 합쳐 2화 v3를 편집해 주세요.
- 입력: `episodes/ep2/ep2-pack-v3-natural.md`, `episodes/ep2/ep2-edl.csv`, 음원 MP3(기존 팩 1절 URL), 아래 「브라우저 스레드 클립」 표
- 완료 기준: `ep2-yejin-1080p-v3.mp4` + 「결과」 기록. **max 승인 완료(2026-11-20 11:50 KST, "고칠 게 있으면 고쳐").** 크레딧 0만 허용. 유료가 필요하면 멈추고 보고.

## 생성 분담 (무료 Seedance는 계정당 한 번에 1개)

| 담당 | 샷 | 생성 수 |
|---|---|---|
| Tuber | E01~E12 (A+B: E02, E04, E07, E08, E09, E11) | 18 |
| 브라우저 스레드(Claude, max의 Chrome) | E13~E24 (A+B: E17, E18, E21, E22, E24) | 17 |

- **번갈아 쓰기 (2026-11-20 13:10 KST 추가):** 내 작업이 끝나면 **60초 기다린 뒤** History에 새 "Generating" 항목이 없을 때만 다음 작업을 제출합니다. 그 사이 브라우저 스레드가 한 개를 제출할 수 있게 하기 위함입니다(브라우저 스레드도 같은 규칙).
- **제출 규칙:** 사이트에 진행 중인 작업이 없을 때만 제출합니다. 진행 중이면 기다렸다 제출. Rerun 버튼 금지.
- E08 (Claude 판단, 13:45 KST): 박수 간격이 곡 박자에 맞는 **E08_N2(약 0.67초 간격 → 1.25배에서 0.53초)를 E08_A3로**, E08_N3(약 1초 간격)는 E08_B3 후보로 씁니다. 편집에서 N3 구간은 박수 소리와 닿는 프레임이 맞는 부분만 고르고, 안 맞으면 E08 B를 한 번 더 생성합니다.
- 실패(귀, 다른 캐릭터, 몸 녹음, 박수 0회)는 같은 카드로 다시 생성(무료). 같은 샷 3번 실패하면 멈추고 보고.

## 편집 규칙 (v1 문제 반영)

1. 원본 프레임 그대로 디코딩(`-fps_mode passthrough`), 프레임 반복 0개 확인.
2. 속도: 일반 샷 1.15배, 박수 샷(E08, E09, E12, E13, E18, E22) 1.25배. 프레임 건너뛰기, 24fps.
3. 컷 위치는 `ep2-edl.csv`의 tl_start/tl_end 그대로. src_range는 속도 적용 후 맞게 다시 고릅니다(같은 클립의 A/B 구간이 겹치지 않게, 박수 샷은 A/B 테이크를 따로 사용).
4. E01은 이제 10초 원본이므로 되감기 없이 씁니다.
5. 박수: 박수 소리(음원 1.5~5kHz 순간 피크) 프레임과 앞발(날개)이 닿는 프레임을 ±2프레임 안으로. 2절은 철자당 박수 1번만 보이게 구간 선택, 6절은 계속 치는 구간.
6. 글자: 지금 타이밍 유지(보컬이 다운비트보다 0.2~0.3초 먼저 들어옴). 첫 줄(14.8~17.2초)만 귀로 확인해 어긋난 글자만 옮깁니다. 별 아이콘은 박수 소리 프레임에.
7. 음량 −14 LUFS 근처, 마지막 정지·최종 화면은 v1과 같게.
8. 검수: 완성본을 0.5초 간격 전체 프레임으로 귀·Pip 끼어듦·글자 확인.

## 브라우저 스레드 클립

| 샷 | 파일명 | URL | 검수 메모 |
|---|---|---|---|
| E24 A | ep2_E24_A3.mp4 | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261120_025921_9b8703ed-f0af-42c7-aa03-3de71a0ed28d.mp4 | 통과. Pip 첨벙 1.5~2.5초 |
| E24 B | ep2_E24_B3.mp4 | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261120_030513_fb044525-f685-490b-a437-65ce4eed3679.mp4 | 통과. A보다 차분 |
| E22 A | ep2_E22_A3.mp4 | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261120_030941_2a5147f6-c585-449a-9955-cbd8d8f83141.mp4 | 통과. 박수 약 7회(닿는 시점 약 0.75/1.25/1.75/2.25/3.0/4.0/4.5초) |
| E22 B | ep2_E22_B3.mp4 | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261120_032806_31b58a18-8f94-4e29-9d9d-dfef4e8e0e86.mp4 | 통과(2차). 박수 6~7회, Pip과 맞음. 1차 실패본은 쓰지 않음 |
| E23 A | ep2_E23_A3.mp4 | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261120_032143_ab69c14f-ef3c-4391-80b6-15990d4c00a4.mp4 | 통과. 10초, 약 4.5초부터 카메라 빠짐 |
| E21 A | ep2_E21_A3.mp4 | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261120_033433_77ee808a-5ada-41b7-90be-f41a2db59952.mp4 | 통과(메모). 약 2.0초 방울 터짐, 코 닿는 순간은 흐림 |
| E21 B | ep2_E21_B3.mp4 | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261120_033934_0d2fa957-dcf2-4321-ae75-3189f3f545bf.mp4 | 통과. 2.5~3.0초 방울 터짐(더 선명), 이후 앞발 통통 |
| E20 A | ep2_E20_A3.mp4 | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261120_035119_39da80fa-baf4-43d1-980c-325a9253a205.mp4 | 통과. 0~2초 작은 점프, 이후 끄덕 2회 |
| E19 A | ep2_E19_A3.mp4 | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261120_043316_859a6452-bbe1-4083-92d4-6088b588a437.mp4 | 통과(2차). 1차는 귀 문제로 사용 금지 |
| E18 A | ep2_E18_A3.mp4 | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261120_040018_b6986e3f-2392-49df-9526-d8a15389e3a0.mp4 | 통과. 박수 5회, 약 1초 간격 |
| E18 B | ep2_E18_B3.mp4 | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261120_041601_f9ca7208-1822-4fc0-93b5-0e45e194a194.mp4 | 통과. 박수 7~8회, A보다 빠름 |

(계속 추가됩니다: E17 A/B, E16, E15, E14, E13)

## 결과

(Tuber 작성: 생성 회수와 실패 기록, 출력 파일 위치, 사양, 프레임 반복 0 확인, 박수 정렬 결과, 특이 사항)

작성 규칙: 로컬 파일 경로, 컴퓨터 이름, OS 사용자 이름, 키·토큰·개인 연락처 금지(공개 저장소).
