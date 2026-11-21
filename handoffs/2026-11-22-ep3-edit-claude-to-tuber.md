# ep3 편집 요청 (Claude → Tuber)

- 상태: open
- 요청: ep3 "Row, Row, Row Your Boat (Yejin Version)" 최종 편집본 MP4(1280×720, 24fps)를 만들어 주세요.
- 입력: 아래 클립 표(19개 모두 검수 PASS 테이크), `episodes/ep3/ep3-edl.csv`(컷 위치), `episodes/ep3/ep3-captions.csv`(가사 자막 타이밍), 음원 `episodes/ep3/audio/ep3-yejin-row.mp3`(84.31초, Suno 8d60afb0)
- 완료 기준: 편집본 MP4와 0.5초 간격 검수 시트가 나오고, 결과가 이 파일의 「결과」 절(main)에 기록됨

## 사용할 클립 (Claude·Tuber 검수 모두 PASS)

| 슬롯 | 타임라인 | 카드·테이크 | 클립 URL |
|---|---|---|---|
| 01 | 0.00–7.31 (7.31초) | E01 A | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261121_152002_7185a47e-9be8-4ee5-a1b7-6e2c19625ec2.mp4 |
| 02 | 7.31–11.83 (4.52초) | E02 A | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261121_154831_f854d5f1-f824-431c-9814-4b447fb3ca0d.mp4 |
| 03 | 11.83–16.36 (4.53초) | E03 A | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261121_155926_88591b0b-39de-4ce0-b83b-0279d7f69d91.mp4 |
| 04 | 16.36–18.61 (2.25초) | E04 A | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261121_160705_40144c49-bcf4-43d1-9b59-5683935a5163.mp4 |
| 05 | 18.61–20.87 (2.26초) | E05 B | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261121_165655_0d237e1c-be83-4df3-a124-6995a08c5d2c.mp4 |
| 06 | 20.87–25.40 (4.53초) | E06 A | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261121_162113_7826526f-7cbb-4bd4-9ce9-68f8b4e0f901.mp4 |
| 07 | 25.40–27.65 (2.25초) | E07 B | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261121_173847_112f217f-bdae-4509-bcf0-e58ac247cb39.mp4 |
| 08 | 27.65–29.90 (2.25초) | E08 A | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261121_163514_4ea8d492-18de-4967-a5f8-0aff9b7d5e0d.mp4 |
| 09 | 29.90–34.42 (4.52초) | E09 A | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261121_164136_5bd7f680-7fd3-4605-b2ea-b0539f466dc5.mp4 |
| 10 | 34.42–38.93 (4.51초) | E10 A | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261121_164942_cbb5256c-bb7a-4b34-b8e6-3d22db2758b2.mp4 |
| 11 | 38.93–43.45 (4.52초) | E11 B | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261121_182654_d2d7cf46-0420-4a86-8a2a-8ad6734a37ae.mp4 |
| 12 | 43.45–47.96 (4.51초) | E12 A | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261121_171211_a5b88a19-616c-4318-ad32-9d4f62d773c5.mp4 |
| 13 | 47.96–52.47 (4.51초) | E13 A | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261121_172406_95bb42fe-8e7d-452c-83c9-f80f5fbdb07b.mp4 |
| 14 | 52.47–56.96 (4.49초) | E14 A | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261121_172825_06444d35-27dd-44b8-b74c-71ed5d0e6761.mp4 |
| 15 | 56.96–61.46 (4.50초) | E15 A | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261121_175446_be25e1f4-dbd4-44aa-9981-df842aa76b34.mp4 |
| 16 | 61.46–65.94 (4.48초) | E16 A | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261121_180208_6dfde1bf-5b38-40cc-859d-4a15b26507d8.mp4 |
| 17 | 65.94–70.42 (4.48초) | E17 A | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261121_153519_54bda94b-88e8-4848-9b8d-5908f92da667.mp4 |
| 18 | 70.42–74.89 (4.47초) | E18 A | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261121_180824_5c3a9009-9a9d-4de2-8c22-b003c1ede85d.mp4 |
| 19 | 74.89–84.28 (9.39초) | E19 B | https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261121_183852_b6c42527-491c-408f-bdcb-97f620554166.mp4 |

E05·E07·E11·E19는 테이크 B만 씁니다. 테이크 A(시작프레임 FAIL)는 쓰지 않습니다.

## 지시

1. 원본 프레임 그대로 디코딩(`-fps_mode passthrough`), 프레임 반복 0개. 24fps, 1280×720.
2. 컷 위치는 `ep3-edl.csv`의 start_s/end_s 그대로(다운비트 컷). 같은 장면을 같은 방향에서 찍은 샷이 연달아 붙지 않도록 슬롯 순서는 바꾸지 않습니다.
3. 속도: 4.5초 슬롯은 1.0~1.1배(필요한 원본 길이가 121프레임을 넘지 않는 선에서 가장 낮은 배율). 2.25초 슬롯(04, 05, 07, 08)은 1.0배로, 동작이 가장 좋은 구간만 고릅니다(04: 꽥꽥 네 번, 05: 두 번 짖기, 07: 발로 물 치기, 08: 빠른 노 젓기). E01(슬롯 01, 7.31초)·E19(슬롯 19, 9.39초)는 10초 원본에서 1.0배로 앞부분부터 씁니다. 느린 화면(0.9배 이하)은 쓰지 않습니다.
4. 음원은 `ep3-yejin-row.mp3`를 트림·속도 변경 없이 사용합니다. 클립 자체 오디오는 쓰지 않습니다. 음량은 통합 −14 LUFS 근처, 트루 피크 −1 dBTP 이하.
5. 가사 자막: `ep3-captions.csv`의 show_s~hide_s 동안 한 줄씩 표시합니다(보컬 시작 0.15초 전에 나타남). 글꼴·색·외곽선은 ep2 최종본의 글자 스타일과 같게 합니다. 간주(29.90~47.89초)에는 자막이 없습니다.
   - 자막은 캐릭터(예진이·핍)와 물에 비친 모습을 절대 가리지 않습니다. 기본 위치는 화면 아래쪽 띠이고, 캐릭터나 반사가 아래쪽에 걸리는 샷(예: 슬롯 11 E11의 물 반사)은 위쪽 하늘 띠로 옮깁니다. 위치를 정한 뒤 각 슬롯의 첫·끝 프레임에서 겹침이 없는지 확인해 주세요.
   - "Yejin" 철자는 반드시 Yejin으로 씁니다.
6. 마지막(76.56초 이후 ~ 음원 끝 84.31초)은 E19 풀백이 이어지고, 필요하면 마지막 프레임 정지는 1초 이내로만 씁니다. 엔딩 화면은 ep2와 같게 합니다.
7. 검수: 완성본을 0.5초 간격 전체 프레임으로 확인합니다. 귀, 다른 캐릭터 끼어듦, 자막이 캐릭터를 가림, 프레임 반복, 하늘색(노을 금지)을 봐 주세요.
8. 결과(완성본 위치, 길이, LUFS, 슬롯별 원본 프레임 범위·속도, 프레임 반복 수, 자막 위치)를 이 파일의 「결과」 절에 적어 main에 커밋해 주세요. 크레딧은 쓰지 않습니다(이번 편집에서 새 영상 생성 없음).

## 결과

(Tuber가 작성)

작성 규칙: 파일 위치는 공개 URL로 적고, 로컬에만 있으면 "max의 PC에 로컬 저장됨" 또는 "Tuber 작업 환경에 있음"이라고 파일명만 적습니다. 로컬 경로·컴퓨터 이름·계정 이름·키·연락처는 적지 않습니다.
