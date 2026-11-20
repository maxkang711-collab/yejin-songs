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

### 분담 조정 (2026-11-20 15:45 KST)

무료 대기열이 느려져 나머지를 다시 나눕니다.
- **Tuber 남은 것:** E03(진행 중), E04 A/B, E05, E06, E07 A/B, E08 B (8회)
- **브라우저 스레드로 이동:** E09 A/B, E10, E11 A/B, E12 (E13~E16 다음에 진행)
- Tuber가 이미 만든 것(History 기준, 아직 검수 기록 없음): E08 N3(02:53 UTC), E01(03:44), E02 두 테이크(04:04, 04:09). 「결과」에 검수 결과와 URL을 적어 주세요.

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
| E17 A | ep2_E17_A3.mp4 | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261120_044002_4e8e0c47-0a91-427b-9969-b328411b823c.mp4 | 통과. 고개 기울임, 끄덕임, 큰 웃음 |
| E17 B | ep2_E17_B3.mp4 | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261120_044459_ea9a3027-b101-43e7-a889-fd9f467ed1b7.mp4 | 통과 |
| E16 A | ep2_E16_A3.mp4 | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261120_073940_f8852048-d2a7-4395-9f78-0b4b2934f2ea.mp4 | 통과(2차). 큰 첨벙 대신 물결 |
| E15 A | ep2_E15_A3.mp4 | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261120_081019_0993dfc9-4e8a-4e1c-b5cf-c8b250559a9a.mp4 | 통과(2차). 연못 쪽으로 달리지만 좌→우가 아니라 화면 안쪽 방향 |
| E14 A | ep2_E14_A3.mp4 | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261120_084757_7d3d16e7-4f50-4633-be45-dbc0932265a8.mp4 | 통과. 무대에서 위아래로 통통, 끝에 앞발 들기 |
| E13 A | ep2_E13_A3.mp4 | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261120_085804_a48a766d-a3c7-44d9-9115-34fa7b6e3034.mp4 | 통과. 박수 4~5회, 분홍 발바닥 보임 |
| E12 A | ep2_E12_A3.mp4 | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261120_091136_09927079-dfd4-4a97-bcea-297dea9f2a15.mp4 | 통과. 서로 앞발-날개 맞부딪치기 4회, 1.25초 주기(1.25배면 1.0초=2박). 3절 슬롯(박수 2번)은 첫 박수 소리에 닿는 프레임을 맞추고, 둘째 박수는 별 아이콘 팝으로 강조 |
| E11 A | ep2_E11_A3.mp4 | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261120_092417_d7ccf3ae-5701-4f06-a0b0-d254c623938d.mp4 | 통과. 제자리 탭 3회 후 올려다봄 |
| E11 B | ep2_E11_B3.mp4 | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261120_093645_4947bbb2-3531-4392-9094-493279abf204.mp4 | 통과(더 좋음). 건반 따라 탭 약 5회, 꼬리 흔들기 |

(계속 추가됩니다: E10, E09 A/B)

## 결과

(Tuber 작성, 2026-11-20 18:10 KST 갱신. Tuber 담당 생성 끝. 편집은 아직 안 함.)

모두 무료 Unlimited, 720p, 16:9, Seedance 2.5, 24fps, Rerun 안 씀, 크레딧 0. 검수: 0.5초 간격 전체 프레임(귀, 다른 캐릭터, 글자, 사람처럼 서기, 몸 녹음).

| 샷 | 파일명 | 제출(KST) | URL | 검수 메모 |
|---|---|---|---|---|
| E01 A | ep2_E01_A3.mp4 | 12:44 | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261120_034458_f490b805-504f-465a-9edb-f46ec4c28245.mp4 | 통과. 10.04초(241프레임). 집 문에서 고개 내밀고 네 발로 걸어 나와 앉아 헥헥, 끝에 밀기. 귀 없음, 혼자 |
| E02 A | ep2_E02_A3.mp4 | 13:04 | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261120_040421_eddbfb6e-42c9-43e2-ac22-3f1ce8b34487.mp4 | 통과. 121프레임. 고개 갸웃, 입 크게 벌려 짖기, 헥헥. 귀 없음 |
| E02 B | ep2_E02_B3.mp4 | 13:09 | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261120_040944_9aa776af-2d93-4919-be67-4f23b77f5914.mp4 | 통과. 121프레임. A보다 움직임 큼(몸·꼬리 흔들기), 짖기. 귀 없음 |
| E08 A | ep2_E08_A3.mp4 (= E08_N2) | 10:42 | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261120_014247_19d97936-ac71-479a-b190-f5a05cbc1691.mp4 | 13:45 Claude 판단대로 A로 사용. 박수 약 6~7회(약 0.67초 간격). 팔 약간 늘어남, 모을 때 발바닥 안 보임 |
| E08 B 후보 | ep2_E08_B3.mp4 (= E08_N3) | 11:53 | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261120_025318_07d0d180-a686-4def-b06d-b9b3ccfd1bdf.mp4 | 통과(실패 기준 없음). 박수 약 5회(6fps 기준, 약 1초 간격), 팔 늘어남 줄어듦, 모을 때 발바닥 안 보임. 편집에서 박수 소리와 맞는 구간만 사용 |
| E03 A | ep2_E03_A3.mp4 | 14:54 | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261120_055403_121ef6df-9d94-4182-be62-d95d57d34fd6.mp4 | 통과. 121프레임. 앞발로 제자리 통통, 몸 흔들기, 입 벌려 웃기. 귀 없음, 혼자 |
| E04 A | ep2_E04_A3.mp4 | 16:44 | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261120_074419_cb6036a2-a794-4767-b609-97c92291d1a0.mp4 | 통과. 121프레임. 집 앞에 앉아 끄덕, 별 반짝. 귀 없음, 혼자. 움직임은 작음 |
| E04 B | ep2_E04_B3.mp4 | 16:48 | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261120_074844_21eea2de-2d28-44c2-8518-4895c135be98.mp4 | 통과. 121프레임. A와 비슷, 별 반짝. 귀 없음, 혼자 |
| E05 A | ep2_E05_A3.mp4 | 17:04 | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261120_080442_e03fefe7-2834-4054-81eb-c9abd7ff212b.mp4 | 통과. 121프레임. 왼쪽에서 고개 돌려 카메라 보고 갸웃, 웃음. 귀 없음, 혼자 |
| E06 A | ep2_E06_A3.mp4 (2차) | 18:03 | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261120_090314_b7098276-5c0a-43a8-9d54-d38b70b9414a.mp4 | 통과(2차). 121프레임. Pip 돌다리로 다가오고 예진 일어나 꼬리 흔들며 Pip 쪽으로. 귀 없음. 1차(17:20, da17cf29)는 약 2초부터 처진 귀가 보여 사용 금지 |
| E07 A | ep2_E07_A3.mp4 | 17:27 | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261120_082709_4d16e9c8-4d02-4ee8-be20-785798ff9889.mp4 | 통과. 121프레임. 예진·Pip 서로 보고 카메라 보며 끄덕. 귀 없음 |
| E07 B | ep2_E07_B3.mp4 | 17:36 | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261120_083623_984d0b0f-6a32-4b39-b20e-e6d691935d18.mp4 | 통과. 121프레임. A와 다른 테이크(파일 다름). 귀 없음 |

진행 상황과 특이 사항:
- Tuber 담당(E01~E08) 생성 완료. E08 B는 편집에서 N3가 박수 소리와 안 맞을 때만 한 번 더 생성합니다.
- E03: 14:53 1차는 몇 초 만에 실패(크레딧 환불). 14:54 2차가 약 1시간 걸려 완료.
- E06: 1차 귀 문제로 같은 카드로 1회 재생성, 2차 통과.
- E09~E12는 15:45 분담 조정대로 생성하지 않았습니다.
- 편집은 브라우저 스레드의 E09~E13이 다 나오면 시작합니다.

작성 규칙: 로컬 파일 경로, 컴퓨터 이름, OS 사용자 이름, 키·토큰·개인 연락처 금지(공개 저장소).
