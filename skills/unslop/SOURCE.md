# 출처 · 검증 기록 — unslop

## 저작자 표시 (CC BY 4.0 — 이 표기는 복제·개작 시 반드시 유지)

| 항목 | 내용 |
|---|---|
| 제목 | **unslop** |
| 저작자 | **Damir Sokolovsky** ([@heydamir](https://x.com/heydamir) · https://heydamir.design/unslop) |
| 원출처 | https://github.com/heydamir/unslop |
| 라이선스 | **CC BY 4.0** (Creative Commons Attribution 4.0 International) — 전문: [`LICENSES/unslop-LICENSE-CC-BY-4.0.txt`](../../LICENSES/unslop-LICENSE-CC-BY-4.0.txt) · 라이선스 링크 https://creativecommons.org/licenses/by/4.0/ |
| 변경 여부 | **변경 없음** — `SKILL.md` 원문 그대로 복제(번역·요약·수정 없음). 이 `SOURCE.md`만 이 저장소에서 덧붙인 기록입니다. |
| 원본 커밋 | `620163eedb3529d9cd23a3994ed8d287d06f760d` (2026-11-15) |
| 원본 경로 | `skills/unslop/SKILL.md` (**원문 전체**) |
| 스타 | ⭐ 18,681 (2026-11-20 `gh api` 확인) |
| 저장(검증)일 | **2026-11-20** (창현 님 승인: 텔레그램 1664번 "딱히 이상없으면 기록해") |

> 원문 `SKILL.md` 첫머리에도 "unslop was created by Damir Sokolovsky (@heydamir) … It is licensed under CC BY 4.0, so keep this credit in any copy or adaptation."이라고 적혀 있습니다. 이 스킬로 만든 결과물(스토리 영상)에는 원문 규칙대로 `unslop by @heydamir` 출처 한 줄을 넣어야 합니다.

## 원문 보존

`SKILL.md` **236줄 32,059B를 한 글자도 수정하지 않고** 올렸습니다(md5 `555ef826baa2283f2a86fdde8c25e31a` 대조 일치). 이 폴더에는 `SKILL.md`와 이 `SOURCE.md` 두 파일만 있습니다.

## 이 저장소에 넣은 것 / 넣지 않은 것

| 원본 파일 | 등록 | 비고 |
|---|---|---|
| `skills/unslop/SKILL.md` (32,059B) | ✅ | 9단계 패스(간격→색→아이콘→카피→타이포→레이아웃→디테일→비주얼→모션), 방향 5줄, 체크리스트 21항, 스토리 영상 규격 |
| `skills/unslop/references/` 6종 — `tokens.md`(137줄)·`signs.md`(122줄)·`visuals.md`(84줄)·`effects.md`(113줄)·`rtl.md`(72줄)·`refs.md`(17줄) + `refs/*.webp` 5장 | ❌ | `SKILL.md`가 수치의 근거로 계속 가리키는 문서 — 열람만 하고 옮기지 않았습니다(수치가 필요하면 원출처에서 함께 받기) |
| `skills/unslop/scripts/snapshot.mjs` (197줄) | ❌ | **열람 완료** — 스크린샷·HTML 저장 도구 |
| `skills/unslop/scripts/story.mjs` (505줄) · `story-path.mjs` (27줄) | ❌ | 열람·실행하지 않음 |
| `skills/unslop/agents/openai.yaml` · `examples/*.html` 3종 · `test/` 3종 · `.claude-plugin/` 매니페스트 | ❌ | 보조 파일 |

## 검증 범위 (2026-11-20 · 1차 안전 확인)

- `SKILL.md` 본문 **전수 열람**: 마크다운 지침만 있고 실행 코드·외부 호출은 이 파일 안에 **0건**입니다. 언급되는 유일한 실행 경로는 로컬 `node scripts/snapshot.mjs`·`story.mjs`입니다.
- `scripts/snapshot.mjs` **전수 열람**: 주소를 열어(local Playwright Chromium) 스크롤·이미지 로딩을 기다린 뒤, 페이지 자신의 스타일시트·이미지를 `data:`로 인라인해 **로컬 파일(`.html`, `.live.png`)로 저장**합니다. `fetch`는 페이지가 이미 불러온 같은 사이트 자원에만 쓰이고, **외부 서버로 보내는 요청·텔레메트리·인증 정보 수집은 없습니다.**
- `story.mjs`(505줄)는 **읽지 않았고 실행하지도 않았습니다.** 스토리 영상 기능을 쓰려면 그 파일부터 따로 확인이 필요합니다.
- → **검사 범위 내 의심 동작 0건**입니다. **저장소 전체(29개 파일) 감사나 렌더·실행 검증을 마쳤다는 뜻이 아닙니다.**

## 무슨 스킬인가 — "AI 티 나는 UI"를 9패스로 정돈

| 순서 | 패스 | 핵심 |
|---|---|---|
| 0 | 방향 5줄 | 제품·성격·세계·모먼트·시그니처를 먼저 적고 **사용자 확인 후** 편집 |
| 1~2 | 간격·색 | 4px 그리드, 하나의 뉴트럴 램프, 액센트 1개, 그라데이션·글로우 제거 |
| 3~5 | 아이콘·카피·타이포 | 이모지→라인 아이콘, 느낌표·환영 문구·과장어 금지, 400~600 두께만 |
| 6~7 | 레이아웃·디테일 | 앱 비율 유지(사이드바 240~280), 중첩 라운드, 차트 위계 |
| 8~9 | 비주얼·모션 | 장식용 블롭 제거, 히어로는 실제 장면 1컷, 무한 반복 모션 제거 |

## 이 저장소에서 쓸 때

- 페이스히어로·소늘이·2D 게임 화면의 "바이브코딩 티"를 걷어낼 때 쓰는 **프롬프트형** 스킬입니다. 코드를 자동 수정하는 도구가 아니므로 클로드·챗지피티에 `SKILL.md`를 붙여 넣고 화면 코드를 함께 주는 방식으로 씁니다.
- `references/tokens.md`의 정확한 수치가 필요하면 원출처 폴더를 함께 받으세요. 이 폴더만으로는 `SKILL.md`가 "값은 tokens.md에 있다"고 가리키는 부분이 비어 있습니다.

## ⚠️ 주의사항

⚠️ 주의사항: **CC BY 4.0**이므로 복제·개작·배포 시 원저작자 **Damir Sokolovsky([@heydamir])** 표기와 라이선스 링크를 반드시 남기고, 스토리 영상 결과물에는 `unslop by @heydamir` 한 줄을 넣어야 합니다. `snapshot.mjs`로 캡처할 때 **로그인한 화면·비공개 페이지·타사 사이트는 저장하지 마세요**(쿠키가 실린 세션 내용이 파일로 남습니다). 원문 8단계의 **이미지 생성 도구 사용(유료 API 가능)** 부분은 사용 범위에서 제외하고, 코드로 만들 수 있는 비주얼·프롬프트 작성까지만 참고하세요. 1차 안전 확인(SKILL.md·snapshot.mjs 읽은 범위 내 의심 동작 0건)만 했고, `story.mjs` 포함 전체 코드 감사·실행 검증은 하지 않았습니다.
