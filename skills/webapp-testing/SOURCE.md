# 출처 · 검증 기록 — webapp-testing

| 항목 | 내용 |
|---|---|
| 원출처 | [https://github.com/anthropics/skills](https://github.com/anthropics/skills) (**Anthropic 공식**) |
| 원본 경로 | `skills/webapp-testing/SKILL.md` (**원문 전체**) |
| 원본 커밋 | `e4bb5d960d87126ff3b3a8af1a104b7db67560ba` (2026-11-16) |
| 라이선스 | **Apache-2.0** — Copyright 2026 Anthropic, PBC — [`LICENSES/webapp-testing-LICENSE.txt`](../../LICENSES/webapp-testing-LICENSE.txt) (원본 폴더의 `LICENSE.txt` 11,345B와 같습니다) |
| 스타 | ⭐ 197,710 (2026-11-20 `gh api` 확인) |
| 저장(검증)일 | **2026-11-20** (창현 님 승인: 텔레그램 1664번 "딱히 이상없으면 기록해") |

## 원문 보존

`SKILL.md` **95줄 3,913B를 한 글자도 수정하지 않고** 올렸습니다(md5 `b02025a3df7ff4a6ac7e765cd1d6d54c` 대조 일치). 이 폴더에는 `SKILL.md`와 이 `SOURCE.md` 두 파일만 있습니다.

## 이 저장소에 넣은 것 / 넣지 않은 것

| 원본 파일 | 등록 | 비고 |
|---|---|---|
| `skills/webapp-testing/SKILL.md` (3,913B) | ✅ | 방법론·판단 트리·셀렉터 탐색 패턴·베스트 프랙티스 |
| `scripts/with_server.py` (105줄) | ❌ | **열람만** 함 — 서버 명령을 `shell=True`로 실행하는 런처라 실행 코드는 싣지 않았습니다 |
| `examples/console_logging.py` · `element_discovery.py` · `static_html_automation.py` (105줄) | ❌ | 열람만 함 — 예제 경로가 `/mnt/user-data/outputs/` 같은 샌드박스 전제 |
| `LICENSE.txt` (11,345B) | ✅ | `LICENSES/webapp-testing-LICENSE.txt`로 전문 보존 |

## 검증 범위 (2026-11-20 · 1차 안전 확인)

- `SKILL.md` 본문 **전수 열람**. 문서 자체는 지침·예제 코드뿐이고, 접속 대상은 `http://localhost:5173` 같은 **로컬 서버**입니다.
- `scripts/with_server.py` **전수 열람**(1회): `subprocess.Popen(server["cmd"], shell=True)`로 넘겨받은 문자열을 셸로 실행하고, `socket.create_connection(('localhost', port))`로 포트가 열릴 때까지 기다린 뒤 `subprocess.run(args.command)`로 자동화 스크립트를 돌리고, 종료 시 서버 프로세스를 `terminate()`/`kill()` 합니다. **파일 쓰기·외부 URL 호출·데이터 전송 0건** — `urllib`·`requests`·원격 호스트 문자열이 없습니다.
- `examples/` 3종 **전수 열람**: `playwright.sync_api`로 Chromium을 headless 실행, `localhost` 접속, 스크린샷·콘솔 로그를 로컬 경로(`/tmp`, `/mnt/user-data/outputs`)에 저장하는 예제입니다.
- → **검사 범위 내 의심 동작 0건**입니다. **`anthropics/skills` 저장소 전체(448개 파일) 감사나 실제 실행 검증을 마쳤다는 뜻이 아닙니다.** Python Playwright 설치는 이 환경에서 시험하지 않았습니다.

## 무슨 스킬인가 — 서버를 띄우고 화면을 직접 본다

| 단계 | 내용 |
|---|---|
| 판단 | 정적 HTML이면 파일을 읽어 셀렉터를 잡고, 동적 웹앱이면 서버를 띄운다 |
| 서버 | `python scripts/with_server.py --server "npm run dev" --port 5173 -- python your_automation.py` (서버 여러 개 동시 지원) |
| 자동화 | `sync_playwright()` + **headless Chromium**, `wait_for_load_state('networkidle')` 뒤에 DOM·스크린샷 확인 |
| 원칙 | 스크립트는 `--help`부터 실행하고 소스는 읽지 않는다(컨텍스트 절약), 끝나면 브라우저를 닫는다 |

## 이 저장소에서 쓸 때

- `with_server.py`와 `examples/`는 여기에 없으므로, 실제로 돌릴 때는 원출처 경로에서 받아 쓰세요. 이 폴더만 복사하면 스킬 설명서만 설치됩니다.
- 소늘이·페이스히어로 같은 **로컬 웹앱**의 화면·콘솔 오류 확인에 맞는 스킬입니다. 아이폰 사파리 실기기 확인(Safe Area·핀치 확대·홈 화면 앱)은 이 스킬로 대체되지 않습니다.

## ⚠️ 주의사항

⚠️ 주의사항: `with_server.py`가 `--server` 문자열을 `shell=True`로 실행하므로 **직접 작성한 신뢰하는 프로젝트에서만** 사용하고, 남이 준 명령 문자열을 그대로 넣지 마세요. Python Playwright(`pip install playwright` + `playwright install chromium`)가 필요하며, 이 스킬은 로컬 브라우저 자동화라 아이폰·애플워치 **실기기 테스트를 대체할 수 없습니다**. 1차 안전 확인(읽은 범위 내 의심 동작 0건)만 했고 전체 코드 감사·실행 검증은 하지 않았습니다.
