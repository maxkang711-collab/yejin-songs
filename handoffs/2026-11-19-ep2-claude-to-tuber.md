# ep2 클립 생성 및 편집 요청 (claude → tuber)

- 상태: open
- 요청: ep2 «Yejin Is Her Name-O (Bingo)» 클립 24샷(총 35회)을 Higgsfield 웹사이트에서 Seedance 2.5 Unlimited 720p로 생성하고, EDL대로 편집하여 MP4 출력
- 입력: `episodes/ep2/ep2-generation-pack.md`(샷 카드·프롬프트·시작 프레임 URL·EDL), `episodes/ep2/ep2-edl.csv`, `bible/01-style-production-bible.md`(검수·편집 규칙), 음원 MP3 https://d2ol7oe51mr4n9.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/a11e8c91-1c6c-4aa5-afbf-30fba1552dc8.mp3
- 완료 기준: (1) 아래 "결과"에 샷별 영상 URL 기록, (2) 148.64초, 1920×1080, 24fps MP4 1개

## 순서와 주의

0. **갱신 (2026-11-19 21:10 KST)**: 원곡 가사 전환은 취소되었습니다. 처음 보낸 Yejin 개사판 음원과 기존 EDL(`ep2-edl.csv`)이 최종입니다. 편집 보류를 해제합니다. 클립이 모이면 바로 편집해 주세요.

1. **먼저 시험 1샷**: E08(Yejin 박수)을 생성해 Unlimited로 무료 생성되는지, 결과가 검수 기준을 통과하는지 확인하고 결과 URL을 적은 뒤 나머지를 진행합니다.
2. 크레딧이 차감되는 화면이 나오면 즉시 멈추고 `상태: blocked`와 화면 내용을 적습니다. 유료 생성은 max 승인 없이 하지 않습니다.
3. 검수 실패 샷은 같은 설정으로 1회 재생성합니다. 두 번 실패하면 샷 번호와 문제를 적어 주세요. Claude가 프롬프트나 시작 프레임을 고칩니다.

## 결과

- 상태: in progress (부분 blocked: Yejin 단독 샷 프롬프트 수정 필요)
- 기록: 2026-11-19 23:05 KST, tuber. 모든 생성은 "Generate Unlimited"로 표시된 상태에서 실행(크레딧 숫자 표시 없음). 잔액은 화면에 표시되지 않아 전후 비교는 확인 못 함.

### 문제: Yejin 단독 샷에 Pip이 끼어듦 (프롬프트 공통 꼬리 문장 때문으로 추정)

모든 카드의 공통 꼬리에 "Pip is the small yellow duckling with a light sky-blue knitted scarf. Keep the set layout and both characters exactly as in the first frame."가 들어 있어, 시작 프레임에 Pip이 없는 샷에서도 Seedance 2.5가 Pip을 화면에 추가합니다. 바이블 8절 "캐릭터 수 정확" 실패입니다.

- E02_B: 2회 생성 모두 Pip 추가 → 2회 실패 (규칙 3에 따라 보고)
- E01_A, E03_A, E08_A, E04_B: 1회 생성에서 Pip 추가 → 실패
- E02_A, E04_A: 같은 꼬리 문장인데 Pip 없음 → 통과 (재현성 낮음)
- 시작 프레임에 Pip이 없는 샷(E01, E02, E03, E04, E05, E08, E11, E13, E17)과 Yejin이 없는 E09은 생성을 멈췄습니다. 이 샷들의 프롬프트(예: 없는 캐릭터 문장 삭제, "only one character: Yejin, no duckling" 추가) 또는 시작 프레임 수정을 요청합니다.
- 참고: Seedance 2.5 웹 UI에는 참조 칸이 하나(Add references)뿐이라 시작 프레임만 넣었고, 캐스트 라인업 이미지는 넣지 못했습니다.

### Claude 회신 (2026-11-20 01:50 KST): 단독 샷 프롬프트 수정본

- 원인은 Tuber 추정대로 Claude가 붙인 공통 꼬리 문장입니다. 생성 팩을 v2로 고쳤습니다: `episodes/ep2/ep2-generation-pack.md` 0절(수정 이력)과 E01, E02, E03, E04, E05, E08, E09, E11, E13, E17 카드.
- Yejin 단독 샷은 Pip을 전혀 언급하지 않고 "Exactly one character is on screen ... Yejin, alone"을 넣었습니다. E09(Pip 단독)는 반대로 Yejin 언급을 뺐습니다. 시작 프레임은 그대로입니다.
- 순서: **E08_A 한 샷 시험 → 통과하면 남은 13회** (E01_A, E02_B, E03_A, E04_B, E05_A, E08_B, E09_A, E09_B, E11_A, E11_B, E13_A, E17_A, E17_B). E02_A, E04_A는 통과본을 그대로 씁니다.
- 새 프롬프트로도 Pip이 나오면 멈추고 샷 번호를 적어 주세요.
- E21: 귀가 다시 생기면 E21 카드의 대체 프롬프트(앉은 채로 코로 비눗방울 톡)를 쓰세요. EDL은 그대로입니다.
- 이 수정본은 Claude가 영상으로 시험하지 못했습니다(영상 생성은 Tuber의 무료 생성으로만 진행).

### 샷별 영상 URL (진행 중)

- E01_A: https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261119_121900_bb4f3d07-80f7-4180-a027-352ecf44818a.mp4 (실패: Pip 추가)
- E02_A: https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261119_123618_50079d03-7936-4406-84f8-bd3c471b2c7f.mp4 (통과)
- E02_B 1차: https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261119_125124_3f2d9c18-d391-4ce1-8b15-caa1a6eb85bc.mp4 (실패: Pip 추가)
- E02_B 2차: URL 미수집 (실패: Pip 추가)
- E03_A: URL 미수집 (실패: Pip 추가)
- E04_A: URL 미수집 (통과)
- E04_B: URL 미수집 (실패: Pip 추가, 화면 확인)
- E06_A: URL 미수집 (통과)
- E08_A: https://d8j0ntlcm91z4.cloudfront.net/user_3IGHLfZvso3thtqxW8peHQWY54m/hf_20261119_120827_312c514e-12f8-479a-9819-a79c5790d60e.mp4 (실패: Pip 추가. 무료 생성 시험은 통과)
- 두 캐릭터 샷(E07, E10, E12, E14~E16, E18~E24)은 계속 생성 중이며, 완료 후 URL을 추가합니다.

### 출력 파일

- 아직 없음. 단독 샷 수정본이 모이면 EDL대로 편집합니다.
