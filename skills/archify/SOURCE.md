# 출처 · 검증 기록 — Archify

| 항목 | 내용 |
|---|---|
| 원출처 | [https://github.com/tt-a1i/archify](https://github.com/tt-a1i/archify) (⭐ 98,359 · 2026-11-21 GitHub API 실측) |
| 원본 경로 | `archify/SKILL.md` (**원문 전체** 137줄 18,877B) |
| 원본 커밋 | `8509a3d63e763b4d454ea9aafa1f939545fcb1ea` (2026-11-21) |
| 스킬 버전 | `3.2` (frontmatter `metadata.version`, 저장소 `archify/package.json` 3.2.0) |
| 라이선스 | **Apache-2.0** — [`LICENSES/archify-LICENSE.txt`](../../LICENSES/archify-LICENSE.txt), NOTICE 전문 [`LICENSES/archify-NOTICE.txt`](../../LICENSES/archify-NOTICE.txt), 과거 MIT 허여분 [`LICENSES/archify-LICENSE-MIT.txt`](../../LICENSES/archify-LICENSE-MIT.txt) |
| 저작자 표기 | **Copyright (c) 2026 tt-a1i (Archify) · Copyright (c) 2025 Cocoon AI** — `Cocoon-AI/architecture-diagram-generator`에서 출발(NOTICE 기재). Apache-2.0 §4(d)에 따라 NOTICE를 함께 두었습니다. |
| 저장(검증)일 | **2026-11-21** |

## 원문 보존

`archify/SKILL.md` 137줄을 **한 글자도 수정하지 않고** 올렸습니다. md5 `5603c915442218e3592ce45021894e1a`(원본과 대조 일치). 이 폴더에는 `SKILL.md`와 이 `SOURCE.md` 두 파일만 있습니다.

## 어떤 스킬인지 (같은 저장소의 다른 스킬과 구분)

- 수록한 것은 **제품용 스킬 `archify`**(frontmatter `name: archify`, 137줄)입니다. 아이디어·계획·코드를 `architecture`·`workflow`·`sequence`·`dataflow`·`lifecycle`·`erd`·`class`·`tree`·`timeline`·`waterfall` 10종의 인터랙티브 HTML 다이어그램(또는 한 장짜리 설명 페이지 `explainer`)으로 만듭니다.
- 같은 저장소의 `.agents/skills/archify-review/SKILL.md`(22줄, `metadata.internal: true`)는 **저장소 유지보수용 이슈·PR 리뷰 스킬**로 전혀 다른 물건입니다. 수록 대상이 아닙니다(`archify-tuning`·`simplify-codebase`·`test-value`도 동일하게 제외).
- 한국어 안내는 저장소의 `README_KO.md`에 있습니다(수록하지 않음).

## 검증 범위 (2026-11-21 · 1차 안전 확인)

- 확인한 파일: `archify/SKILL.md` 137줄 전수, `archify/references/update-awareness.md`(외부 확인 절차), `archify/references/delivery-contract.md` 일부, `archify/scripts/update-contract.mjs`(업데이트 확인 주소), `archify/package.json`, 루트 `LICENSE`·`NOTICE`·`LICENSE-MIT`·`THIRD_PARTY_NOTICES.md`, `README_EN.md` 설치·업데이트 항목.
- `SKILL.md` 본문에 스크립트 실행이나 원격 명령을 직접 넣지는 않았습니다. 다만 **`node bin/archify.mjs finalize` 같은 CLI 실행을 전제**로 쓰였습니다.
- → **검사 범위 내 의심 동작 0건**(1차 안전 확인). 저장소 전체 감사(1.79GB, 벤치마크·웹사이트·뷰어·테스트 다수)나 코드 실행 검증은 하지 않았습니다.

## 확인된 네트워크 동작 — 업데이트 확인 1건

- `finalize`·`deliver`를 실행하면 결과 영수증에 **업데이트 확인 결과가 함께 들어갑니다.** 고정 주소 `https://tt-a1i.github.io/archify/skill-updates/archify/stable.json`에 GET 1회(성공 후 약 24시간 캐시, 실패 시 6→24시간 재시도)를 보내고, 받은 내용은 **알림 표시에만** 쓰며 다운로드·설치·실행은 하지 않습니다(README 기재).
- 서버가 보는 것은 일반 HTTP 메타데이터(IP·시각)뿐이고 버전·에이전트·프로젝트 데이터·계정 ID는 보내지 않는다고 저장소가 밝히고 있습니다.
- 끄는 방법: 환경변수 **`ARCHIFY_UPDATE_CHECK_DISABLED=1`** (README 기재). 폐쇄망·오프라인 작업에서는 이 값을 설정하세요.
- 이 1건 외에 스킬 코어의 다이어그램 생성은 로컬 node 렌더러로 동작하며 **API 키·계정·유료 호출이 필요 없습니다**(`dependencies` 없음, `devDependencies` 는 ajv·simple-icons).

## 사용 시 주의

- **`SKILL.md` 단독으로는 실행되지 않습니다.** 본문이 `bin/archify.mjs`, `schemas/`, `examples/`, `references/`를 전제로 합니다. 이 저장소는 문서만 보관하므로, 실제 생성은 원출처 패키지를 설치해 쓰세요. 이 폴더의 `SKILL.md`는 절차·규칙 참고용입니다.
- **설치 경로가 원격 `npx`입니다.** README의 `npx -y skills@latest add https://archify.si ...`, `npx skills use tt-a1i/archify@archify`는 원격 주소에서 스킬을 받아오는 방식이라 출처·버전을 확인한 뒤 쓰는 편이 안전합니다. 오프라인·폐쇄 환경에는 맞지 않습니다.
- **오픈소스 코어와 제3자 유료 서비스는 별개입니다.** 저장소·스킬은 무료·오픈소스지만, README에는 유료 AI API 중계 서비스(Kimi Work·Supercode·OpenLux·PackyCode·AICodeMirror·Infistar 등)의 **스폰서·제휴 링크**가 실려 있습니다. 이들은 Archify가 아니라 각 사업자가 운영하며, 가입·결제는 별개 결정입니다(README에도 같은 취지가 적혀 있습니다).
- 브랜드 마크(로고)는 Simple Icons 16.28.0에서 온 벡터 데이터이고, 개별 아이콘 라이선스는 제각각입니다(Vue 로고는 CC-BY-NC-SA-4.0 등). 다이어그램을 **외부에 배포·상업 이용**할 때는 `THIRD_PARTY_NOTICES.md`의 표를 확인해야 합니다(이 저장소에는 넣지 않았음).
- **실전 HTML 생성 테스트는 하지 않았습니다.** 설치·`finalize` 통과·브라우저 확인·내보내기(이미지/SVG/WebM) 모두 미검증입니다.
- 오래 걸리는 작업입니다. 8테이블 이상 ERD는 `standard`로 먼저 뽑고, 실패 게이트는 지정된 횟수까지만 재시도하는 규칙이 본문에 있습니다.
