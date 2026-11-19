# Yejin Songs 제작 허브

Yejin Songs(유아용 YouTube 채널) 제작에 참여하는 봇들이 작업을 주고받는 공용 저장소입니다.
봇끼리 직접 연결되는 통로가 없으므로, 모든 전달은 이 저장소의 파일로 합니다.

## 참여 봇

| 이름 | 위치 | 담당 |
|---|---|---|
| claude | Claude (프로젝트 "tuber") | 음원(Suno), 캐릭터·클립 생성(Higgsfield), 편집 결정 목록(EDL) |
| tuber | Grok | 최종 편집, 1080p MP4 출력 |
| max | 사람 | 승인, 업로드, 봇 사이 전달 |

## 폴더 구조

```
README.md            이 문서(규칙)
STATUS.md            에피소드별 단계와 현재 담당
episodes/<ep>/       에피소드 산출물(EDL, 클립 목록, 메모)
handoffs/            봇 사이 전달 문서
```

## 전달(handoff) 규칙

1. 일을 넘길 때 `handoffs/<날짜>-<에피소드>-<보내는봇>-to-<받는봇>.md` 파일을 만듭니다.
   예: `handoffs/2026-11-19-ep1-claude-to-tuber.md` (날짜는 KST, YYYY-MM-DD)
2. 같은 날 같은 방향으로 두 번째 전달이 있으면 끝에 `-2`, `-3`을 붙입니다.
3. 전달 문서 맨 위에는 다음 항목을 둡니다.
   - `상태:` open / accepted / done / blocked
   - `요청:` 받는 봇이 할 일 한 줄
   - `입력:` 참고할 파일 경로나 URL
   - `완료 기준:` 무엇이 나오면 끝인지
4. 받는 봇은 일을 시작하면 `상태: accepted`, 끝나면 `상태: done`으로 바꾸고, 결과(링크·파일·메모)를 문서 아래 "결과" 절에 적습니다. 막히면 `상태: blocked`와 이유를 적습니다.
5. 회신이 필요하면 반대 방향의 새 전달 문서를 만듭니다(예: `...-tuber-to-claude.md`).
6. 전달을 만들거나 끝낼 때마다 `STATUS.md`의 해당 에피소드 행을 갱신합니다.
7. 저장소에 쓰기 권한이 없는 봇은 결과를 max에게 주고, max(또는 Claude)가 대신 커밋합니다.

## Tuber(Grok)가 읽는 법

이 저장소는 공개 저장소이므로 로그인 없이 아래 주소로 읽을 수 있습니다.

- 현황: https://raw.githubusercontent.com/maxkang711-collab/yejin-songs/main/STATUS.md
- 규칙: https://raw.githubusercontent.com/maxkang711-collab/yejin-songs/main/README.md
- 전달 목록: https://github.com/maxkang711-collab/yejin-songs/tree/main/handoffs
- 개별 파일: `https://raw.githubusercontent.com/maxkang711-collab/yejin-songs/main/<경로>`

공개 저장소이므로 누구나 읽을 수 있습니다. 아래 금지 사항을 반드시 지킵니다.

## 금지 사항

- API 키, 토큰, 비밀번호, 쿠키 등 비밀 정보를 커밋하지 않습니다.
- 개인 이메일 주소나 연락처를 적지 않습니다.
- 대용량 영상·음원 파일은 커밋하지 않고, 다운로드 URL이나 보관 위치만 적습니다.
