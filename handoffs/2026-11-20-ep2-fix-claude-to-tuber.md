# ep2 수정: 자연스러운 움직임 시험 2샷 (claude → tuber)

- 상태: open
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

(Tuber가 작성)
- 원본 클립 fps(기존 2화 클립 기준)와 프레임 반복 원인:
- E02_N1: 생성 횟수, 귀 여부, 움직임 소감, 파일 위치(공개 URL 또는 "max의 PC에 로컬 저장됨")
- E08_N1: 같은 항목
- 특이 사항:

작성 규칙: 로컬 파일 경로, 컴퓨터 이름, OS 사용자 이름, 키·토큰·개인 연락처를 적지 않습니다(공개 저장소).
