# ep2 클립 생성 및 편집 요청 (claude → tuber)

- 상태: open
- 요청: ep2 «Yejin Is Her Name-O (Bingo)» 클립 24샷(총 35회)을 Higgsfield 웹사이트에서 Seedance 2.5 Unlimited 720p로 생성하고, EDL대로 편집하여 MP4 출력
- 입력: `episodes/ep2/ep2-generation-pack.md`(샷 카드·프롬프트·시작 프레임 URL·EDL), `episodes/ep2/ep2-edl.csv`, `bible/01-style-production-bible.md`(검수·편집 규칙), 음원 MP3(max가 Suno 곡 `99fa56ab-4102-4461-a88b-63c334127bd0`에서 내려받아 전달)
- 완료 기준: (1) 아래 "결과"에 샷별 영상 URL 기록, (2) 148.64초, 1920×1080, 24fps MP4 1개

## 순서와 주의

1. **먼저 시험 1샷**: E08(Yejin 박수)을 생성해 Unlimited로 무료 생성되는지, 결과가 검수 기준을 통과하는지 확인하고 결과 URL을 적은 뒤 나머지를 진행합니다.
2. 크레딧이 차감되는 화면이 나오면 즉시 멈추고 `상태: blocked`와 화면 내용을 적습니다. 유료 생성은 max 승인 없이 하지 않습니다.
3. 검수 실패 샷은 같은 설정으로 1회 재생성합니다. 두 번 실패하면 샷 번호와 문제를 적어 주세요. Claude가 프롬프트나 시작 프레임을 고칩니다.

## 결과

(tuber가 작성: 샷별 영상 URL `E01_A: ...`, 검수 메모, 출력 파일 위치)
