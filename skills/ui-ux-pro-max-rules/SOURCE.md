# 출처 · 검증 기록 — ui-ux-pro-max-rules (발췌)

| 항목 | 내용 |
|---|---|
| 원출처 | [https://github.com/nextlevelbuilder/ui-ux-pro-max-skill](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill) |
| 원본 경로 | `.claude/skills/ui-ux-pro-max/references/pro-rules.md` (원문 등록), `.claude/skills/ui-ux-pro-max/SKILL.md`·`data/*.csv` (수치 기준표 근거) |
| 버전 | `skill.json` **v2.15.0** |
| 원본 커밋 | `e59ff376a41f7ca47b7541ad5c116495cbade3ee` (2026-11-16) |
| 라이선스 | **MIT** — [`LICENSES/ui-ux-pro-max-LICENSE.txt`](../../LICENSES/ui-ux-pro-max-LICENSE.txt) (Copyright (c) 2024 Next Level Builder) |
| 스타 | ⭐ 150,890 (2026-11-18 확인) |
| 저장(검증)일 | **2026-11-18** |

## 이 폴더가 발췌인 이유 — **전체 설치 비권장**

원본은 저장소 728파일 21.7MiB, `.claude/skills/`만 7개 스킬 **10,211,013B**이고 그중 `ui-ux-pro-max` 혼자 **81파일 3,825,768B**입니다(큰 파일: `data/google-fonts.csv` 747KB, `data/phosphor-icons-upstream.json` 824KB, `data/google-font-licenses.json` 433KB, `SKILL.md` 18,640B).

- 원본 `SKILL.md`는 `scripts/search.py`(데이터 검색) 호출을 전제로 쓰여 있어, 스크립트·데이터 없이 그 파일만 올리면 동작하지 않는 지시가 됩니다. 그래서 `SKILL.md`는 **싣지 않고**, 자립적으로 읽히는 `references/pro-rules.md`만 원문 등록했습니다.
- 실전 가치가 확인된 것은 **수치 기준과 Pre-Delivery 체크리스트**입니다. 스타일·폰트·색 추천이 필요하면 원출처를 직접 클론해 `scripts/search.py`를 돌리는 편이 낫습니다(로컬 실행, 비용 0).
- 알려진 결함: 제작사도 인정한 **중복 폴더 드리프트** 이력이 있습니다 — `cli/scripts/sync-assets.mjs` 26~40행 주석 원문: `.claude/skills/ui-ux-pro-max/{data,scripts}`가 `src/ui-ux-pro-max/{data,scripts}`의 *"second, independent copy"*이고 *"Nothing previously checked it against src/, so it silently drifted (missing stack CSVs, stale content in several data files)"*.

## 원문 보존

- `pro-rules.md` (10,909B) — 원출처 `references/pro-rules.md`를 **한 글자도 수정하지 않고** 올렸습니다(md5 대조 일치).
- `criteria.md` — **원문이 아닙니다.** 편집 정리본이며, 인용문과 출처 행 번호를 함께 적었습니다. 원문 인용은 그대로 두었습니다.
- `SKILL.md` (이 폴더의 것) — 이 저장소용으로 새로 쓴 안내문(원출처 `SKILL.md`와 다른 파일입니다).

## 검증 범위 (2026-11-18 · 1차 안전 확인)

- `scripts/` Python 6종(`core.py`·`design_system.py`·`preview.py`·`reasoning_contract.py`·`search.py`·`validate_data.py`)의 import를 전수 확인 — `re, pathlib, json, sys, os, csv, math, io, hashlib, difflib, statistics, html, argparse, datetime, tempfile, urllib.parse`만 사용, **표준 라이브러리 외부 패키지 0**.
- 실행 시 **네트워크 요청 0**: http 요청 코드 없음. 유일한 외부 참조는 `preview.py`가 *생성하는* 미리보기 HTML 안의 Google Fonts `<link>`(195~196행)이며, 그 HTML을 브라우저로 열 때만 나갑니다.
- 기본 실행은 파일 쓰기 없음. `--persist`/`--preview`일 때만 `design-system/<slug>/`에 씁니다.
- → **검사 범위 내 의심 동작 0건**입니다. **전체 저장소 보안 감사 보증은 아닙니다** — 설치 CLI(`npx ui-ux-pro-max-cli init`)는 GitHub release를 받으러 네트워크를 쓰므로, 설치가 필요하면 `--offline`을 쓰세요.

## 실전 실측 (2026-11-18)

시험 기록: `tmp/2026-11-18-skill-tests/REPORT.md`, 증거 `tmp/2026-11-18-skill-tests/evidence/checklist_review.md`

- PaceHero v22.1(`style.css` 53,647B·1,048줄, `index.html` 17,105B) 대조로 **결함 6건 판정**: 터치 타깃 미달 4건, 12px 미만 본문 글자 71/151개(47.0%), 텍스트 대비 3.38~3.97(4.5:1 미달), `user-scalable=no` 안티패턴. 통과 4건(safe-area·reduced-motion·누름 피드백·disabled).
- **주의**: 위 6건은 에이전트가 CSS를 읽고 계산한 것이고, 스킬은 기준값과 목록을 제공했습니다.
- 값이 있었던 지점: "웹이니 44×44 미달 = 결함"으로 볼 뻔한 것을, 스킬이 *"웹 기준은 WCAG 24px(+간격), 44pt는 iOS·48dp는 안드로이드"*로 구분해 줘서 판정을 **"WCAG 통과, 플랫폼 권장 미달"**로 바로잡았습니다.
