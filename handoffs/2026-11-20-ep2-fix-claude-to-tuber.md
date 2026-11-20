# ep2 수정: 자연스러운 움직임 시험 2샷 (claude → tuber)

- 상태: done (2026-11-20 Tuber)
- 요청: 새 "자연스러운 움직임" 프롬프트로 시험 클립 2개를 Unlimited로 만들고, 결과를 이 파일 「결과」에 적어 주세요. **편집은 아직 하지 않습니다.**
- 입력: `episodes/ep2/ep2-generation-pack.md`(시작 프레임 URL), 이 파일
- 완료 기준: `ep2_E02_N1.mp4`, `ep2_E08_N1.mp4` 생성 + 「결과」 기록. max 승인 완료(2026-11-20). 크레딧 0, 웹사이트 Unlimited 720p만 사용.

## 배경

2화 편집본 검수 결과(max 확인):
- 움직임이 너무 느리고 둥실둥실합니다. 원인은 Claude가 모든 프롬프트에 넣은 "smooth gentle motion", "sways gently", "very slow push-in" 같은 표현입니다. max는 **훨씬 사실적이고 자연스러운 움직임**을 원합니다.
- E02_A, E24_A에 귀가 생겼습니다(고개를 좌우로 흔들거나 털을 털 때).
- 편집본에서 대부분 클립이 **25프레임마다 같은 프레임을 한 번 반복**합니다(약 4% 느려지고 1초마다 살짝 끊김). 원본 클립의 fps를 확인해 주세요(「결과」에 기록). 다음 편집부터는 프레임 반복 없이 원본 속도 그대로 써야 합니다.

시험 2샷이 좋으면 Claude가 35개 전체 프롬프트를 같은 방식으로 다시 써서 보냅니다. 그 뒤에 재생성과 재편집(E01 되감기 제거, 박수 정렬 포함)을 합니다.

## 지시

설정: Seedance 2.5 · Unlimited · 720p · 16:9 · 5초 · 오디오 끔 · 시작 프레임 = 팩의 해당 샷 이미지

### 시험 1: E02 (얼굴 클로즈업, 귀 결함 샷) → `ep2_E02_N1.mp4`

```
A real-time, natural-speed shot of Yejin, a fluffy white Bichon puppy, sitting on the grass and looking at the camera. She moves like a real lively puppy filmed at normal speed: quick curious head tilt to one side, a fast happy wiggle of her whole body, tail wagging rapidly, then she opens her mouth in one sharp happy bark and pants with her tongue out. Natural animal body mechanics with weight, quick small movements and tiny pauses, never slow motion. Camera: handheld-feeling static close-up with slight natural drift. Soft clay-and-plush 3D animation style with lifelike puppy motion. Her head is a perfectly round fluffy ball from every angle with no visible ears, no clothing; she never stands upright like a person. Exactly one character is on screen from the first frame to the last: Yejin, alone. Keep the set layout and Yejin exactly as in the first frame. No text, no letters, no logos.
```

### 시험 2: E08 (박수 샷) → `ep2_E08_N1.mp4`

```
A real-time, natural-speed shot of Yejin, a fluffy white Bichon puppy, sitting on the grass facing the camera. Like a real excited puppy, she bounces her front paws up and pats them together quickly in a playful rhythm, about two pats per second, her body bouncing with each pat, tail wagging fast, mouth open in a happy pant. Natural animal body mechanics with weight and quick snappy movements, never slow motion. Camera: static close-up with slight natural drift. Soft clay-and-plush 3D animation style with lifelike puppy motion. Her head is a perfectly round fluffy ball from every angle with no visible ears, no clothing; she never stands upright like a person and never walks on two legs. Exactly one character is on screen from the first frame to the last: Yejin, alone. Keep the set layout and Yejin exactly as in the first frame. No text, no letters, no logos.
```

각 샷 최대 2회(무료). 확인할 것: 귀가 생기는지(0.5초 간격 전체 프레임), 실제 속도로 보이는지, 캐릭터 모양이 시작 프레임과 같은지.

## 결과

(Tuber 작성, 2026-11-20 10:20 KST)

- 원본 클립 fps와 프레임 반복 원인:
  - 승인된 기존 2화 클립 35개 모두 24fps(r_frame_rate·avg_frame_rate 24/1). 34개는 121프레임(5.04초), E23_A만 241프레임(10.04초). 원본에는 연속 중복 프레임이 없습니다.
  - 원인은 Tuber 편집 스크립트입니다. 클립을 trim한 뒤 프레임레이트 정보가 사라져 ffmpeg가 기본값 25fps로 디코딩했고, 그 과정에서 컷 안 27·52·77·102·127번째 프레임 자리에 중복 프레임이 1개씩 들어갔습니다. 요청 프레임 수만큼만 잘라 쓰면서 각 컷 끝의 원본 프레임 1~4개가 빠졌고, 24fps로 인코딩돼 약 4%(25/24) 느려졌습니다. 최종본에서 95곳을 측정으로 확인했습니다.
  - 수정: 디코딩 명령에 `-fps_mode passthrough`를 넣고 프레임 수가 맞는지 검사합니다. 시험에서 요청 프레임과 1:1로 일치했습니다. 다음 편집부터 적용합니다.
- E02_N1:
  - 생성 1회(Unlimited, 크레딧 0, 720p 16:9 5초, 24fps 121프레임). 사이트에 오디오 토글이 없어 오디오 설정은 바꾸지 못했습니다(편집 때 원본 오디오는 쓰지 않습니다).
  - 귀: 0.5초 간격 전체 프레임과 영상 검토 모두에서 없음. 머리는 끝까지 둥근 공 모양. 다른 캐릭터·글자·자세 문제 없음, 세트 안정.
  - 움직임: 기존 E02_A보다 확실히 활발합니다(연속 프레임 평균 차이 1.27 → 2.82, 약 2.2배). 고개 기울임, 몸 흔들기, 4초 무렵 입 벌린 웃음/짖음이 있습니다. 다만 영상 검토 평가는 5점 중 3점으로, 아직 약간 느리고 둥실한 느낌이 남고 "짧고 날카로운 짖음"은 뚜렷하지 않습니다.
  - 파일: https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261120_005527_6364ac10-705c-4f7e-ac45-9b2cdb2f38df.mp4
- E08_N1:
  - 생성 1회(조건 같음).
  - 귀: 없음. 캐릭터·세트 안정, 두 발로 서지 않음.
  - 움직임: 기존 E08_A-v2보다 움직임 양은 많습니다(0.59 → 2.43, 약 4배). 그러나 1초쯤 앞발을 모아 올린 뒤 끝까지 붙인 채 몸만 들썩입니다. 앞발이 떨어졌다 다시 맞닿는 박수는 0회입니다. 영상 검토 평가 3점, 박수 샷으로는 불합격입니다.
  - 파일: https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261120_010907_020348e4-ca9b-448e-b111-152084556e34.mp4
- 특이 사항:
  - 두 번째 시도(각 샷 최대 2회)는 쓰지 않았습니다. 같은 프롬프트로 다시 돌려도 박수가 나올지는 확인 못 함. 프롬프트 방향이 정해지면 바로 재시도할 수 있습니다.
  - 제안(검증 안 됨): 박수는 "paws held together"로 해석되는 것 같습니다. "paws spread apart, then clap together, apart again, clap" 처럼 벌어짐과 맞닿음을 번갈아 적고 횟수(예: 5초에 8번)를 넣으면 나아질 수 있습니다.
  - 생성 한 번에 약 13분 걸렸습니다. 페이지를 새로고침하면 Unlimited가 꺼지므로 매번 확인했고, 크레딧 버튼 상태에서는 누르지 않았습니다.
  - 기존 편집본 문제 중 E01 되감기, 글자 6프레임 이른 표시, 박수 프레임 정렬 미확인은 재편집 때 함께 고칩니다.

작성 규칙: 로컬 파일 경로, 컴퓨터 이름, OS 사용자 이름, 키·토큰·개인 연락처를 적지 않습니다(공개 저장소).

---

## 2차 시험 (TUBER 프로젝트(Claude), 2026-11-20 10:35 KST)

Claude 검수: 1차 결과에 동의합니다. E02_N1은 귀가 없고 움직임이 2배 이상 늘었지만 아직 둥실합니다. E08_N1은 앞발을 붙인 채라 박수 0회로 불합격입니다. 프레임 반복 원인 분석과 `-fps_mode passthrough` 수정은 좋습니다.

각 샷의 남은 1회(무료)를 아래 프롬프트로 써 주세요. 설정은 1차와 같습니다.

### E02 → `ep2_E02_N2.mp4`

```
Fast, energetic, real-time puppy action, never slow motion. Yejin, a fluffy white Bichon puppy, sits on the grass facing the camera. 0-1 s: she snaps her head quickly to one side in a curious tilt. 1-2 s: she wiggles her whole body fast with excitement, tail wagging rapidly. 2-3 s: she does a quick little bounce on her front paws. 3-4 s: she barks once, a short sharp bark with her mouth snapping wide open and closed. 4-5 s: she pants happily with her tongue out. Quick snappy movements with weight and tiny pauses, like a real lively puppy. Camera: static close-up. Soft clay-and-plush 3D animation style. Her head is a perfectly round fluffy ball from every angle with no visible ears, no clothing; she never stands upright like a person. Exactly one character is on screen from the first frame to the last: Yejin, alone. Keep the set layout and Yejin exactly as in the first frame. No text, no letters, no logos.
```

### E08 → `ep2_E08_N2.mp4`

```
Fast, energetic, real-time action, never slow motion. Yejin, a fluffy white Bichon puppy, sits on the grass facing the camera and plays pat-a-cake: she spreads her two front paws wide apart to the sides, then smacks them together in front of her chest, then spreads them wide apart again, then smacks them together again. She does this clap four times, the paws clearly separating with a visible gap between every clap, about two claps per second, her body bouncing on each clap, mouth open in a happy pant. Camera: static close-up. Soft clay-and-plush 3D animation style. Her head is a perfectly round fluffy ball from every angle with no visible ears, no clothing; she never stands upright like a person. Exactly one character is on screen from the first frame to the last: Yejin, alone. Keep the set layout and Yejin exactly as in the first frame. No text, no letters, no logos.
```

### 편집 속도 시험 (무료)
E02_N1을 1.15배와 1.25배로 빠르게 한 5초 미리보기 두 개도 만들어 주세요(보간 없이 프레임 건너뛰기, 24fps 유지). 생성 클립 속도를 올리면 둥실한 느낌이 얼마나 줄어드는지 비교하려는 것입니다.

### 2차 결과 (Tuber 작성, 2026-11-20 10:55 KST)

두 샷 모두 각 1회, Unlimited, 크레딧 0, 720p 16:9 5초(24fps 121프레임)로 만들었습니다. 이로써 각 샷 무료 2회를 모두 썼습니다.

- E02_N2:
  - 귀: 없음(0.5초 간격 프레임과 영상 검토 모두). 다른 캐릭터·글자 없음, 세트 안정, 두 발로 서지 않음.
  - 움직임: 영상 검토 2/5로 불합격. 1~2초 사이에 빠르게 몸을 흔드는 대신 몸이 납작하게 땅으로 퍼지는 변형이 생깁니다. 앞발 바운스는 없습니다. 연속 프레임 평균 차이는 2.96(N1 2.82)으로 움직임 양은 비슷합니다.
  - 짖음: 3초쯤 입이 열리고 끝까지 벌린 채 헐떡여서, 열렸다 닫히는 짧은 짖음은 없습니다.
  - 파일: https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261120_013029_facdb7b1-84f7-4628-af70-e4b32b3acaad.mp4
  - 결론: 1차 E02_N1이 더 낫습니다.
- E08_N2:
  - 박수: 앞발이 양옆으로 벌어졌다 가슴 앞에서 모이는 동작은 확실히 생겼습니다(1차는 0회). 횟수는 두 결과가 다릅니다. Tuber가 초당 6프레임으로 앞발 부분을 잘라 세어 보면 5초 동안 벌어짐→모임이 약 6~7번(초당 약 1.3~1.4회)입니다. 영상 검토는 "떨어졌다 확실히 닿는 박수"를 2회(약 1초, 4초)로 셌습니다. 모일 때 세게 부딪히지 않고 부드럽게 붙는 경우가 많아서인 것으로 보입니다. 정확한 횟수는 확인 못 함.
  - 귀: 없음. 캐릭터·세트 안정, 두 발로 서지 않음, 다른 캐릭터·글자 없음.
  - 결함: 팔이 반죽처럼 살짝 늘어나고, 앞발 분홍 패드가 벌렸을 때만 보이고 모으면 사라집니다. 요청한 초당 2회보다 느립니다. 연속 프레임 평균 차이 1.14(N1 2.43, 몸 들썩임이 줄어든 대신 앞발만 움직임).
  - 파일: https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261120_014247_19d97936-ac71-479a-b190-f5a05cbc1691.mp4
  - 결론: 박수 동작 자체는 처음으로 성공. 속도와 "맞닿음" 강도는 부족해 조건부 통과.
- 속도 미리보기(E02_N1, 보간 없이 프레임 건너뛰기, 24fps):
  - 1.15배: 4.38초 105프레임. 영상 검토 4/5. 둥실한 느낌이 줄고 실제 속도에 가깝다는 평가. 프레임 건너뛰기로 아주 약한 끊김.
  - 1.25배: 4.04초 97프레임. 영상 검토 3/5. 인위적으로 빨라 보이고 끊김이 느껴짐.
  - 원본이 5.04초라 빠르게 하면 5초보다 짧아집니다(5초 길이로는 못 만듦). 파일은 Tuber 작업 컴퓨터에 저장됨(공개 URL 없음).
  - 소감: 1.15배가 가장 자연스럽습니다. 편집에서 1.15배를 쓰면 컷 길이를 채우는 데 원본이 약 15% 더 필요합니다.
- 특이 사항:
  - 한 번에 1개만 생성되는 Unlimited 제한 안내가 기록상 진행 중인 작업이 없을 때도 떴습니다. 약 7분 기다린 뒤 제출됐고 E08은 1번만 제출됐습니다.
  - 제안(검증 안 됨): 초 단위 시간표 프롬프트는 동작이 덜 지켜졌습니다(E02_N2). 박수는 "spread wide, then smack together" 표현이 효과가 있었습니다. 1차식 짧은 묘사에 박수 표현만 더하고, 편집에서 1.15배 속도를 쓰는 조합이 현실적일 수 있습니다.


---

## 3차 지시 (TUBER 프로젝트(Claude), 2026-11-20 11:55 KST)

2차 결과 확인했습니다. Claude도 E08_N2 앞발 크롭에서 벌렸다 모으는 동작을 약 7회(약 0.67초 간격) 셌습니다. 편집에서 1.25배로 쓰면 0.53초 간격이 되어 곡 박자(112.9 BPM)와 맞습니다. 판단: **E08_N2 방식 채택, E02는 1차(N1) 방식 채택, 편집 속도 일반 1.15배·박수 1.25배.**

다음 프롬프트 방향은 새 팩 `episodes/ep2/ep2-pack-v3-natural.md`(이 브랜치)에 24샷 전부 정리했습니다. 박수 카드에는 팔 늘어남·발바닥 사라짐을 막는 문장을 넣었습니다.

- **전체 재생성(35회)은 max 승인 후에 시작합니다.** 승인되면 다시 알립니다.
- 지금 해도 되는 것(무료, 1회): 팩 v3의 E08 카드로 `ep2_E08_N3.mp4` 한 번 생성해 팔 늘어남이 줄었는지 확인. 결과를 아래에 적어 주세요.
- Rerun 버튼 금지(Unlimited가 꺼진 채 유료 제출됨). 무료 Seedance는 브라우저 스레드와 번갈아 씁니다.

### 3차 결과 (Tuber가 작성)
- E08_N3 (`ep2_E08_N3.mp4`, 2026-11-20 11:53 KST 제출, 무료 Unlimited, 1회, Rerun 안 씀): https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261120_025318_07d0d180-a686-4def-b06d-b9b3ccfd1bdf.mp4
  - 사양: 1280x720, 24fps, 121프레임(5.04초). 첫 프레임이 E08 시작 그림과 같음(눈으로 확인).
  - 박수: 앞발 크롭 6fps 프레임으로 세면 벌렸다 모으는 동작 약 5회(약 1초 간격). 영상 검토 모델은 1초 간격 스틸만 보고 1회로 셌는데, 1초 간격이면 박수 주기와 겹쳐 놓칠 수 있어 정확한 횟수는 확인 못 함. N2(약 0.67초 간격)보다 느릴 수 있음.
  - 팔 늘어남: 없음 또는 약간(N2보다 줄어든 것으로 보임). 앞다리가 짧게 유지됨.
  - 발바닥: 벌렸을 때 분홍 발바닥이 보이지만, 모았을 때는 발등만 보여 발바닥이 안 보임(녹아내림은 없음).
  - 귀 없음, 다른 캐릭터 없음, 글자 없음, 사람처럼 서기 없음, 몸 녹음 없음. 움직임 지표 1.34(N2 1.14).
  - 판단: 실패 기준(귀, 다른 캐릭터, 몸 녹음, 박수 0회)에 해당하지 않아 `ep2_E08_A3`로 사용 예정. 영상 검토 모델 평점은 1/5(느리고 박수 1회로 봄)라 편집 때 박수 구간을 다시 확인함.
