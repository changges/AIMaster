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
| 15 | **systematic-debugging** (발췌 2파일) | [`skills/systematic-debugging/`](skills/systematic-debugging/) | 근본 원인 조사 없이는 수정 금지 — 4단계 디버깅·호출 스택 역추적 | [obra/superpowers](https://github.com/obra/superpowers) v7.0.2 | MIT | 2026-11-18 |
| 16 | **ui-ux-pro-max-rules** (발췌) | [`skills/ui-ux-pro-max-rules/`](skills/ui-ux-pro-max-rules/) | UI 수치 기준(iOS 44pt·Android 48dp·웹 WCAG 24px·대비 4.5:1) + 배포 전 체크리스트 | [nextlevelbuilder/ui-ux-pro-max-skill](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill) v2.15.0 | MIT | 2026-11-18 |
| 17 | **caveman** | [`skills/caveman/`](skills/caveman/) | 군더더기(인사·연결어·마무리) 제거 문체 규칙 — 사실·수치는 원형 유지 | [JuliusBrussee/caveman](https://github.com/JuliusBrussee/caveman) | Apache-2.0 (+NOTICE) | 2026-11-18 |
| 18 | **frontend-design** | [`skills/frontend-design/`](skills/frontend-design/) | AI 클리셰를 피하는 디자인 방향 — 색 토큰·타이포·레이아웃 2패스 계획과 카피 규칙 | [anthropics/skills](https://github.com/anthropics/skills) (공식) | Apache-2.0 | 2026-11-19 |
| 19 | **last30days** (원문 1파일 · 실행 코드 제외) | [`skills/last30days/`](skills/last30days/) | 최근 30일 여론 리서치의 출력 계약 LAW 1~11 · 제출 전 자기 점검 · 소스별 무료/유료 구분 | [mvanhorn/last30days-skill](https://github.com/mvanhorn/last30days-skill) v4.3.2 | MIT | 2026-11-19 |
| 20 | **self-improving-agent** | [`skills/self-improving-agent/`](skills/self-improving-agent/) | `MEMORY.md` 자동 학습을 `CLAUDE.md`·`.claude/rules/`·스킬로 승격하는 큐레이션 워크플로 | [alirezarezvani/claude-skills](https://github.com/alirezarezvani/claude-skills) v1.0.0 | MIT | 2026-11-19 |
| 21 | **webapp-testing** (원문 1파일 · 스크립트 제외) | [`skills/webapp-testing/`](skills/webapp-testing/) | 로컬 웹앱을 Playwright로 띄워 화면·셀렉터·콘솔 로그를 직접 확인 | [anthropics/skills](https://github.com/anthropics/skills) (공식) | Apache-2.0 | 2026-11-20 |
| 22 | **unslop** | [`skills/unslop/`](skills/unslop/) | 바이브코딩 UI의 'AI 티'를 9패스(간격→색→아이콘→카피→타이포→레이아웃→디테일→비주얼→모션)로 걷어내는 디자인 패스 | [heydamir/unslop](https://github.com/heydamir/unslop) — **저작자 Damir Sokolovsky [@heydamir]** | CC-BY-4.0 | 2026-11-20 |
| 23 | **cartoon-3d-short** (저장소: Claude Animated Shorts) | [`skills/cartoon-3d-short/`](skills/cartoon-3d-short/) | three.js+Remotion 로컬 렌더로 55~70초 세로 스토리 쇼츠를 만드는 11단계 파이프라인 | [mromidev/claude-animated-shorts](https://github.com/mromidev/claude-animated-shorts) | MIT | 2026-11-20 |

총 **16개 출처 · 23종 스킬**. 스킬별 상세 검증 기록은 각 폴더의 `SOURCE.md`, 라이선스 전문은 [`LICENSES/`](LICENSES/)에 있습니다.

## ⚠️ 주의사항 (2026-11-20 등록 3종)

프롬프트 본문에는 사용 내용만 두고, 검토 범위와 제한은 아래에 따로 적습니다.

- **webapp-testing** — ⚠️ 주의사항: `with_server.py`가 `--server` 문자열을 `shell=True`로 실행하므로 **직접 작성한 신뢰하는 프로젝트에서만** 사용하고, 남이 준 명령 문자열을 그대로 넣지 마세요. Python Playwright(`pip install playwright` + `playwright install chromium`)가 필요하며, 로컬 브라우저 자동화라 **아이폰·애플워치 실기기 테스트를 대체할 수 없습니다**. 1차 안전 확인(읽은 범위 내 의심 동작 0건)만 했고 전체 코드 감사·실행 검증은 하지 않았습니다.
- **unslop** — ⚠️ 주의사항: **CC BY 4.0**이므로 복제·개작·배포 시 원저작자 **Damir Sokolovsky([@heydamir])** 표기와 라이선스 링크를 반드시 남기고, 스토리 영상 결과물에는 `unslop by @heydamir` 한 줄을 넣어야 합니다. `snapshot.mjs`로 캡처할 때 **로그인한 화면·비공개 페이지·타사 사이트는 저장하지 마세요**(쿠키가 실린 세션 내용이 파일로 남습니다). 원문 8단계의 **이미지 생성 도구 사용(유료 API 가능)** 부분은 사용 범위에서 제외하고, 코드로 만들 수 있는 비주얼·프롬프트 작성까지만 참고하세요. 1차 안전 확인(SKILL.md·snapshot.mjs 읽은 범위 내 의심 동작 0건)만 했고, `story.mjs` 포함 전체 코드 감사·실행 검증은 하지 않았습니다.
- **cartoon-3d-short** — ⚠️ 주의사항: ASMR 영상용이 아니라 **스토리 쇼츠(55~70초·내레이션·음성 별도 준비)** 후보이며, 원출처 `templates/`·`scripts/`를 함께 받아야만 동작합니다. Remotion은 번들마다 `public/`(약 1.3GB)를 임시 폴더로 복사하므로 **디스크 여유를 확인하고 `TEMP`/`TMP`를 큰 드라이브로 지정**해야 하며(원저작자도 60GB 이상 차서 렌더가 죽었다고 기록), 2K 렌더는 약 4fps로 67초 영상에 **10분 내외** 걸립니다. `references/`의 참고 프레임·콘택트시트는 **스타일 학습용**이므로 그대로 복사·업로드·공개하지 말고, 스토리·캐릭터·음성은 반드시 직접 만드세요. 1차 안전 확인(SKILL.md·README 읽은 범위 내 의심 동작 0건)만 했고 전체 코드 감사·실행 검증은 하지 않았습니다.

공통: 세 종 모두 **1차 안전 확인**(확인한 범위에서 의심 동작 0건)이며, 저장소 전체 보안 감사나 코드 실행 검증을 마쳤다는 뜻이 아닙니다. "100% 안전"으로 읽지 마세요.

## ⚠️ 주의사항 (2026-11-19 등록 3종)

프롬프트 본문에는 사용 내용만 두고, 검토 범위와 제한은 아래에 따로 적습니다.

- **frontend-design** — ⚠️ 주의사항: 1차 검토는 `skills/frontend-design/` 폴더 내 지침·`LICENSE.txt` 범위만 확인했으며(전체 저장소 아님), 디자인 가이드이므로 실제 UI 컴포넌트 코드는 별도 구현이 필요합니다.
- **last30days** — ⚠️ 주의사항: 240KB 파이썬 엔진(`last30days.py`) 및 `scripts/`(`box_chrome_login.py` 브라우저 쿠키 읽기 경로 포함)는 코드 감사 전 실행 금지이며, 유료 API(ScrapeCreators 등) 가입 권유·X/YouTube/TikTok 등 유료·로그인 확장 소스는 사용 범위에서 제외하고 무료 소스·프롬프트 워크플로만 참고하세요.
- **self-improving-agent** — ⚠️ 주의사항: 윈도우 클로드 코드(v2.1.32+) 자동 메모리 환경을 전제로 하며, 410개+ 모노레포 전체 클론 금지 및 `hooks/`·`settings.json` 등 보조 스크립트 실행 전 코드 추가 확인이 필요하므로 당장은 `SKILL.md` 프롬프트·워크플로 발췌만 참고하세요.

공통: 세 종 모두 **1차 안전 확인**(확인한 범위에서 의심 동작 0건)이며, 저장소 전체 보안 감사나 코드 실행 검증을 마쳤다는 뜻이 아닙니다. "100% 안전"으로 읽지 마세요.

- **소늘이 AI 지식창고 등록 상태**: POST 응답(`ok: true`, IDs `1795050236856010~12`) 기준 서버 접수만 확인되었으며, 아이폰 소늘이 앱 동기화 후 'AI 지식' 탭 실제 표시는 미확인 상태입니다.

## 폴더 규칙

```
skills/<스킬명>/
├── SKILL.md     # 원출처 원문 그대로 (수정 금지)
├── SOURCE.md    # 출처·커밋 SHA·라이선스·검증일·검증 범위·한계
└── (첨부 문서)   # 원문이 참조하는 rules/ · references/ 등도 함께
LICENSES/        # 재배포하는 원출처 라이선스 전문
```

- **발췌 등록**일 때는 원문 파일을 원래 파일명 그대로 옮기고(`pro-rules.md` 등), 폴더 안내용 `SKILL.md`를 따로 둘 수 있습니다. 이때 그 `SKILL.md`는 원문이 아니므로 파일 첫머리와 `SOURCE.md`에 그 사실을 밝힙니다(예: `ui-ux-pro-max-rules/`).
- 원본 `SKILL.md`가 별도 스크립트·데이터를 전제해 단독으로 읽히지 않으면, 그 파일은 싣지 않고 자립적으로 읽히는 문서만 발췌합니다.

## 사용 방법

- **클로드 코드 / 클로드 데스크탑**: 스킬 폴더를 통째로 스킬 디렉터리(예: `~/.claude/skills/<스킬명>/`)에 복사하거나, 폴더를 ZIP으로 묶어 웹 클로드에 업로드합니다. `SKILL.md`의 frontmatter(`name`, `description`)가 그대로 살아 있어야 자동 인식됩니다.
- **챗지피티**: 프로젝트 지침이나 대화에 `SKILL.md` 원문을 붙여 넣고 "이 지침대로 처리해"라고 지시하는 방식으로 사용합니다.
- **피클**: 워크스페이스 `skills/<스킬명>/SKILL.md`로 두면 다음 작업부터 자동으로 목록에 잡힙니다.

## 갱신 이력

| 날짜 | 내용 |
|---|---|
| 2026-11-16 | 저장소를 **AI 스킬·프롬프트 원문 창고**로 정리. prompt-master, agentic-awesome-skills 6종, obsidian-skills 7종 + README 수록. 이전 README(첫 AI 프로젝트 학습 노트)는 커밋 `ceee66d`에 그대로 남아 있습니다. |
| 2026-11-18 | 11-18 9시 브리핑 실전 비교 시험 통과 3종 추가 — systematic-debugging(발췌), ui-ux-pro-max-rules(발췌), caveman(원문). 라이선스 4종(MIT 2 · Apache-2.0 + NOTICE 2)과 시험 결과·한계를 각 `SOURCE.md`에 기록. |
| 2026-11-19 | 11-19 9시 브리핑 3종 추가 — frontend-design(원문, Apache-2.0 라이선스 전문 동봉), last30days(`SKILL.md` 원문 1파일만 · 엔진·`references/`·쿠키 스크립트 제외), self-improving-agent(`SKILL.md` 원문 1파일만 · `hooks/`·`settings.json` 제외). 라이선스 3종(MIT 2 · Apache-2.0 1) 추가, 창현 님 지시(텔레그램 1308번)대로 **주의사항을 본문과 섞지 않고 아래에 따로** 적었습니다. |
| 2026-11-20 | 11-20 9시 브리핑 3종 추가 — webapp-testing(원문, Apache-2.0 라이선스 전문 동봉 · `scripts/`·`examples/` 제외), unslop(`SKILL.md` 원문, **CC BY 4.0 저작자 표기** 전문 동봉 · `references/`·`scripts/` 제외), cartoon-3d-short(`SKILL.md` 원문, MIT · `templates/`·`references/` 제외). 라이선스 3종(Apache-2.0 · CC-BY-4.0 · MIT) 추가. |
