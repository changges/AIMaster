# AIMaster — AI 스킬 · 프롬프트 원문 창고

**클로드(Claude) · 챗지피티(ChatGPT) · 피클(Pickle)이 함께 쓰는 AI 스킬·프롬프트 아카이브**입니다.
좋은 스킬을 찾았을 때 요약본이 아니라 **원출처 원문 그대로** 모아 두고, 어느 AI에서든 같은 파일을 꺼내 쓰는 것이 목적입니다.

## 이 저장소의 4가지 규칙

1. **원문 보존** — 각 스킬의 `SKILL.md`는 원출처 파일을 **한 글자도 고치지 않고** 올립니다. 요약·번역·재작성하지 않습니다.
2. **출처·라이선스 병기** — 스킬마다 `SOURCE.md`에 저장소 주소, 원본 커밋 SHA, 라이선스, 검증일, 검증 범위를 남깁니다.
3. **실행 코드 최소화** — 마크다운 지침 문서 위주로 수록하고, 스크립트·외부 연동이 있으면 검증 범위에 명시합니다. 다른 스킬을 추가할 때는 `skill-security-audit`으로 먼저 선검수합니다.
4. **비밀정보 금지** — API 키·토큰·계정 비밀번호·개인정보는 이 저장소에 절대 올리지 않습니다. (공개 저장소이므로 누구나 볼 수 있습니다)

## 수록 목차

| # | 스킬 | 경로 | 무엇에 쓰나 | 출처 | 라이선스 | 검증일 |
|---|---|---|---|---|---|---|
| 1 | **prompt-master** | [`skills/prompt-master/`](skills/prompt-master/) | 대상 AI(클로드·챗지피티·제미나이·커서·이미지/영상 AI 등)에 맞춘 단일 최적 프롬프트 생성 | [nidhinjs/prompt-master](https://github.com/nidhinjs/prompt-master) v1.8.2 | MIT | 2026-11-15 |
| 2 | **skill-security-audit** | [`skills/skill-security-audit/`](skills/skill-security-audit/) | 설치 전 스킬·MCP 서버·확장의 코드·권한·자격증명·데이터 흐름 감사 | [sickn33/agentic-awesome-skills](https://github.com/sickn33/agentic-awesome-skills) (원출처 [sandbaseai/awesome-workbuddy](https://github.com/sandbaseai/awesome-workbuddy)) | CC0-1.0 | 2026-11-16 |
| 3 | **2d-games** | [`skills/2d-games/`](skills/2d-games/) | 2D 게임 시스템 원칙 — 스프라이트·아틀라스·타일맵·물리·카메라 | sickn33/agentic-awesome-skills | MIT | 2026-11-16 |
| 4 | **game-design** | [`skills/game-design/`](skills/game-design/) | 게임 디자인 원칙 — GDD 구조·밸런싱·플레이어 심리·성장 설계 | sickn33/agentic-awesome-skills | MIT | 2026-11-16 |
| 5 | **remotion-best-practices** | [`skills/remotion-best-practices/`](skills/remotion-best-practices/) | React 기반 영상 제작(Remotion) 실전 규칙 — 규칙 28종 + 예제 3종 | sickn33/agentic-awesome-skills | MIT | 2026-11-16 |
| 6 | **remotion-captions** | [`skills/remotion-captions/`](skills/remotion-captions/) | 자막 전사·표시·애니메이션 (Remotion `Caption` 타입) | sickn33/agentic-awesome-skills (원출처 [remotion-dev/skills](https://github.com/remotion-dev/skills) 공식, v4.0.526) | MIT | 2026-11-16 |
| 7 | **youtube-seo-optimizer** | [`skills/youtube-seo-optimizer/`](skills/youtube-seo-optimizer/) | 유튜브·팟캐스트 SEO 패키지 — 제목·설명·태그·해시태그·챕터·진단 | sickn33/agentic-awesome-skills | MIT | 2026-11-16 |
| 8 | **obsidian-skills** — `obsidian-markdown` | [`skills/obsidian-skills/obsidian-markdown/`](skills/obsidian-skills/obsidian-markdown/) | 옵시디언 문법(.md) — 위키링크·임베드·콜아웃·속성 | [obsidianmd/obsidian-skills](https://github.com/obsidianmd/obsidian-skills) (공식) | MIT | 2026-11-16 |
| 9 | 〃 `obsidian-bases` | [`skills/obsidian-skills/obsidian-bases/`](skills/obsidian-skills/obsidian-bases/) | Bases(.base) — 뷰·필터·수식·요약 | obsidianmd/obsidian-skills | MIT | 2026-11-16 |
| 10 | 〃 `json-canvas` | [`skills/obsidian-skills/json-canvas/`](skills/obsidian-skills/json-canvas/) | JSON Canvas(.canvas) — 노드·엣지·그룹·연결 | obsidianmd/obsidian-skills | MIT | 2026-11-16 |
| 11 | 〃 `obsidian-cli` | [`skills/obsidian-skills/obsidian-cli/`](skills/obsidian-skills/obsidian-cli/) | CLI로 볼트 읽기·생성·검색, 노트/태스크/속성 관리 | obsidianmd/obsidian-skills | MIT | 2026-11-16 |
| 12 | 〃 `obsidian-headless` | [`skills/obsidian-skills/obsidian-headless/`](skills/obsidian-skills/obsidian-headless/) | 앱 없이 CLI(`ob`)로 볼트 동기화·퍼블리시 | obsidianmd/obsidian-skills | MIT | 2026-11-16 |
| 13 | 〃 `defuddle` | [`skills/obsidian-skills/defuddle/`](skills/obsidian-skills/defuddle/) | 웹 페이지에서 본문만 깨끗한 마크다운으로 추출 | obsidianmd/obsidian-skills | MIT | 2026-11-16 |
| 14 | 〃 `knap` | [`skills/obsidian-skills/knap/`](skills/obsidian-skills/knap/) | 템플릿 + JSON/CSV로 마크다운 노트 대량 생성 | obsidianmd/obsidian-skills | MIT | 2026-11-16 |

총 **8개 출처 · 14종 스킬**. 스킬별 상세 검증 기록은 각 폴더의 `SOURCE.md`, 라이선스 전문은 [`LICENSES/`](LICENSES/)에 있습니다.

## 폴더 규칙

```
skills/<스킬명>/
├── SKILL.md     # 원출처 원문 그대로 (수정 금지)
├── SOURCE.md    # 출처·커밋 SHA·라이선스·검증일·검증 범위·한계
└── (첨부 문서)   # 원문이 참조하는 rules/ · references/ 등도 함께
LICENSES/        # 재배포하는 원출처 라이선스 전문
```

## 사용 방법

- **클로드 코드 / 클로드 데스크탑**: 스킬 폴더를 통째로 스킬 디렉터리(예: `~/.claude/skills/<스킬명>/`)에 복사하거나, 폴더를 ZIP으로 묶어 웹 클로드에 업로드합니다. `SKILL.md`의 frontmatter(`name`, `description`)가 그대로 살아 있어야 자동 인식됩니다.
- **챗지피티**: 프로젝트 지침이나 대화에 `SKILL.md` 원문을 붙여 넣고 "이 지침대로 처리해"라고 지시하는 방식으로 사용합니다.
- **피클**: 워크스페이스 `skills/<스킬명>/SKILL.md`로 두면 다음 작업부터 자동으로 목록에 잡힙니다.

## 갱신 이력

| 날짜 | 내용 |
|---|---|
| 2026-11-16 | 저장소를 **AI 스킬·프롬프트 원문 창고**로 정리. prompt-master, agentic-awesome-skills 6종, obsidian-skills 7종 + README 수록. 이전 README(첫 AI 프로젝트 학습 노트)는 커밋 `ceee66d`에 그대로 남아 있습니다. |
