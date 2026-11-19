# 출처 · 검증 기록 — self-improving-agent

| 항목 | 내용 |
|---|---|
| 원출처 | [https://github.com/alirezarezvani/claude-skills](https://github.com/alirezarezvani/claude-skills) |
| 원본 경로 | `engineering-team/self-improving-agent/skills/self-improving-agent/SKILL.md` (**원문 전체**) |
| 원본 커밋 | `f8593c4941210a621a6629ce1da9e07897976d5f` (2026-11-17) |
| 버전 | 플러그인 `settings.json` 기준 **1.0.0** |
| 라이선스 | **MIT** — Copyright (c) 2025 Alireza Rezvani — [`LICENSES/self-improving-agent-LICENSE.txt`](../../LICENSES/self-improving-agent-LICENSE.txt) (원본 폴더에도 같은 `LICENSE` 1,069B가 있습니다) |
| 스타 | ⭐ 30,078 (2026-11-19 확인) |
| 저장(검증)일 | **2026-11-19** (창현 님 승인: 텔레그램 1308번 · **발췌** 등록) |

## 원문 보존

`SKILL.md` **163줄 7,222B를 한 글자도 수정하지 않고** 올렸습니다(md5 `2af00db4c1c01e42285f42f136bcb41b` 대조 일치). 이 폴더에는 `SKILL.md`와 이 `SOURCE.md` 두 파일만 있습니다.

## 이 저장소에 넣은 것 / 넣지 않은 것

| 원본 파일 | 등록 | 비고 |
|---|---|---|
| `skills/self-improving-agent/SKILL.md` (7,222B) | ✅ | 큐레이션 워크플로·메모리 구조·승격 절차 |
| `hooks/error-capture.sh` (4,072B) · `hooks/skill_router.py` (4,541B) · `hooks/hooks.json` · `hooks/skill_routes.json` | ❌ | **설치하면 자동 실행되는 훅** — 열람만 하고 등록하지 않음 |
| `settings.json` (852B) | ❌ | 위 훅을 플러그인 설치 시 자동 등록하는 선언 |
| `agents/memory-analyst.md` · `agents/skill-extractor.md` | ❌ | 서브에이전트 정의 |
| `reference/` 3개 · `templates/` 2개 · `README.md` · `CLAUDE.md` · `.claude-plugin/` | ❌ | 보조 문서·매니페스트 |

## 검증 범위 (2026-11-19 · 1차 안전 확인)

- `SKILL.md` 본문 **전수 열람**. 스크립트·외부 호출은 이 파일 안에 **0건**(문서 링크만 있음).
- `hooks/` 4개 파일도 **1차 열람**했습니다(등록은 안 함):
  - `error-capture.sh` — `PostToolUse(Bash)`에서 표준입력으로 받은 명령 출력에서 오류 패턴 30여 개를 찾아 **`additionalContext` 한 줄(약 30~40토큰)만 주입**합니다. 파일을 쓰거나 네트워크로 보내지 않습니다(`http`·`curl`·`urllib`·`requests` 검색 결과 주석 속 문서 URL 1건뿐).
  - `skill_router.py` — `UserPromptSubmit`에서 프롬프트를 정규식으로 매칭해 **스킬 이름 한 줄**을 덧붙입니다. 차단하지 않고, 모델 호출도 하지 않습니다.
- → **검사 범위 내 의심 동작 0건**입니다. **모노레포 전체(5,665개 파일 · `SKILL.md` 495개 · 플러그인 121개) 보안 감사 보증은 아닙니다.**
- **문서와 실제 스크립트의 차이 1건**: `SKILL.md`의 "Hooks — error-capture" 설명은 "auto-memory에 구조화 항목을 **추가한다**"고 적혀 있지만, 실제 `error-capture.sh`는 메모리에 쓰지 않고 **모델에게 리마인더 한 줄을 주입**하는 데서 끝납니다. 어느 쪽이든 자동 기록은 아니므로, "클로드가 스스로 학습해 쌓아 준다"는 기대와는 다릅니다.

## 무슨 아이디어인가 — 캡처는 클로드가, 큐레이션은 사람이

| 층 | 파일 | 쓰는 주체 | 로드 |
|---|---|---|---|
| 프로젝트 규칙 | `./CLAUDE.md` | 사람(+`/si:promote`) | 매 세션 전체 |
| 자동 메모리 | `~/.claude/projects/<path>/memory/MEMORY.md` | 클로드 자동(v2.1.32+) | **첫 200줄만** |
| 주제 메모 | 같은 폴더 `*.md` | 클로드(넘칠 때) | 필요할 때 |
| 범위 규칙 | `.claude/rules/*.md` | 사람(+`/si:promote`) | 해당 파일을 열 때 |

- **승격 절차**: 클로드가 패턴을 발견 → `MEMORY.md` → 2~3회 반복되면 `/si:memory-review`가 승격 후보로 표시 → 사람이 승인 → `/si:promote`로 `CLAUDE.md` 또는 `.claude/rules/`로 이동 → `MEMORY.md` 항목 삭제(200줄 한도 확보).
- 핵심 구분: **`MEMORY.md`는 배경 지식("이 프로젝트는 pnpm을 쓴다")**, **`CLAUDE.md`는 강제 지시("npm 대신 pnpm을 써라")**.

## 환경 전제 (그대로 확인됨)

- **클로드 코드 v2.1.32+**의 자동 메모리 기능이 있어야 의미가 있습니다. 원문은 설치 예시를 플러그인 마켓플레이스·OpenClaw·Codex CLI로 안내하고, 인용 경로는 `${CLAUDE_PLUGIN_ROOT}` 기준입니다.
- 플랫폼 표: **Claude Code 전체 지원**, OpenClaw·Codex CLI는 적응형, GitHub Copilot은 수동 승격만.
- 윈도우(PowerShell)에서의 동작은 원문이 별도로 보증하지 않습니다 — 경로·훅 실행은 그 환경에서 한 번 확인이 필요합니다.

## ⚠️ 주의사항

⚠️ 주의사항: 윈도우 클로드 코드(v2.1.32+) 자동 메모리 환경을 전제로 하며, 410개+ 모노레포 전체 클론 금지 및 hooks/·settings.json 등 보조 스크립트 실행 전 코드 추가 확인이 필요하므로 당장은 SKILL.md 프롬프트·워크플로 발췌만 참고하세요.
