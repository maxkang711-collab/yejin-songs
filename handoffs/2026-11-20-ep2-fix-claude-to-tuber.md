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
