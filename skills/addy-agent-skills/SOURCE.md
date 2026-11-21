# 출처 · 검증 기록 — Addy Osmani Agent Skills (26종 스킬팩)

| 항목 | 내용 |
|---|---|
| 원출처 | [https://github.com/addyosmani/agent-skills](https://github.com/addyosmani/agent-skills) (⭐ 119,410 · 2026-11-21 GitHub API 실측) |
| 원본 경로 | `skills/<스킬명>/SKILL.md` 26개 전부 + `references/*.md` 7개 + 각 스킬의 `references/`·첨부 문서 6개 |
| 원본 커밋 | `8c99fa36d90068c82d547f7c12a9d67a3e95f4ee` (2026-11-18, 플러그인 매니페스트 0.6.17) |
| 라이선스 | **MIT** — [`LICENSES/addy-agent-skills-LICENSE.txt`](../../LICENSES/addy-agent-skills-LICENSE.txt) (Copyright (c) 2025 Addy Osmani) |
| 저장(검증)일 | **2026-11-21** |

## 수록 범위 — 26종 전부

저장소 `skills/` 아래 **26개 스킬의 `SKILL.md`를 하나도 빼지 않고** 평평하게 옮겼습니다(원래 경로 `skills/<스킬명>/SKILL.md` → 이 저장소 `skills/addy-agent-skills/<스킬명>/SKILL.md`). 각 스킬의 한 줄 설명은 [`INDEX.md`](INDEX.md)에 정리했습니다.

- 26종 = 수명주기 스킬 25종 + 메타 스킬 1종(`using-agent-skills`)
- 스킬이 `../../references/<파일>.md`로 참조하는 공용 문서 7개를 `references/`에 그대로 넣었습니다(accessibility-checklist · definition-of-done · observability-checklist · orchestration-patterns · performance-checklist · security-checklist · testing-patterns).
- 스킬 자체 `references/`·첨부 문서 6개도 함께 넣었습니다 — `constraint-driven-development/references/floor-guard.md`, `performance-optimization/references/optimization-patterns.md`, `security-and-hardening/references/hardening-patterns.md`, `idea-refine/{frameworks,refinement-criteria,examples}.md`.

## 넣지 않은 것 (실행 코드·도구 모음)

- `hooks/` 9개 파일(셸 스크립트 `sdd-cache-*.sh`, `session-start*.sh`, `simplify-ignore*.sh` 등) — **자동 적용 금지**, 아래 주의 참고
- `scripts/`(quality-gate·secret-scan·validator 등 node 스크립트), `commands/`(슬래시 커맨드 toml 10개), `agents/`, `evals/`, `docs/`, 플러그인 매니페스트(`plugin.json`, `.claude-plugin/`, `.agents/`, `.codex-plugin/`)
- 저장소 루트 `README.md`(배지·설치 안내·스폰서 링크 포함) — 이 저장소의 [`INDEX.md`](INDEX.md)로 대체

## 원문 보존 확인

옮긴 39개 마크다운 파일을 원본과 `diff -r`로 대조해 **차이 0건**(빠진 것은 위에서 제외한 실행 코드 폴더뿐)입니다. 파일 내용은 한 글자도 고치지 않았습니다.

## 경로가 바뀐 부분

원문의 상대 링크는 그대로 두었기 때문에 다음 두 종류는 이 저장소에서 그대로 열리지 않습니다.

| 원문 링크 | 원문 위치 | 이 저장소에서의 실제 위치 |
|---|---|---|
| `../../references/<파일>.md` | `skills/<스킬명>/` 기준 | `skills/addy-agent-skills/references/<파일>.md` |
| `scripts/<파일>` | 각 스킬 폴더 안 | 수록하지 않음(원출처에서 받아야 함) |

## 검증 범위 (2026-11-21 · 1차 안전 확인)

- 26개 `SKILL.md`와 참조 문서 13개 전수에서 **네트워크 요청 명령(curl·wget)·난독화·파일 삭제·자격증명 수집 0건**을 확인했습니다. 본문에 나오는 URL은 npm·pnpm·yarn·react.dev·W3C·OWASP·Chrome 문서 같은 **문서 인용**뿐입니다.
- `hooks/`·`scripts/`는 열람만 하고 수록·실행하지 않았습니다.
- → **검사 범위 내 의심 동작 0건**(1차 안전 확인). 저장소 전체(약 2MB, `evals/`·`docs/` 포함) 감사나 실전 성능 검증은 하지 않았습니다.

## 사용 시 주의

- **`hooks/` 셸 스크립트는 자동 적용하지 마세요.** 세션 시작·파일 저장 시점에 도는 훅이 포함되어 있어, 별도 코드 검토 전에 설치하면 원치 않는 동작이 붙을 수 있습니다. 지금은 `SKILL.md` 프롬프트만 복사해 쓰는 방식이 안전합니다.
- **단일 스킬 `npx` 설치 시 `references/`가 빠지는 보고가 있었습니다** — 이슈 [#361 "npx packs only skills/"](https://github.com/addyosmani/agent-skills/issues/361)(2026-07-08 접수, 2026-08-03 `completed`로 종료). 예: `planning-and-task-breakdown`이 `references/definition-of-done.md`를 참조하는데 npx 설치본에는 그 폴더가 없었습니다. 설치 후 `references/`가 함께 받아졌는지 확인하고, 빠졌으면 이 저장소의 `skills/addy-agent-skills/references/`를 복사해 넣으세요.
- **리팩토링 계열(`code-simplification` 등)은 테스트로 동작 보존을 확인해야 합니다.** 스킬 본문도 그렇게 지시하지만, 테스트가 없는 프로젝트에서는 먼저 테스트를 만들거나 변경 범위를 좁히는 편이 안전합니다.
- 스킬끼리 서로를 호출하도록 설계된 부분이 있습니다(`orchestration-patterns.md`). 한 세션에 여러 스킬을 한꺼번에 붙이면 지시가 충돌할 수 있으니, 작업 단위로 골라 쓰세요.
- **실전 성능은 미검증입니다.** 26종 중 이 환경에서 실제 작업에 적용해 본 스킬은 없습니다.
