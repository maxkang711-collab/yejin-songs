# ep2 «Yejin Is Her Name-O (Bingo)» 생성 팩 (Tuber용)

작성: 2026-11-19 (KST), Claude. 규칙서: [`bible/01-style-production-bible.md`](../../bible/01-style-production-bible.md)

## 1. 요약

- 곡: 전래 동요 «Bingo»(1778년 기록, 퍼블릭 도메인)를 Yejin 이름(Y-E-J-I-N)으로 개사. Suno 새 편곡.
- 음원: Suno 곡 ID `99fa56ab-4102-4461-a88b-63c334127bd0` (테이크 2, 148.64초, 112.9 BPM, G장조, 4/4). 링크: https://suno.com/song/99fa56ab-4102-4461-a88b-63c334127bd0 (테이크 1은 일부 가사 누락 판정으로 미사용)
- 음원 파일은 max가 Suno에서 MP3로 내려받아 Tuber에게 전달합니다(다운로드 크레딧 1개 사용).
- 이야기: Yejin 소개(정원) → 친구 Pip 등장(정원) → 실내 놀이(놀이방) → 간주에 연못으로 달려감 → 연못 놀이 2절 → 정원으로 돌아와 비눗방울 축하 → 작별 인사.
- 노래는 화면 밖 내레이터가 부릅니다. **립싱크 없음.** Yejin은 박자에 맞춰 반응하고 "Woof!" 지점에서만 입을 크게 벌립니다.
- 생성: Higgsfield 웹사이트, Seedance 2.5, **Unlimited(무료)**, 720p, 16:9. 고유 샷 24개, 총 35회 생성(11개 샷은 2테이크).
- 화면 글자(Y E J I N, 박수 아이콘)는 생성하지 말고 편집에서 그래픽으로 얹습니다.

## 2. Tuber 작업 순서

1. 아래 3절의 샷 카드를 E01부터 순서대로 생성합니다. 설정: Seedance 2.5 · Unlimited · 720p · 16:9 · 길이(카드에 표시) · 오디오 끔.
2. 시작 프레임(Start frame / First frame)에 카드의 이미지 URL 그림을 넣습니다. 웹 UI가 URL을 받지 않으면 이미지를 내려받아 업로드합니다.
3. 웹 UI에 참조 이미지(Reference) 칸이 있으면 캐스트 라인업을 함께 넣습니다: https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261119_100035_d48b6ee4-b469-4564-8904-98cbea88c1ff.png
4. 프롬프트 칸에 카드의 영문 프롬프트를 그대로 붙여넣습니다.
5. 결과를 바이블 8절 기준으로 검수합니다: 귀 없음, 옷 없음, 사람처럼 서지 않음, 화면 글자 없음, 캐릭터 수 정확, 세트 배치 유지, 손발 녹아내림 없음. 실패하면 같은 설정으로 한 번 더 생성합니다(무료).
6. 결과 영상 URL을 이 저장소의 `handoffs/2026-11-19-ep2-claude-to-tuber.md` "결과" 절에 샷별로 적습니다.
7. 4절 EDL대로 편집합니다. 편집 규칙은 바이블 7절(다운비트 컷, 박수 정렬, 글자 그래픽)을 따릅니다.
8. **만약 Unlimited가 막히거나 크레딧이 차감되는 화면이 나오면 생성을 멈추고 `상태: blocked`로 적어 주세요.** 유료 생성은 max 승인 없이 하지 않습니다.

## 3. 샷별 생성 카드 (24샷, 복사해서 그대로 붙여넣기)

공통: Seedance 2.5 · **Unlimited** · **720p** · **16:9** · 오디오 끔 · 시작 프레임 = 아래 이미지 URL · (선택) 참조 이미지 = 캐스트 라인업 URL

`테이크` 열이 `A+B`인 샷은 같은 설정으로 **2번** 생성합니다(B는 재사용 구간용). 총 생성 횟수: 35회.

### E01 · GARDEN · WIDE→밀기 · 10초 · 테이크 B

- 내용: 오프닝: 개집에서 빼꼼, 나와서 앉기
- 시작 프레임: https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261119_100630_718c5c7c-8aa8-4958-af36-c85867f6826a.png
- 파일명 규칙: `ep2_E01_A.mp4`
- 프롬프트:

```
Yejin peeks out of the doghouse door, then trots out happily on all four legs along the stepping stones to the center of the lawn, sits down facing the camera and wags her tail. Camera: static wide shot, then a very slow push-in. Soft clay-and-plush 3D preschool animation, warm late-morning light from upper left, low contrast, smooth gentle motion. Yejin is the round fluffy white puppy with a ball-shaped head and no visible ears, no clothing; she never stands upright like a person and never walks on two legs. Pip is the small yellow duckling with a light sky-blue knitted scarf. Keep the set layout and both characters exactly as in the first frame. No text, no letters, no logos, no extra characters.
```

### E02 · GARDEN · CU 정지 · 5초 · 테이크 A+B

- 내용: Yejin 얼굴, 박자 고개 까딱 → 멍!
- 시작 프레임: https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261119_100629_d230eac3-205b-4a32-a6af-0c5305052784.png
- 파일명 규칙: `ep2_E02_A.mp4`, `ep2_E02_B.mp4`
- 프롬프트:

```
Yejin looks at the camera and bobs her head left and right in a steady happy rhythm three times, then opens her mouth wide in one happy bark and ends with a big smile. Camera: static close-up. Soft clay-and-plush 3D preschool animation, warm late-morning light from upper left, low contrast, smooth gentle motion. Yejin is the round fluffy white puppy with a ball-shaped head and no visible ears, no clothing; she never stands upright like a person and never walks on two legs. Pip is the small yellow duckling with a light sky-blue knitted scarf. Keep the set layout and both characters exactly as in the first frame. No text, no letters, no logos, no extra characters.
```

### E03 · GARDEN · MED 밀기 · 5초 · 테이크 A

- 내용: 'There is a puppy' 몸 흔들기
- 시작 프레임: https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261119_100630_166baa16-8272-4fe5-a17a-e6bd8cba142b.png
- 파일명 규칙: `ep2_E03_A.mp4`
- 프롬프트:

```
Yejin sways her body gently side to side in a steady rhythm, her fluffy fur bouncing softly, smiling at the camera. Camera: slow push-in. Soft clay-and-plush 3D preschool animation, warm late-morning light from upper left, low contrast, smooth gentle motion. Yejin is the round fluffy white puppy with a ball-shaped head and no visible ears, no clothing; she never stands upright like a person and never walks on two legs. Pip is the small yellow duckling with a light sky-blue knitted scarf. Keep the set layout and both characters exactly as in the first frame. No text, no letters, no logos, no extra characters.
```

### E04 · GARDEN · MED 로우앵글 · 5초 · 테이크 A+B

- 내용: 'Yejin is her name-o' 자랑 포즈
- 시작 프레임: https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261119_100629_6e432a63-a3bb-45e0-86bd-fa8046a8006e.png
- 파일명 규칙: `ep2_E04_A.mp4`, `ep2_E04_B.mp4`
- 프롬프트:

```
Yejin sits proudly in front of her doghouse, puffs up her fluffy chest, nods once and wags her tail fast while the yellow star above her twinkles. Camera: static low angle with a tiny push-in. Soft clay-and-plush 3D preschool animation, warm late-morning light from upper left, low contrast, smooth gentle motion. Yejin is the round fluffy white puppy with a ball-shaped head and no visible ears, no clothing; she never stands upright like a person and never walks on two legs. Pip is the small yellow duckling with a light sky-blue knitted scarf. Keep the set layout and both characters exactly as in the first frame. No text, no letters, no logos, no extra characters.
```

### E05 · GARDEN · CU 3/4 · 5초 · 테이크 A

- 내용: 고개 돌려 카메라 보고 갸웃·끄덕
- 시작 프레임: https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261119_100631_2012d1dc-02e4-4d95-833f-b306e43eac20.png
- 파일명 규칙: `ep2_E05_A.mp4`
- 프롬프트:

```
Yejin turns her head from the left to face the camera, tilts her head cutely, then nods happily twice. Camera: static close-up. Soft clay-and-plush 3D preschool animation, warm late-morning light from upper left, low contrast, smooth gentle motion. Yejin is the round fluffy white puppy with a ball-shaped head and no visible ears, no clothing; she never stands upright like a person and never walks on two legs. Pip is the small yellow duckling with a light sky-blue knitted scarf. Keep the set layout and both characters exactly as in the first frame. No text, no letters, no logos, no extra characters.
```

### E06 · GARDEN · WIDE 2S · 5초 · 테이크 A

- 내용: Pip 등장, 날개 인사
- 시작 프레임: https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261119_100631_cc6c2a64-8c94-42ac-88ea-9a549b81664c.png
- 파일명 규칙: `ep2_E06_A.mp4`
- 프롬프트:

```
Pip waddles along the stepping stones toward Yejin, waving one little wing hello; Yejin turns toward Pip, her tail wagging fast. Camera: static wide shot. Soft clay-and-plush 3D preschool animation, warm late-morning light from upper left, low contrast, smooth gentle motion. Yejin is the round fluffy white puppy with a ball-shaped head and no visible ears, no clothing; she never stands upright like a person and never walks on two legs. Pip is the small yellow duckling with a light sky-blue knitted scarf. Keep the set layout and both characters exactly as in the first frame. No text, no letters, no logos, no extra characters.
```

### E07 · GARDEN · MED 2S 밀기 · 5초 · 테이크 A+B

- 내용: 둘이 마주 보고 카메라 보며 끄덕
- 시작 프레임: https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261119_100630_dd8cca67-9408-482f-a69f-4f1ead9dffe3.png
- 파일명 규칙: `ep2_E07_A.mp4`, `ep2_E07_B.mp4`
- 프롬프트:

```
Yejin and Pip look at each other, then both turn to the camera and nod happily together twice in rhythm. Camera: slow push-in. Soft clay-and-plush 3D preschool animation, warm late-morning light from upper left, low contrast, smooth gentle motion. Yejin is the round fluffy white puppy with a ball-shaped head and no visible ears, no clothing; she never stands upright like a person and never walks on two legs. Pip is the small yellow duckling with a light sky-blue knitted scarf. Keep the set layout and both characters exactly as in the first frame. No text, no letters, no logos, no extra characters.
```

### E08 · GARDEN · CU Yejin · 5초 · 테이크 A+B

- 내용: Yejin 앞발 박수 3번
- 시작 프레임: https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261119_100629_49c669d5-aa1c-49ae-be09-5a2f3ff62df2.png
- 파일명 규칙: `ep2_E08_A.mp4`, `ep2_E08_B.mp4`
- 프롬프트:

```
Yejin claps her two fluffy front paws together three times in a clear steady rhythm, paws touching in front of her chest, smiling at the camera. Camera: static close-up. Soft clay-and-plush 3D preschool animation, warm late-morning light from upper left, low contrast, smooth gentle motion. Yejin is the round fluffy white puppy with a ball-shaped head and no visible ears, no clothing; she never stands upright like a person and never walks on two legs. Pip is the small yellow duckling with a light sky-blue knitted scarf. Keep the set layout and both characters exactly as in the first frame. No text, no letters, no logos, no extra characters.
```

### E09 · GARDEN · CU Pip · 5초 · 테이크 A+B

- 내용: Pip 날개 박수 3번
- 시작 프레임: https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261119_100629_486f2b9b-e77e-487f-969c-f7ad3cd53d5b.png
- 파일명 규칙: `ep2_E09_A.mp4`, `ep2_E09_B.mp4`
- 프롬프트:

```
Pip claps both little wings together three times in a clear steady rhythm in front of the chest, beak open in a happy smile. Camera: static close-up. Soft clay-and-plush 3D preschool animation, warm late-morning light from upper left, low contrast, smooth gentle motion. Yejin is the round fluffy white puppy with a ball-shaped head and no visible ears, no clothing; she never stands upright like a person and never walks on two legs. Pip is the small yellow duckling with a light sky-blue knitted scarf. Keep the set layout and both characters exactly as in the first frame. No text, no letters, no logos, no extra characters.
```

### E10 · PLAYROOM · WIDE 2S · 5초 · 테이크 A

- 내용: Pip 쿠션 트램펄린, Yejin 웃음
- 시작 프레임: https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261119_100631_4035a9d1-0c0e-4457-9220-eeab2614012e.png
- 파일명 규칙: `ep2_E10_A.mp4`
- 프롬프트:

```
Pip bounces up and down twice on the soft mint-green cushion like a trampoline; Yejin on the rainbow rug laughs and wags her tail. Camera: static wide shot. Soft clay-and-plush 3D preschool animation, warm late-morning light from upper left, low contrast, smooth gentle motion. Yejin is the round fluffy white puppy with a ball-shaped head and no visible ears, no clothing; she never stands upright like a person and never walks on two legs. Pip is the small yellow duckling with a light sky-blue knitted scarf. Keep the set layout and both characters exactly as in the first frame. No text, no letters, no logos, no extra characters.
```

### E11 · PLAYROOM · MED · 5초 · 테이크 A+B

- 내용: 실로폰 치기
- 시작 프레임: https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261119_100628_4ee3d6da-ea5a-4a7d-b48a-e031c98fde57.png
- 파일명 규칙: `ep2_E11_A.mp4`, `ep2_E11_B.mp4`
- 프롬프트:

```
Yejin taps the colorful xylophone bars with one front paw, three gentle taps from left to right, then looks up at the camera delighted. Camera: static. Soft clay-and-plush 3D preschool animation, warm late-morning light from upper left, low contrast, smooth gentle motion. Yejin is the round fluffy white puppy with a ball-shaped head and no visible ears, no clothing; she never stands upright like a person and never walks on two legs. Pip is the small yellow duckling with a light sky-blue knitted scarf. Keep the set layout and both characters exactly as in the first frame. No text, no letters, no logos, no extra characters.
```

### E12 · PLAYROOM · MED 2S 측면 · 5초 · 테이크 A

- 내용: 둘이 함께 박수
- 시작 프레임: https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261119_100630_29a7906e-ecbb-4b4e-bb48-a4c0396f5ddb.png
- 파일명 규칙: `ep2_E12_A.mp4`
- 프롬프트:

```
Yejin and Pip clap together three times in a steady rhythm, paws and wings touching in front of their chests, smiling at each other. Camera: slow small arc to the left. Soft clay-and-plush 3D preschool animation, warm late-morning light from upper left, low contrast, smooth gentle motion. Yejin is the round fluffy white puppy with a ball-shaped head and no visible ears, no clothing; she never stands upright like a person and never walks on two legs. Pip is the small yellow duckling with a light sky-blue knitted scarf. Keep the set layout and both characters exactly as in the first frame. No text, no letters, no logos, no extra characters.
```

### E13 · PLAYROOM · CU Yejin · 5초 · 테이크 A

- 내용: Yejin 박수 3번(실내)
- 시작 프레임: https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261119_100713_28feec3d-14fb-438d-a3d2-50b5439ab5bd.png
- 파일명 규칙: `ep2_E13_A.mp4`
- 프롬프트:

```
Yejin claps her front paws together three times in a steady rhythm, then smiles at the camera. Camera: static close-up. Soft clay-and-plush 3D preschool animation, warm late-morning light from upper left, low contrast, smooth gentle motion. Yejin is the round fluffy white puppy with a ball-shaped head and no visible ears, no clothing; she never stands upright like a person and never walks on two legs. Pip is the small yellow duckling with a light sky-blue knitted scarf. Keep the set layout and both characters exactly as in the first frame. No text, no letters, no logos, no extra characters.
```

### E14 · PLAYROOM · MED 무대 밀기 · 5초 · 테이크 A

- 내용: 무대 위 춤, 쇼 포즈
- 시작 프레임: https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261119_100714_e7eb7a0a-31c4-4876-863f-0c1cc86119bd.png
- 파일명 규칙: `ep2_E14_A.mp4`
- 프롬프트:

```
On the little stage, Yejin and Pip sway side to side together in rhythm, then Yejin lifts one front paw and Pip lifts one wing up high in a happy show pose; the star garland swings gently. Camera: slow push-in. Soft clay-and-plush 3D preschool animation, warm late-morning light from upper left, low contrast, smooth gentle motion. Yejin is the round fluffy white puppy with a ball-shaped head and no visible ears, no clothing; she never stands upright like a person and never walks on two legs. Pip is the small yellow duckling with a light sky-blue knitted scarf. Keep the set layout and both characters exactly as in the first frame. No text, no letters, no logos, no extra characters.
```

### E15 · POND · WIDE 트래킹 · 5초 · 테이크 A

- 내용: 연못으로 달려가기(간주)
- 시작 프레임: https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261119_100711_fadf24d3-6929-4106-adbf-9eccfc51581c.png
- 파일명 규칙: `ep2_E15_A.mp4`
- 프롬프트:

```
Yejin bounds forward happily on all four legs like a puppy and Pip waddles quickly beside her, both moving from left to right along the grassy bank toward the pond. Camera: slow tracking move to the right. Soft clay-and-plush 3D preschool animation, warm late-morning light from upper left, low contrast, smooth gentle motion. Yejin is the round fluffy white puppy with a ball-shaped head and no visible ears, no clothing; she never stands upright like a person and never walks on two legs. Pip is the small yellow duckling with a light sky-blue knitted scarf. Keep the set layout and both characters exactly as in the first frame. No text, no letters, no logos, no extra characters.
```

### E16 · POND · MED · 5초 · 테이크 A

- 내용: Pip 연잎 위 착지, 첨벙
- 시작 프레임: https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261119_100716_c2a7b9ab-ce70-4a44-925f-965439b9026b.png
- 파일명 규칙: `ep2_E16_A.mp4`
- 프롬프트:

```
Pip hops on the lily pad, lands with a tiny splash, wobbles and laughs; Yejin on the bank wags her tail and bobs her head. Camera: static. Soft clay-and-plush 3D preschool animation, warm late-morning light from upper left, low contrast, smooth gentle motion. Yejin is the round fluffy white puppy with a ball-shaped head and no visible ears, no clothing; she never stands upright like a person and never walks on two legs. Pip is the small yellow duckling with a light sky-blue knitted scarf. Keep the set layout and both characters exactly as in the first frame. No text, no letters, no logos, no extra characters.
```

### E17 · POND · CU 밀기 · 5초 · 테이크 A+B

- 내용: 연못가 Yejin 얼굴, 박자 끄덕
- 시작 프레임: https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261119_100714_c7577519-c34f-41b3-b114-6655a3759bd7.png
- 파일명 규칙: `ep2_E17_A.mp4`, `ep2_E17_B.mp4`
- 프롬프트:

```
Yejin looks at the camera, bobs her head in rhythm and blinks happily while the water sparkles behind her. Camera: very slow push-in. Soft clay-and-plush 3D preschool animation, warm late-morning light from upper left, low contrast, smooth gentle motion. Yejin is the round fluffy white puppy with a ball-shaped head and no visible ears, no clothing; she never stands upright like a person and never walks on two legs. Pip is the small yellow duckling with a light sky-blue knitted scarf. Keep the set layout and both characters exactly as in the first frame. No text, no letters, no logos, no extra characters.
```

### E18 · POND · MED 2S · 5초 · 테이크 A+B

- 내용: 강둑과 연잎에서 함께 박수
- 시작 프레임: https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261119_100712_d3597c34-0c06-489a-8568-7866834ef5a6.png
- 파일명 규칙: `ep2_E18_A.mp4`, `ep2_E18_B.mp4`
- 프롬프트:

```
Yejin on the bank and Pip on the lily pad clap together three times in a steady rhythm while tiny water droplets sparkle. Camera: static. Soft clay-and-plush 3D preschool animation, warm late-morning light from upper left, low contrast, smooth gentle motion. Yejin is the round fluffy white puppy with a ball-shaped head and no visible ears, no clothing; she never stands upright like a person and never walks on two legs. Pip is the small yellow duckling with a light sky-blue knitted scarf. Keep the set layout and both characters exactly as in the first frame. No text, no letters, no logos, no extra characters.
```

### E19 · POND · WIDE 다리 · 5초 · 테이크 A

- 내용: 다리 건너기(간주)
- 시작 프레임: https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261119_100712_4c8548fe-eb6c-4fd9-b773-da9324750df5.png
- 파일명 규칙: `ep2_E19_A.mp4`
- 프롬프트:

```
Yejin and Pip walk together across the wooden bridge from left to center, Yejin on all four legs and Pip waddling, then stop and look at the camera. Camera: static wide shot. Soft clay-and-plush 3D preschool animation, warm late-morning light from upper left, low contrast, smooth gentle motion. Yejin is the round fluffy white puppy with a ball-shaped head and no visible ears, no clothing; she never stands upright like a person and never walks on two legs. Pip is the small yellow duckling with a light sky-blue knitted scarf. Keep the set layout and both characters exactly as in the first frame. No text, no letters, no logos, no extra characters.
```

### E20 · POND · MED 2S 다리 · 5초 · 테이크 A

- 내용: 다리 위에서 함께 끄덕
- 시작 프레임: https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261119_100711_c1e1b1ae-1a53-4d5e-a67c-8998a24e3644.png
- 파일명 규칙: `ep2_E20_A.mp4`
- 프롬프트:

```
Yejin and Pip on the bridge bounce gently in rhythm and nod together twice, smiling at the camera. Camera: slow push-in. Soft clay-and-plush 3D preschool animation, warm late-morning light from upper left, low contrast, smooth gentle motion. Yejin is the round fluffy white puppy with a ball-shaped head and no visible ears, no clothing; she never stands upright like a person and never walks on two legs. Pip is the small yellow duckling with a light sky-blue knitted scarf. Keep the set layout and both characters exactly as in the first frame. No text, no letters, no logos, no extra characters.
```

### E21 · GARDEN · WIDE 비눗방울 · 5초 · 테이크 A+B

- 내용: 비눗방울, Yejin 코로 톡
- 시작 프레임: https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261119_101205_d6deccc9-8526-4ae1-83e9-1c21ee8f8bfd.png
- 파일명 규칙: `ep2_E21_A.mp4`, `ep2_E21_B.mp4`
- 프롬프트:

```
Shiny soap bubbles float down; from her sitting position Yejin springs up off her short hind legs into a small soft hop to boop a bubble with her nose and it pops into sparkles, then she lands softly; Pip flaps both wings happily. Camera: static wide shot, then a very slow push-in. Soft clay-and-plush 3D preschool animation, warm late-morning light from upper left, low contrast, smooth gentle motion. Yejin is the round fluffy white puppy with a ball-shaped head and no visible ears, no clothing; she never stands upright like a person and never walks on two legs. Pip is the small yellow duckling with a light sky-blue knitted scarf. Keep the set layout and both characters exactly as in the first frame. No text, no letters, no logos, no extra characters.
```

### E22 · GARDEN · MED 2S · 5초 · 테이크 A+B

- 내용: 피날레 빠른 박수
- 시작 프레임: https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261119_100714_08953874-1aaa-4991-bed3-adc1516ed503.png
- 파일명 규칙: `ep2_E22_A.mp4`, `ep2_E22_B.mp4`
- 프롬프트:

```
Yejin and Pip clap together quickly and happily four times while soap bubbles float around them. Camera: static. Soft clay-and-plush 3D preschool animation, warm late-morning light from upper left, low contrast, smooth gentle motion. Yejin is the round fluffy white puppy with a ball-shaped head and no visible ears, no clothing; she never stands upright like a person and never walks on two legs. Pip is the small yellow duckling with a light sky-blue knitted scarf. Keep the set layout and both characters exactly as in the first frame. No text, no letters, no logos, no extra characters.
```

### E23 · GARDEN · MED 2S→빼기 · 10초 · 테이크 A

- 내용: 작별 인사, 와이드로 빠지기
- 시작 프레임: https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261119_100711_aa6973d8-3b7c-45c5-ad5a-0fe9e420b9be.png
- 파일명 규칙: `ep2_E23_A.mp4`
- 프롬프트:

```
Yejin and Pip wave goodbye to the camera together, Yejin with one front paw and Pip with one wing, smiling warmly; then the camera slowly pulls back to a wide shot of the whole garden while they keep waving. Soft clay-and-plush 3D preschool animation, warm late-morning light from upper left, low contrast, smooth gentle motion. Yejin is the round fluffy white puppy with a ball-shaped head and no visible ears, no clothing; she never stands upright like a person and never walks on two legs. Pip is the small yellow duckling with a light sky-blue knitted scarf. Keep the set layout and both characters exactly as in the first frame. No text, no letters, no logos, no extra characters.
```

### E24 · POND · MED · 5초 · 테이크 A+B

- 내용: Pip이 물 튀기고 Yejin 털 털기 (16번 시작 프레임 재사용)
- 시작 프레임: https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261119_100716_c2a7b9ab-ce70-4a44-925f-965439b9026b.png
- 파일명 규칙: `ep2_E24_A.mp4`, `ep2_E24_B.mp4`
- 프롬프트:

```
Pip flaps both wings on the lily pad and splashes a little water onto Yejin; Yejin shakes her fluffy white fur, droplets flying, and laughs. Camera: static. Soft clay-and-plush 3D preschool animation, warm late-morning light from upper left, low contrast, smooth gentle motion. Yejin is the round fluffy white puppy with a ball-shaped head and no visible ears, no clothing; she never stands upright like a person and never walks on two legs. Pip is the small yellow duckling with a light sky-blue knitted scarf. Keep the set layout and both characters exactly as in the first frame. No text, no letters, no logos, no extra characters.
```

## 4. 편집 결정 목록 (EDL)

시각은 음원 기준 초입니다. 모든 컷은 Suno 박 분석의 다운비트(마디 첫 박, 마디 길이 약 2.13초)에 맞췄습니다. 가사 위치는 Suno 청취 분석 기준이며, 보컬은 다운비트보다 0.2~0.3초 먼저 들어옵니다(정상). 기계 판독용: `ep2-edl.csv`.

| 슬롯 | 구간 | 가사 | 시작 | 끝 | 길이 | 소스 | 소스 구간(초) | 메모 |
|---|---|---|---|---|---|---|---|---|
| 01 | Intro | (Woof woof!) | 0.00 | 2.14 | 2.14 | E01_A | 0.00-2.14 |  |
| 02 | V1 | Hello, friends! | 2.14 | 6.49 | 4.35 | E01_A | 2.14-6.49 | 나와서 앉기 |
| 03 | V1 | There is a puppy, soft and white | 6.49 | 10.79 | 4.30 | E03_A | 0.00-4.30 |  |
| 04 | V1 | And Yejin is her name-o | 10.79 | 15.06 | 4.27 | E04_A | 0.00-4.27 | 그래픽: YEJIN 이름 카드 |
| 05 | V1 | Y-E-J-I-N | 15.06 | 17.20 | 2.14 | E02_A | 0.00-2.14 | 글자 Y E J I N 박자마다 팝 |
| 06 | V1 | Y-E-J-I-N | 17.20 | 19.34 | 2.14 | E05_A | 0.00-2.14 | 글자 |
| 07 | V1 | Y-E-J-I-N | 19.34 | 21.49 | 2.15 | E02_A | 2.86-5.00 | 글자 |
| 08 | V1 | And Yejin is her name-o | 21.49 | 23.63 | 2.14 | E05_A | 2.86-5.00 |  |
| 09 | V2 | There is a puppy, soft and white | 23.63 | 27.91 | 4.28 | E06_A | 0.00-4.28 | Pip 등장 |
| 10 | V2 | And Yejin is her name-o | 27.91 | 32.19 | 4.28 | E07_A | 0.00-4.28 |  |
| 11 | V2 | (clap)-E-J-I-N | 32.19 | 34.33 | 2.14 | E08_A | 0.00-2.14 | Y 자리 박수 아이콘 |
| 12 | V2 | (clap)-E-J-I-N | 34.33 | 36.47 | 2.14 | E09_A | 0.00-2.14 |  |
| 13 | V2 | (clap)-E-J-I-N | 36.47 | 38.61 | 2.14 | E08_A | 2.86-5.00 |  |
| 14 | V2 | And Yejin is her name-o | 38.61 | 40.75 | 2.14 | E09_A | 2.86-5.00 |  |
| 15 | V3 | There is a puppy, soft and white | 40.75 | 45.02 | 4.27 | E10_A | 0.00-4.27 | 장소 전환: 원형 와이프 |
| 16 | V3 | And Yejin is her name-o | 45.02 | 49.27 | 4.25 | E11_A | 0.00-4.25 |  |
| 17 | V3 | (clap)-(clap)-J-I-N | 49.27 | 51.40 | 2.13 | E12_A | 0.00-2.13 |  |
| 18 | V3 | (clap)-(clap)-J-I-N | 51.40 | 53.54 | 2.14 | E13_A | 0.00-2.14 |  |
| 19 | V3 | (clap)-(clap)-J-I-N | 53.54 | 55.67 | 2.13 | E12_A | 2.87-5.00 |  |
| 20 | V3 | And Yejin is her name-o | 55.67 | 57.81 | 2.14 | E13_A | 2.86-5.00 |  |
| 21 | Break | (instrumental) | 57.81 | 62.08 | 4.27 | E14_A | 0.00-4.27 | 무대 춤 |
| 22 | Break | (instrumental) | 62.08 | 66.33 | 4.25 | E11_B | 0.00-4.25 | 실로폰 |
| 23 | Break | (instrumental) | 66.33 | 70.58 | 4.25 | E15_A | 0.00-4.25 | 장소 전환: 흰 플래시 0.3초 |
| 24 | Break | (instrumental) | 70.58 | 74.85 | 4.27 | E19_A | 0.00-4.27 |  |
| 25 | V4 | There is a puppy, soft and white | 74.85 | 79.11 | 4.26 | E16_A | 0.00-4.26 |  |
| 26 | V4 | And Yejin is her name-o | 79.11 | 83.34 | 4.23 | E17_A | 0.00-4.23 |  |
| 27 | V4 | (clap)-(clap)-(clap)-I-N | 83.34 | 85.46 | 2.12 | E18_A | 0.00-2.12 |  |
| 28 | V4 | (clap)-(clap)-(clap)-I-N | 85.46 | 87.58 | 2.12 | E20_A | 0.00-2.12 |  |
| 29 | V4 | (clap)-(clap)-(clap)-I-N | 87.58 | 89.71 | 2.13 | E18_A | 2.87-5.00 |  |
| 30 | V4 | And Yejin is her name-o | 89.71 | 91.83 | 2.12 | E20_A | 2.88-5.00 |  |
| 31 | V5 | There is a puppy, soft and white | 91.83 | 96.07 | 4.24 | E24_A | 0.00-4.24 | 첨벙 효과음 |
| 32 | V5 | And Yejin is her name-o | 96.07 | 100.29 | 4.22 | E17_B | 0.00-4.22 |  |
| 33 | V5 | (clap)x4-N | 100.29 | 102.41 | 2.12 | E18_B | 0.00-2.12 |  |
| 34 | V5 | (clap)x4-N | 102.41 | 104.53 | 2.12 | E24_B | 0.00-2.12 |  |
| 35 | V5 | (clap)x4-N | 104.53 | 106.65 | 2.12 | E18_B | 2.88-5.00 |  |
| 36 | V5 | And Yejin is her name-o | 106.65 | 108.76 | 2.11 | E24_B | 2.89-5.00 |  |
| 37 | V6 | There is a puppy, soft and white | 108.76 | 112.99 | 4.23 | E21_A | 0.00-4.23 | 장소 전환: 원형 와이프 |
| 38 | V6 | And Yejin is her name-o | 112.99 | 117.21 | 4.22 | E22_A | 0.00-4.22 |  |
| 39 | V6 | (clap)x5 | 117.21 | 119.31 | 2.10 | E08_B | 0.00-2.10 | 글자 전부 박수 아이콘 |
| 40 | V6 | (clap)x5 | 119.31 | 121.43 | 2.12 | E09_B | 0.00-2.12 |  |
| 41 | V6 | (clap)x5 | 121.43 | 123.54 | 2.11 | E22_B | 0.00-2.11 |  |
| 42 | V6 | (clap)x5 | 123.54 | 125.65 | 2.11 | E07_B | 0.00-2.11 |  |
| 43 | V6 | And Yejin is her name-o | 125.65 | 127.77 | 2.12 | E04_B | 0.00-2.12 |  |
| 44 | Outro | Y-E-J-I-N! | 127.77 | 131.99 | 4.22 | E21_B | 0.00-4.22 | 글자 Y E J I N 다시 등장 |
| 45 | Outro | And Yejin is her name-o! (Woof!) | 131.99 | 136.21 | 4.22 | E02_B | 0.00-4.22 | 멍! 지점에 입 벌림 맞추기 |
| 46 | Outro | (tail) | 136.21 | 140.43 | 4.22 | E23_A | 0.00-4.22 | 작별 인사 |
| 47 | Outro | (tail) + 최종 화면 | 140.43 | 148.64 | 8.21 | E23_A | 4.22-10.00 | 5.78초 사용 후 마지막 프레임 정지 2.43초. 마지막 8초에 YouTube 최종 화면 요소 배치 |
**편집 메모**
- 재사용 구간(같은 클립의 앞부분·뒷부분)은 겹치지 않도록 이미 나눠 두었습니다(검증 완료).
- 박수 슬롯(11~13, 17~19, 27~29, 33~35, 39~42)은 음원의 박수 소리와 화면의 손 맞닿는 프레임을 맞춥니다. 어긋나면 0.9~1.1배 속도 조정을 허용합니다.
- 글자 그래픽: V1은 Y E J I N이 박자마다 하나씩, V2부터는 박수로 바뀐 글자 자리에 별 모양 박수 아이콘. 위치는 화면 위쪽 1/4.
- 출력: 1920×1080(720p 소스 업스케일), 24fps, H.264 + AAC, 148.64초.
