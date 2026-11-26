# [TUBER 프로젝트(Claude)] ep4 편집 요청 (claude → tuber)

- 상태: open (2026-11-26 KST). max가 "4화 빨리 완성"을 요청했습니다. 가장 먼저 처리해 주세요.
- 요청: ep4 «Yejin Had a Little Lamb» 최종 편집본 MP4를 만들어 주세요. 규격은 ep3 최종본과 같습니다(1920×1080, 24fps, 원본 720p를 lanczos로만 확대).
- 입력:
  - 아래 클립 표(25슬롯, 모두 검수를 통과한 테이크)
  - `episodes/ep4/ep4-edl.csv`(컷 위치)
  - `episodes/ep4/ep4-captions.csv`(가사 자막 타이밍)
  - 음원 `episodes/ep4/audio/ep4-yejin-lamb.mp3`(94.75초, Suno ca0003f1)
- 완료 기준: 편집본 MP4와 0.5초 간격 검수 시트가 나오고, 결과가 **이 파일의 「결과」 절에 기록되어 main에 커밋됨**. 저장소 기록이 꼭 필요합니다.

## 사용할 클립

| 슬롯 | 타임라인 | 카드·테이크 | 클립 URL |
|---|---|---|---|
| 01 | 0.00–7.61 (7.61초) | E01 A | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261125_032038_42625e07-d6ad-494b-8861-485f52fd96ba.mp4 |
| 02 | 7.61–10.92 (3.32초) | E02 A | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261125_033644_e7a5fdf6-2666-4b9e-9369-b7e546993ce0.mp4 |
| 03 | 10.92–14.24 (3.32초) | E03 A | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261125_034812_1fd65319-7a1e-4187-8c66-edc22609ba55.mp4 |
| 04 | 14.24–17.57 (3.32초) | E04 A | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261125_040203_f734337e-eac4-423c-8491-e63f99d56bd1.mp4 |
| 05 | 17.57–20.89 (3.32초) | E05 A | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261125_041644_dc31f216-605d-4264-97c9-f3dddb263411.mp4 |
| 06 | 20.89–24.20 (3.32초) | E06 B | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261125_170357_c512d35b-d218-4413-9caa-f249c032a425.mp4 |
| 07 | 24.20–27.52 (3.32초) | E07 A | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261125_085423_decad9e0-1cfb-4292-bdf9-41805e3df3ec.mp4 |
| 08 | 27.52–30.84 (3.32초) | E08 B (원본 0–3.5초 안에서만) | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261125_162944_01f7bd7d-bc0d-489e-8ce5-8114a05a14f2.mp4 |
| 09 | 30.84–34.15 (3.31초) | E09 B | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261125_172201_ec024a4c-6123-4508-83fe-97f331cc8fec.mp4 |
| 10 | 34.15–37.46 (3.31초) | E10 A | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261125_100858_42fb4b7d-915d-4cc2-920c-4aa63885d038.mp4 |
| 11 | 37.46–40.78 (3.32초) | E11 A | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261125_102506_e6b1e375-0136-45f9-924c-a708fe2650b6.mp4 |
| 12 | 40.78–44.09 (3.32초) | E12 A | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261125_104055_1098bd2b-c7eb-423f-94a1-3ace9cab0e11.mp4 |
| 13 | 44.09–47.41 (3.31초) | E13 A | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261125_105651_2ca44383-b59c-4c1d-b4d0-f8a6ff312d2b.mp4 |
| 14 | 47.41–54.05 (6.64초) | E14 A | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261125_112414_ce39d59d-e7c5-485c-93c4-5ad83bdf5dbc.mp4 |
| 15 | 54.05–57.37 (3.32초) | E15 A | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261125_114120_e9e1c05f-15f2-4b8b-bf85-5fbc1ed2e6ef.mp4 |
| 16 | 57.37–60.69 (3.32초) | E16 B | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261125_164624_4dfd405c-e76e-4e0a-95d2-1b295a275716.mp4 |
| 17 | 60.69–64.00 (3.32초) | E17 A | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261125_124720_540855d4-74a5-4b54-858a-c3a8ad45ecf9.mp4 |
| 18 | 64.00–67.32 (3.32초) | E18 A | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261125_130424_3a333ae1-f318-4132-8b46-fb1ca8ccd35e.mp4 |
| 19 | 67.32–70.64 (3.32초) | E19 A | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261125_140021_c9b605a8-e655-45ba-8bdd-265782fc51d2.mp4 |
| 20 | 70.64–73.95 (3.32초) | E20 A | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261125_142100_549227cf-5812-48f6-a6d2-4ab89c3cbada.mp4 |
| 21 | 73.95–77.27 (3.32초) | E21 A | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261125_143916_26fcb4f6-8de4-4625-981d-e5d932dd08b6.mp4 |
| 22 | 77.27–80.59 (3.32초) | E22 A | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261125_145556_a2b352a4-3536-495a-ab5e-d79e2fa78e87.mp4 |
| 23 | 80.59–83.90 (3.31초) | E23 A | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261125_151323_0288a916-7a17-4fd6-ac05-6d0579b2e5a0.mp4 |
| 24 | 83.90–87.22 (3.31초) | E24 A | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261125_152846_47904928-a285-42fa-b899-f95f1c0a3fe7.mp4 |
| 25 | 87.22–94.72 (7.50초) | E25 A | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261125_161213_c0fdbb94-b1f3-4908-a7e4-d20dd300e30d.mp4 |

E06·E08·E09·E16은 테이크 B(재생성본)만 씁니다. 원본 테이크는 쓰지 않습니다(근거: `handoffs/2026-11-22-ep4-gen-result-tuber.md`). E17은 Tuber 테이크(540855d4)입니다.

## 지시

1. **디코딩과 규격**
   - 원본 프레임을 그대로 디코딩합니다(`-fps_mode passthrough`). 프레임 반복은 0개여야 합니다.
   - 24fps로 만들고, 1080p는 lanczos로만 확대합니다.
2. **컷 위치와 순서:** `ep4-edl.csv`의 start_s/end_s를 그대로 씁니다. 가사 한 줄은 2마디, 3.32초입니다. 슬롯 순서는 바꾸지 않습니다.
3. **속도:** 전 슬롯 1.0배입니다. 0.9배 이하의 느린 화면은 쓰지 않습니다.
   - 5초 원본은 3.32초 슬롯에 원본 앞부분부터 씁니다.
   - 10초 원본은 E01(7.61초), E14(6.64초), E25(7.50초)이며, 역시 앞부분부터 씁니다.
   - **E08 B는 약 4초에 자세가 갑자기 바뀌므로 반드시 원본 0–3.5초 안에서만 씁니다.**
4. **음원**
   - `ep4-yejin-lamb.mp3`는 트림하거나 속도를 바꾸지 않고 씁니다. 클립 자체 오디오는 쓰지 않습니다.
   - 음량은 통합 −14 LUFS 근처, 트루 피크 −1 dBTP 이하로 맞춥니다.
5. **가사 자막**
   - `ep4-captions.csv`의 show_s~hide_s 동안 한 줄씩 표시합니다.
   - 스타일은 ep3 최종본과 같게 합니다(Baloo 2 ExtraBold, 흰 외곽선·허니 그림자, 단어별 색, 110% 팝).
   - **최소 90pt**입니다. ep3에서는 자막이 작다는 지적이 있었습니다.
   - 예진이, 양, Pip을 절대 가리지 않습니다. 기본은 아래쪽 풀밭 띠입니다. 캐릭터가 아래쪽에 걸리는 샷은 위쪽 하늘 띠로 옮깁니다.
   - "Yejin" 철자를 유지합니다.
   - 간주(Break, 슬롯 14–16)에는 자막이 없습니다.
6. **엔딩:** E25의 풀백이 음원 끝까지 이어지게 합니다. 마지막 프레임 정지가 필요하면 1초 이내로만 씁니다. 번인 엔딩 화면은 넣지 않습니다(ep3과 같음).
7. **검수:** 완성본을 0.5초 간격 프레임으로 확인합니다. 다음 항목을 봐 주세요.
   - 귀
   - 다른 캐릭터가 끼어듦
   - 자막이 캐릭터를 가림
   - 프레임 반복
   - 노을 하늘(금지)
   - E08 구간의 갑작스러운 자세 변화
8. **결과 기록:** 다음 항목을 이 파일의 「결과」 절에 적어 main에 커밋해 주세요.
   - 완성본 위치(공개 URL, 없으면 파일명만)
   - 길이, LUFS
   - 슬롯별 원본 프레임 범위와 속도
   - 프레임 반복 수
   - 자막 위치

   크레딧은 쓰지 않습니다(새 영상 생성 없음). 업로드(YouTube 등)는 하지 않습니다.

## 결과

(Tuber가 작성)

작성 규칙: 파일 위치는 공개 URL로 적고, 로컬에만 있으면 "max의 PC에 로컬 저장됨" 또는 "Tuber 작업 환경에 있음"이라고 파일명만 적습니다. 로컬 경로·컴퓨터 이름·계정 이름·키·연락처는 적지 않습니다.
