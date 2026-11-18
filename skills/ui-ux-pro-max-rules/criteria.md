# UI 수치 기준표 (원출처 발췌 정리)

> 이 파일은 **원문 그대로가 아니라 이 저장소에서 뽑아 정리한 참조표**입니다. 인용은 원출처 문장을 그대로 옮겼고, 각 항목에 출처 파일·행을 적었습니다.
> 원출처: `nextlevelbuilder/ui-ux-pro-max-skill` 커밋 `e59ff376` (2026-11-16), MIT. 경로는 `.claude/skills/ui-ux-pro-max/` 기준.

## 1. 플랫폼별 터치 타깃 최소 크기 — **플랫폼마다 다릅니다**

| 플랫폼 | 최소 크기 | 근거 원문 |
|---|---|---|
| iOS | **44pt** | `data/app-interface.csv` 7행: *"Native targets use 44pt on iOS and 48dp on Android; web WCAG 2.2 has a separate 24 by 24 CSS px minimum with exceptions"* |
| Android | **48dp** | 〃 |
| 웹 | **24 × 24 CSS px** (WCAG 2.2 AA 2.5.8, 예외 있음) | `data/ux-guidelines.csv` 105행: *"WCAG 2.2 AA requires 24 CSS px pointer targets or an applicable exception"* |

원출처가 명시한 **흔한 실수**: *"Collapse iOS 44pt, Android 48dp, and web 24 CSS px into one cross-platform number"* — 세 값을 하나로 뭉뚱그리는 것.

판정 요령(실측에서 쓴 방식): 웹앱이면 **WCAG 24px로 적합/부적합을 먼저 판정**하고, 44pt·48dp는 "플랫폼 권장 미달"로 따로 적습니다. 44px를 웹 기준으로 써서 "결함"이라고 단정하면 과잉 판정이 됩니다.

## 2. 그 밖의 수치 기준

| 항목 | 기준값 | 근거 원문 |
|---|---|---|
| 본문 텍스트 대비 | **4.5:1 이상** | `references/pro-rules.md` Light/Dark Mode 표: *"Maintain body text contrast >=4.5:1 against light surfaces"* |
| 의미 있는 아이콘·컨트롤 경계 대비 | **3:1 이상** | 〃 Icons 표: *"Meaningful icons and control boundaries need at least 3:1 against adjacent colors"* (비텍스트 대비 기준) |
| 큰 글자·비텍스트 UI | 3:1 허용 | 〃: *"normal text contrast >=4.5:1 on dark surfaces; 3:1 is only for large text or non-text UI"* |
| 누름 피드백 | **80~150ms 안에** | 〃 Interaction 표: *"Provide clear pressed feedback (ripple/opacity/elevation) within 80-150ms"* |
| 본문 글자 크기(웹) | 기본 16px, **12px 미만 본문 금지** | `SKILL.md` 우선순위 6행: 안티패턴 *"Text < 12px body"* |
| 줄 높이 | 1.5 | 〃: *"Base 16px, Line-height 1.5, Semantic color tokens"* |
| 간격 리듬 | **4/8dp 배수** | `references/pro-rules.md` Layout 표: *"Use a consistent 4/8dp spacing system for padding/gaps/section spacing"* |
| 애니메이션 | reduced-motion 존중, width/height 애니메이션 금지 | `SKILL.md` 우선순위 7행 안티패턴: *"One duration for every transition, Animating width/height, No reduced-motion"* |
| 폼 | 라벨은 항상 보이게, 오류는 필드 옆에 | 〃 8행: *"Visible labels, Error near field"* / 안티패턴 *"Placeholder-only label"* |
| 내비게이션 | 하단 탭 **5개 이하**, 뒤로가기 예측 가능, 딥링크 | 〃 9행 |

## 3. 안티패턴 목록 (원출처 `SKILL.md` 우선순위 표)

| # | 카테고리 | 피할 것 (원문) |
|---|---|---|
| 1 | Accessibility | *Removing focus rings, Icon-only buttons without labels* |
| 2 | Touch & Interaction | *Reliance on hover only, Instant state changes (0ms)* |
| 3 | Performance | *Layout thrashing, Cumulative Layout Shift* (CLS < 0.1 유지) |
| 4 | Style Selection | *Mixing flat & skeuomorphic randomly, Emoji as icons* |
| 5 | Layout & Responsive | *Horizontal scroll, Fixed px container widths, **Disable zoom*** |
| 6 | Typography & Color | *Text &lt; 12px body, Gray-on-gray, Raw hex in components* |
| 7 | Animation | *One duration for every transition, Animating width/height, No reduced-motion* |
| 8 | Forms & Feedback | *Placeholder-only label, Errors only at top, Overwhelm upfront* |
| 9 | Navigation Patterns | *Overloaded nav, Broken back behavior, No deep links* |
| 10 | Charts & Data | *Relying on color alone to convey meaning* |

**"Disable zoom"** 항목은 `<meta name="viewport" content="... user-scalable=no">`를 안티패턴으로 규정한 것입니다(모바일 웹 WCAG 1.4.4 연계).

## 4. 이 기준표를 쓸 때의 한계 (실측에서 확인)

- 원출처의 검색 스크립트는 **키워드 매칭**입니다. 결과 용어로 물으면 맞고("touch target minimum 44px"), 증상으로 물으면 빗나갑니다("small screen controls button too small"). 이 발췌본에는 스크립트가 없습니다.
- 이 스킬은 **CSS를 읽고 결함을 찾아 주는 분석기가 아닙니다.** 기준값과 체크리스트를 주는 도구이고, 실제 대조는 사람(또는 에이전트)이 코드를 읽고 계산해야 합니다.
