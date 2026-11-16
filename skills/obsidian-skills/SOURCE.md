# 출처 · 검증 기록 — Obsidian Skills (옵시디언 공식 스킬셋 7종)

| 항목 | 내용 |
|---|---|
| 원출처 | [https://github.com/obsidianmd/obsidian-skills](https://github.com/obsidianmd/obsidian-skills) (옵시디언 공식 팀 제작, ⭐ 52,890) |
| 원본 경로 | `README.md`, `plugins/obsidian/skills/{7종}/` |
| 원본 커밋 | `398127736bd4ba42d767b1419fee1a927508370b` (2026-11-11) |
| 라이선스 | **MIT** — [`LICENSES/obsidian-skills-LICENSE.txt`](../../LICENSES/obsidian-skills-LICENSE.txt) (Copyright (c) 2026 Steph Ango (@kepano)) |
| 저장(검증)일 | **2026-11-16** |

## 수록한 7종

- **`obsidian-markdown`** — 옵시디언 문법(.md) — 위키링크·임베드·콜아웃·속성(frontmatter). `references/` 3종(CALLOUTS·EMBEDS·PROPERTIES) 포함
- **`obsidian-bases`** — 옵시디언 Bases(.base) — 뷰·필터·수식·요약. `references/FUNCTIONS_REFERENCE.md` 포함
- **`json-canvas`** — JSON Canvas(.canvas) — 노드·엣지·그룹·연결. `references/EXAMPLES.md` 포함
- **`obsidian-cli`** — 옵시디언 CLI로 볼트 읽기·생성·검색·노트/태스크/속성 관리, 플러그인·테마 개발 지원
- **`obsidian-headless`** — 데스크탑 앱 없이 CLI(`ob`)로 볼트 동기화·퍼블리시 (Obsidian Sync/Publish)
- **`defuddle`** — Defuddle CLI로 웹 페이지에서 본문만 깨끗한 마크다운으로 추출
- **`knap`** — Knap CLI로 템플릿+구조화 데이터(JSON/CSV)에서 마크다운 노트 대량 생성

## 폴더 구조

원출처는 `plugins/obsidian/skills/<스킬명>/` 아래에 있으나, 이 저장소에서는 `skills/obsidian-skills/<스킬명>/`로 평평하게 옮겨 담았습니다(파일 내용은 무수정).

## 원문 보존

`README.md`와 7종 `SKILL.md`, 그리고 각 스킬의 `references/` 문서를 **수정 없이** 그대로 올렸습니다.

## 검증 범위 (2026-11-16)

- 저장소 전체 트리 확인 후 `README.md`, `LICENSE`, `plugins/obsidian/skills/` 아래 7종 스킬과 첨부 문서 전부 대조
- 실행 스크립트는 저장소 루트의 `scripts/bump.sh`(버전 범프용) 하나뿐이며, 스킬 폴더 안에는 없습니다 — 수록 대상 아님
- 외부 유료 API 없음 (단, **Obsidian Headless Sync/Publish 서비스 이용 시에만 유료**)

## 한계

- 옵시디언 앱·CLI를 쓰지 않는 상태에서는 `obsidian-cli`·`obsidian-headless`·`defuddle`·`knap`의 실제 동작 확인이 불가능합니다(미시험).
- `defuddle`·`knap`은 각각 npm 전역 패키지 설치가 필요합니다.
