# 1화 v3 재생성 팩: «Clap with Yejin» (TUBER 프로젝트(Claude))

작성: 2026-11-25 KST. 음원은 기존 그대로(Suno 89609f3a, ep1-clap-v2, 57.08초, 98.5 BPM, 한 줄 = 1마디 약 2.44초). 기존 v1/v2 편집본에 대한 max 피드백(2026-11-25): 움직임이 둔하고 느림, 발바닥 패드 개수가 샷마다 다름(3개/4개), 장면 전환이 매끄럽지 않음.

## 왜 다시 만드는가 (진단)

- 1화는 «실시간 속도·자연스러운 움직임» 규칙(2026-11-20)이 생기기 **전** 프롬프트로 만든 유일한 회차입니다. 동작 하나가 2.5초에 걸쳐 작고 느리게 나오고, 밀기·빼기 카메라가 느립니다.
- 발바닥: 참조 이미지(7e21b96a)는 앞발을 내리고 있어 패드가 보이지 않으므로 모델이 샷마다 패드를 새로 지어냈습니다. 확인(max 스크린숏): 0:28(S11 클립)은 발가락 패드 **3개**+큰 패드, 0:30(S12 클립)과 0:40(S15 클립)은 **4개**+큰 패드.
- 전환: 컷 16개 중 PLAYROOM 샷끼리의 컷마다 방 배치(러그·쿠션·선반)가 바뀌어 다른 방처럼 보이고(PLAYROOM이 8가지 배치), 재사용 슬롯은 같은 방향·같은 장면 컷이며, 끝부분은 역재생입니다.

## 생성 결과 (2026-11-25, Claude)

- 11개 클립 모두 생성 완료, 전부 0크레딧(웹 Unlimited). 클립 URL과 편집용 사용 구간은 `ep1-v3-clips.json`.
- 검수: 모든 클립에서 보이는 발바닥은 발가락 패드 4개 + 하트 패드 1개, 귀 없음, 세트 유지, 실시간 속도 확인.
- 아래 카드와 달라진 점:
  - F02, F03, F06, F07, F09, F10 프롬프트에 «카메라 고정, 줌아웃 금지» 문장을 추가해 생성했습니다(첫 시도에서 화면이 뒤로 빠지는 문제).
  - F03: 첫 시작 프레임이 F01·F02와 같은 정면 앵글이어서 3/4 클로즈업 시작 프레임(2935c3d0)을 새로 만들었고, 점프는 네 발로 뛰어오르게 바꿨습니다. 최종 F03 = 0cc3de02.
  - F02: 같은 카드로 다시 생성한 테이크(8f910b79)가 프레이밍을 더 잘 지켜 이것을 씁니다. F01→F02는 같은 정면 축에서 와이드→미디엄으로 들어가는 컷입니다.

## 고정 규칙

- **발바닥 규칙(모든 샷)**: 앞발 하나에 작은 동그란 분홍 발가락 패드 **4개**가 호를 이루고 그 아래 더 큰 하트형 분홍 패드 **1개**. 두 앞발 동일. 실제 강아지 앞발 구조와 같고, 기존 샷 다수(0:30, 0:40)와도 같습니다. 패드 시트 이미지 P00을 먼저 만들어 모든 시작 프레임의 참조 2로 씁니다.
- **세트 고정**: PLAYROOM은 2화에서 쓴 세트 한 장(0fbb2f5e, 둥근 창·레몬나무·별 가랜드·작은 무대·무지개 러그)을 그대로 씁니다(채널 연속성). MEADOW는 빈 세트 M00 한 장을 새로 만들어 고정합니다.
- **움직임**: 모든 프롬프트에 실시간 속도, 1박(약 0.6초)마다 동작 하나. «gentle/slow» 계열 단어 없음. 카메라는 고정 또는 추적만(느린 밀기 없음).
- 설정: **Seedance 2.5 · Unlimited · 720p · 16:9 · 오디오 끔**, 길이는 카드 표기. **Rerun 금지**, Generate 버튼에 Unlimited 표시 확인 후 제출. 계정 전체에서 동시에 1개만.
- 비용: 이미지(P00, M00, F01–F11)와 영상 모두 웹 Unlimited로 **0크레딧** 목표.

## 전환 계획 (편집 규칙)

1. 컷은 모두 줄 경계(다운비트)에서. 디졸브·역재생·정지 화면 없음(마지막 0.4초 페이드만).
2. 같은 장면 안에서는 매번 각도가 다릅니다(정면 와이드 → 왼쪽 3/4 → 오른쪽 3/4 …). 같은 방향 컷 없음.
3. 장면 전환은 동작으로 연결: F03 끝에서 위로 뛰어 화면 밖으로 → F04에서 위에서 떨어지며 착지(17.70초). F05 오른쪽으로 퇴장 → F06 왼쪽에서 등장(화면 방향 유지). 36.96초와 41.70초는 장면이 확실히 달라 다운비트 하드 컷.
4. 속도: 원본 1.0배(`-fps_mode passthrough`, 프레임 복제 금지). 1.0배보다 느리게 쓰지 않음. 박수·홉 접촉은 박자 ±2프레임.
5. 슬롯은 `ep1-v3-edl.csv`(11샷, 기존 20슬롯·재사용 9회 → 재사용 0회). 자막은 2–4화와 같은 스타일, 캐릭터를 가리지 않음.

## 검수 (Claude가 클립마다)

0.25초 간격 프레임에서: 발바닥 패드 4+1(보이는 모든 프레임), 귀 없음, 다리 늘어남 없음, 세트가 시작 프레임과 같음, 하늘 파랑(노을 금지), 동작 속도(1박 1동작). FAIL이면 같은 카드로 새 제출 1회, 그래도 FAIL이면 멈추고 보고.

## 준비 이미지 (먼저)

- **P00 패드 시트**: 참조 1 = Yejin 참조 7e21b96a. 프롬프트는 `ep1-v3-startframe-prompts.json`의 `P00_paw_sheet`.
- **M00 MEADOW 세트**: 참조 1 = 캐스트 라인업(스타일만). 프롬프트 `M00_meadow_set`.
- **F01–F11 시작 프레임**: 참조 1 = PLAYROOM 세트 또는 M00, 참조 2 = 승인된 P00. 프롬프트는 같은 JSON.

## 샷 카드

### F01 · PLAYROOM · WIDE front · 10초 · 타임라인 0.00–7.70초

- 시작 프레임: https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261125_050939_868205c2-f48a-429f-a9cc-f19c6aabbd1d.png
- 파일명: `ep1v3_F01_A.mp4`

```
Real-time, natural-speed action, never slow motion. Yejin trots quickly on all four short legs from the right edge to the middle of the rainbow rug, skids to a stop with a little bounce, plops down onto her bottom, tilts her head and lifts one front paw high in a quick happy hello, then pants with an open-mouth smile, her tail wagging fast. Camera: static wide shot. Natural lifelike animal body mechanics with weight, quick small movements and tiny pauses. Soft clay-and-plush 3D animation style. Warm late-morning light from the round window. Yejin is a fluffy white Bichon puppy whose head is a large perfectly round fluffy ball from every angle with no visible ears, about the same width as her body, exactly as in the first frame; no clothing; she never stands upright like a person and never walks on two legs. Her short legs stay short and stubby and never stretch. Each front paw has exactly four small round pink toe beans above one larger pink heart-shaped main pad, exactly as in the first frame; the pads never change shape, size or number. Exactly one character is on screen from the first frame to the last: Yejin, alone. Nobody and nothing else enters the frame. Start exactly from the uploaded first frame and keep every background element from it (round window with the lemon tree, wooden toy shelf, yellow star garland, low wooden stage, rainbow rug, green and pink floor cushions) in place for the whole clip; never replace the background. No text, no letters, no logos.
```

### F02 · PLAYROOM · MED 3/4 from left · 10초 · 타임라인 7.70–12.80초

- 시작 프레임: https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261125_051048_43373646-f926-4b00-83c5-b77970845530.png
- 파일명: `ep1v3_F02_A.mp4`

```
Real-time, natural-speed action, never slow motion. Yejin sits facing the camera and claps to the beat: she spreads her two front paws wide apart to the sides, then smacks them together in front of her chest, again and again, about one clap every 0.6 seconds, the paws clearly separating with a visible gap between every clap, her whole body bouncing on each clap, mouth open singing. Camera: static medium shot. Natural lifelike animal body mechanics with weight, quick small movements and tiny pauses. Soft clay-and-plush 3D animation style. Warm late-morning light from the round window. Yejin is a fluffy white Bichon puppy whose head is a large perfectly round fluffy ball from every angle with no visible ears, about the same width as her body, exactly as in the first frame; no clothing; she never stands upright like a person and never walks on two legs. Her short legs stay short and stubby and never stretch. Each front paw has exactly four small round pink toe beans above one larger pink heart-shaped main pad, exactly as in the first frame; the pads never change shape, size or number. Exactly one character is on screen from the first frame to the last: Yejin, alone. Nobody and nothing else enters the frame. Start exactly from the uploaded first frame and keep every background element from it (round window with the lemon tree, wooden toy shelf, yellow star garland, low wooden stage, rainbow rug, green and pink floor cushions) in place for the whole clip; never replace the background. No text, no letters, no logos.
```

### F03 · PLAYROOM · CU 3/4 from right · 10초 · 타임라인 12.80–17.70초

- 시작 프레임: https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261125_081221_2935c3d0-2a2b-477c-b2ac-1befb78cc1ec.png
- 파일명: `ep1v3_F03_A.mp4`

```
Real-time, natural-speed action, never slow motion. Yejin claps to the beat: she spreads her two front paws wide apart, then smacks them together in front of her chest, again and again, about one clap every 0.6 seconds, bouncing on each clap; after six claps she crouches and springs straight up off her short hind legs in one quick jump, rising out of the top of the frame. Camera: static close-up. Natural lifelike animal body mechanics with weight, quick small movements and tiny pauses. Soft clay-and-plush 3D animation style. Warm late-morning light from the round window. Yejin is a fluffy white Bichon puppy whose head is a large perfectly round fluffy ball from every angle with no visible ears, about the same width as her body, exactly as in the first frame; no clothing; she never stands upright like a person and never walks on two legs. Her short legs stay short and stubby and never stretch. Each front paw has exactly four small round pink toe beans above one larger pink heart-shaped main pad, exactly as in the first frame; the pads never change shape, size or number. Exactly one character is on screen from the first frame to the last: Yejin, alone. Nobody and nothing else enters the frame. Start exactly from the uploaded first frame and keep every background element from it (round window with the lemon tree, wooden toy shelf, yellow star garland, low wooden stage, rainbow rug, green and pink floor cushions) in place for the whole clip; never replace the background. No text, no letters, no logos.
```

### F04 · MEADOW · WIDE front · 5초 · 타임라인 17.70–22.52초

- 시작 프레임: https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261125_044006_5828bd3e-47e3-4925-8213-d8cdfb01bdc6.png
- 파일명: `ep1v3_F04_A.mp4`

```
Real-time, natural-speed action, never slow motion. Yejin lands from the top of her hop onto the grass with a bounce, then springs up off her short hind legs into a quick bouncy hop toward the camera, both front paws lifting at the top of each hop, landing with weight, again and again in a steady rhythm, about one hop every 0.6 seconds; she never stands upright like a person and never trots. Camera: static wide shot. Natural lifelike animal body mechanics with weight, quick small movements and tiny pauses. Soft clay-and-plush 3D animation style. Clear bright blue sky with white clouds and warm late-morning sun the whole time, never sunset, never golden hour. Yejin is a fluffy white Bichon puppy whose head is a large perfectly round fluffy ball from every angle with no visible ears, about the same width as her body, exactly as in the first frame; no clothing; she never stands upright like a person and never walks on two legs. Her short legs stay short and stubby and never stretch. Each front paw has exactly four small round pink toe beans above one larger pink heart-shaped main pad, exactly as in the first frame; the pads never change shape, size or number. Exactly one character is on screen from the first frame to the last: Yejin, alone. Nobody and nothing else enters the frame. Start exactly from the uploaded first frame and keep every background element from it (green meadow, daisies and buttercups, rolling hills, round trees, blue sky with white clouds) in place for the whole clip; never replace the background. No text, no letters, no logos.
```

### F05 · MEADOW · WIDE side tracking L→R · 10초 · 타임라인 22.52–27.18초

- 시작 프레임: https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261125_044020_2833686d-5e9f-4da2-ace5-a8834a094790.png
- 파일명: `ep1v3_F05_A.mp4`

```
Real-time, natural-speed action, never slow motion. Seen from the side, Yejin hops from left to right across the meadow in quick bouncy hops, springing off her short hind legs, front paws lifting at the top of each hop and landing with weight, about one hop every 0.6 seconds, and finally hops out of the frame on the right. Camera: smooth sideways tracking shot that keeps pace with her, then stops and lets her leave the frame. Natural lifelike animal body mechanics with weight, quick small movements and tiny pauses. Soft clay-and-plush 3D animation style. Clear bright blue sky with white clouds and warm late-morning sun the whole time, never sunset, never golden hour. Yejin is a fluffy white Bichon puppy whose head is a large perfectly round fluffy ball from every angle with no visible ears, about the same width as her body, exactly as in the first frame; no clothing; she never stands upright like a person and never walks on two legs. Her short legs stay short and stubby and never stretch. Each front paw has exactly four small round pink toe beans above one larger pink heart-shaped main pad, exactly as in the first frame; the pads never change shape, size or number. Exactly one character is on screen from the first frame to the last: Yejin, alone. Nobody and nothing else enters the frame. Start exactly from the uploaded first frame and keep every background element from it (green meadow, daisies and buttercups, rolling hills, round trees, blue sky with white clouds) in place for the whole clip; never replace the background. No text, no letters, no logos.
```

### F06 · PLAYROOM · MED front · 5초 · 타임라인 27.18–31.92초

- 시작 프레임: https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261125_051416_d6741830-8da7-4f05-bda3-2a95d3df285f.png
- 파일명: `ep1v3_F06_A.mp4`

```
Real-time, natural-speed action, never slow motion. Yejin bounces in place on the left side of the rug, then sits and waves one front paw high side to side quickly, about two waves per second, pads toward the camera, mouth open singing, tail wagging fast. Camera: static medium shot. Natural lifelike animal body mechanics with weight, quick small movements and tiny pauses. Soft clay-and-plush 3D animation style. Warm late-morning light from the round window. Yejin is a fluffy white Bichon puppy whose head is a large perfectly round fluffy ball from every angle with no visible ears, about the same width as her body, exactly as in the first frame; no clothing; she never stands upright like a person and never walks on two legs. Her short legs stay short and stubby and never stretch. Each front paw has exactly four small round pink toe beans above one larger pink heart-shaped main pad, exactly as in the first frame; the pads never change shape, size or number. Exactly one character is on screen from the first frame to the last: Yejin, alone. Nobody and nothing else enters the frame. Start exactly from the uploaded first frame and keep every background element from it (round window with the lemon tree, wooden toy shelf, yellow star garland, low wooden stage, rainbow rug, green and pink floor cushions) in place for the whole clip; never replace the background. No text, no letters, no logos.
```

### F07 · PLAYROOM · CU 3/4 from left · 5초 · 타임라인 31.92–36.96초

- 시작 프레임: https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261125_051509_0df37068-1a49-4c41-8312-453e7b4d3675.png
- 파일명: `ep1v3_F07_A.mp4`

```
Real-time, natural-speed action, never slow motion. Yejin waves her right front paw side to side quickly beside her face, pads toward the camera, then switches and waves her left front paw, bobbing her head to the beat with a big squinting smile. Camera: static close-up. Natural lifelike animal body mechanics with weight, quick small movements and tiny pauses. Soft clay-and-plush 3D animation style. Warm late-morning light from the round window. Yejin is a fluffy white Bichon puppy whose head is a large perfectly round fluffy ball from every angle with no visible ears, about the same width as her body, exactly as in the first frame; no clothing; she never stands upright like a person and never walks on two legs. Her short legs stay short and stubby and never stretch. Each front paw has exactly four small round pink toe beans above one larger pink heart-shaped main pad, exactly as in the first frame; the pads never change shape, size or number. Exactly one character is on screen from the first frame to the last: Yejin, alone. Nobody and nothing else enters the frame. Start exactly from the uploaded first frame and keep every background element from it (round window with the lemon tree, wooden toy shelf, yellow star garland, low wooden stage, rainbow rug, green and pink floor cushions) in place for the whole clip; never replace the background. No text, no letters, no logos.
```

### F08 · MEADOW · MED front · 5초 · 타임라인 36.96–41.70초

- 시작 프레임: https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261125_044036_b79faa1f-5e8d-4683-bf80-ec7afea36212.png
- 파일명: `ep1v3_F08_A.mp4`

```
Real-time, natural-speed action, never slow motion. Yejin claps twice quickly (paws spread wide apart, then smacked together in front of her chest), springs up off her short hind legs into one quick hop and lands with weight, then waves one front paw high side to side quickly; she does this sequence twice in a steady rhythm. Camera: static medium shot. Natural lifelike animal body mechanics with weight, quick small movements and tiny pauses. Soft clay-and-plush 3D animation style. Clear bright blue sky with white clouds and warm late-morning sun the whole time, never sunset, never golden hour. Yejin is a fluffy white Bichon puppy whose head is a large perfectly round fluffy ball from every angle with no visible ears, about the same width as her body, exactly as in the first frame; no clothing; she never stands upright like a person and never walks on two legs. Her short legs stay short and stubby and never stretch. Each front paw has exactly four small round pink toe beans above one larger pink heart-shaped main pad, exactly as in the first frame; the pads never change shape, size or number. Exactly one character is on screen from the first frame to the last: Yejin, alone. Nobody and nothing else enters the frame. Start exactly from the uploaded first frame and keep every background element from it (green meadow, daisies and buttercups, rolling hills, round trees, blue sky with white clouds) in place for the whole clip; never replace the background. No text, no letters, no logos.
```

### F09 · PLAYROOM · MED side from right (stage) · 5초 · 타임라인 41.70–46.62초

- 시작 프레임: https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261125_051841_0ddb6c4c-9e31-4774-9083-89cd7bb67444.png
- 파일명: `ep1v3_F09_A.mp4`

```
Real-time, natural-speed action, never slow motion. On the low wooden stage Yejin claps twice quickly (paws spread wide apart, then smacked together), does one quick hop off her short hind legs and lands with weight, then waves one front paw quickly, mouth open singing. Camera: static medium side shot. Natural lifelike animal body mechanics with weight, quick small movements and tiny pauses. Soft clay-and-plush 3D animation style. Warm late-morning light from the round window. Yejin is a fluffy white Bichon puppy whose head is a large perfectly round fluffy ball from every angle with no visible ears, about the same width as her body, exactly as in the first frame; no clothing; she never stands upright like a person and never walks on two legs. Her short legs stay short and stubby and never stretch. Each front paw has exactly four small round pink toe beans above one larger pink heart-shaped main pad, exactly as in the first frame; the pads never change shape, size or number. Exactly one character is on screen from the first frame to the last: Yejin, alone. Nobody and nothing else enters the frame. Start exactly from the uploaded first frame and keep every background element from it (round window with the lemon tree, wooden toy shelf, yellow star garland, low wooden stage, rainbow rug, green and pink floor cushions) in place for the whole clip; never replace the background. No text, no letters, no logos.
```

### F10 · PLAYROOM · CU front (stage) · 5초 · 타임라인 46.62–51.66초

- 시작 프레임: https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261125_052205_e9ba03e3-dd1f-42bb-8f6c-77d1e97c4c18.png
- 파일명: `ep1v3_F10_A.mp4`

```
Real-time, natural-speed action, never slow motion. Yejin sings happily, bobbing her head left and right on every beat, about one bob every 0.6 seconds, her mouth opening and closing as if singing, her body bouncing, tail wagging fast behind her. Camera: static close-up. Natural lifelike animal body mechanics with weight, quick small movements and tiny pauses. Soft clay-and-plush 3D animation style. Warm late-morning light from the round window. Yejin is a fluffy white Bichon puppy whose head is a large perfectly round fluffy ball from every angle with no visible ears, about the same width as her body, exactly as in the first frame; no clothing; she never stands upright like a person and never walks on two legs. Her short legs stay short and stubby and never stretch. Each front paw has exactly four small round pink toe beans above one larger pink heart-shaped main pad, exactly as in the first frame; the pads never change shape, size or number. Exactly one character is on screen from the first frame to the last: Yejin, alone. Nobody and nothing else enters the frame. Start exactly from the uploaded first frame and keep every background element from it (round window with the lemon tree, wooden toy shelf, yellow star garland, low wooden stage, rainbow rug, green and pink floor cushions) in place for the whole clip; never replace the background. No text, no letters, no logos.
```

### F11 · PLAYROOM · WIDE high 3/4 from left · 10초 · 타임라인 51.66–57.08초

- 시작 프레임: https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261125_052100_a9c03c69-e760-459f-8a62-7123ae0ec1bd.png
- 파일명: `ep1v3_F11_A.mp4`

```
Real-time, natural-speed action, never slow motion. Yejin waves goodbye with one front paw high side to side quickly, then with the other paw, then flops happily onto the pink floor cushion beside her and rolls onto her back with her paws in the air, wiggling. Camera: static wide shot. Natural lifelike animal body mechanics with weight, quick small movements and tiny pauses. Soft clay-and-plush 3D animation style. Warm late-morning light from the round window. Yejin is a fluffy white Bichon puppy whose head is a large perfectly round fluffy ball from every angle with no visible ears, about the same width as her body, exactly as in the first frame; no clothing; she never stands upright like a person and never walks on two legs. Her short legs stay short and stubby and never stretch. Each front paw has exactly four small round pink toe beans above one larger pink heart-shaped main pad, exactly as in the first frame; the pads never change shape, size or number. Exactly one character is on screen from the first frame to the last: Yejin, alone. Nobody and nothing else enters the frame. Start exactly from the uploaded first frame and keep every background element from it (round window with the lemon tree, wooden toy shelf, yellow star garland, low wooden stage, rainbow rug, green and pink floor cushions) in place for the whole clip; never replace the background. No text, no letters, no logos.
```
