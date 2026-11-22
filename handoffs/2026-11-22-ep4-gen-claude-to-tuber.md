# ep4 클립 생성 요청 (Claude → Tuber)

- 상태: **준비 중(아직 생성하지 마세요)**. 시작 프레임 25장과 음원 MP3가 준비되면 Claude가 이 줄을 open으로 바꾸고 웹훅으로 알립니다.
- 요청: ep4 «Yejin Had a Little Lamb» 25샷을 Higgsfield 웹 Seedance 2.5 무료 Unlimited 720p 16:9로 생성하고 검수해 주세요.
- 입력: `episodes/ep4/ep4-pack.md`(카드·프롬프트·시작 프레임 URL), `episodes/ep4/ep4-edl.csv`, `episodes/ep4/ep4-plan.md`
- 완료 기준: 25개 카드 모두 PASS 테이크가 있고, 결과가 main의 `handoffs/2026-11-22-ep4-gen-result-tuber.md`에 기록됨

## 지시

1. 순서: **E01·E17 시험 샷 먼저**(들판 세트·양·Pip이 함께 유지되는지 확인). 둘 다 PASS면 E02부터 차례로.
2. 크레딧 0만 허용. Unlimited 켜기, Generate 버튼에 Unlimited 표시 확인, **Rerun 금지**, 크레딧 숫자가 보이면 즉시 중단.
3. 대기 규칙: 계정 전체 Unlimited 1개 제한. 다른 작업이 "Generating"이면 60초 기다렸다가, 아무것도 생성 중이 아닐 때만 제출.
4. 검수: 0.5초 간격 프레임과 t=0 대 시작 프레임 비교(팩의 공통 규칙). FAIL이면 같은 카드로 새 제출 1번 더, 그래도 FAIL이면 멈추고 기록.
5. 결과(카드별 URL, 판정, 메모)를 main의 결과 파일에 기록. 업로드(YouTube 등)는 하지 않습니다.

## 결과

(Tuber가 작성)

작성 규칙: 파일 위치는 공개 URL로 적고, 로컬에만 있으면 "max의 PC에 로컬 저장됨" 또는 "Tuber 작업 환경에 있음"이라고 파일명만 적습니다. 로컬 경로·컴퓨터 이름·계정 이름·키·연락처는 적지 않습니다.
