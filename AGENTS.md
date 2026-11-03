# shortform-guide — 에이전트 진입점

AI마스터스쿨(방화차량기지 임직원 대상 AI 활용 강의) 수강생이 **Gemini 노트북 채팅 하나로 숏폼 한 편을 만드는 과정**을 보고 따라 하는 반응형 안내 페이지다.
GitHub Pages로 공개한다: https://toddoward.github.io/shortform-guide/
강의 자료의 원본은 비공개 리포 `ai-master-school`에 있다. 이 리포는 수강생에게 보이는 공개본이다.

## 0. 콜드스타트

1. 이 파일
2. [`docs/WORKLOG.md`](docs/WORKLOG.md) 최신 3건
3. 고칠 대상: 페이지 `index.html` · 노트북 자료 `notebook/`

## 1. 무엇이 어디에 있나

| 내용 | 원본 | 이 리포 |
|---|---|---|
| 노트북 자료(안내서) | `ai-master-school/materials/04_노트북소스/AI마스터스쿨_숏폼안내서.md` | `notebook/guide.md` (복사본) |
| 노트북 요청 사항 | `ai-master-school/materials/04_노트북소스/노트북_요청사항.txt` | `notebook/instructions.txt` (복사본) |
| 안내 페이지 | 여기 `index.html` (한 파일 — CSS · JS · 화면 그림이 모두 안에) | — |

노트북 자료를 고칠 때는 **원본을 먼저 고치고** 복사한다: `cp` 두 줄(§3). 페이지의 버튼 순서 · 이름은 `notebook/guide.md`와 같아야 한다.

## 2. 하드 룰

- **공개 리포다.** 수강생 이름 · 이메일 · 계정 사진 · 내부 자료를 넣지 않는다. 화면 그림은 실제 화면을 보고 **직접 그린 그림**(HTML · SVG)으로, 계정 정보 자리는 비워 둔다
- 수강생은 비개발 직군이다. 기술 용어를 쓰지 않는다(프롬프트 → 지시문, 소스 → 자료). **버튼 이름은 화면 글자 그대로** 「」 안에 쓴다
- 도구 사양(메뉴 이름 · 한도)은 실제 화면이나 공식 문서로 확인한 것만 쓰고 확인일을 적는다
- 만들기 안내는 **컴퓨터(Chrome) 기준**. 휴대폰은 보기만 지원한다(사용자 결정 2026-11-03)
- 모션은 `~/dev/visual-design/skills/slide-design/motion.md` §0 값을 그대로 쓴다. `prefers-reduced-motion`이면 끝 상태로 정적

## 3. 검증 명령

```bash
# 원본과 복사본이 같은가
cmp notebook/guide.md "../ai-master-school/materials/04_노트북소스/AI마스터스쿨_숏폼안내서.md"
cmp notebook/instructions.txt "../ai-master-school/materials/04_노트북소스/노트북_요청사항.txt"
# 페이지 확인: 브라우저로 index.html 열기 — 가로 1366 · 1920, 세로 390(휴대폰)에서 넘침 없는지
```

## 4. 디렉터리

| 위치 | 무엇 |
|---|---|
| `index.html` | 안내 페이지 전체 |
| `notebook/` | 노트북에 넣을 글 두 개 (페이지의 「복사」 버튼이 이 파일을 읽는다) |
| `assets/` | 예시 영상 · 포스터 등 그림 파일 |
| `docs/WORKLOG.md` | 작업 기록 — 맨 위에 최신 |
