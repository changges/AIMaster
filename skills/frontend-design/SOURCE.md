# 출처 · 검증 기록 — frontend-design

| 항목 | 내용 |
|---|---|
| 원출처 | [https://github.com/anthropics/skills](https://github.com/anthropics/skills) (Anthropic 공식) |
| 원본 경로 | `skills/frontend-design/SKILL.md` (**원문 전체**), `skills/frontend-design/LICENSE.txt` |
| 원본 커밋 | `e4bb5d960d87126ff3b3a8af1a104b7db67560ba` (2026-11-16) |
| 라이선스 | **Apache-2.0** — 원본 폴더의 `LICENSE.txt` 전문을 [`LICENSES/frontend-design-LICENSE.txt`](../../LICENSES/frontend-design-LICENSE.txt)로 옮겼습니다. |
| 스타 | ⭐ 197,210 (2026-11-19 확인) |
| 저장(검증)일 | **2026-11-19** (창현 님 승인: 텔레그램 1308번) |

## 원문 보존

`SKILL.md` **71줄 9,390B를 한 글자도 수정하지 않고** 올렸습니다(md5 `7d6df6b2e98e38f8b86046325dc6afd0` 대조 일치). 이 폴더에는 `SKILL.md`와 이 `SOURCE.md` 두 파일만 있습니다.

## 라이선스 주의

- 원본 폴더의 `LICENSE.txt`는 **저작자 표기 줄 없이 Apache-2.0 본문만** 들어 있습니다(10,174B, 177줄, 그대로 보존). 저장소 README는 "Many skills in this repo are open source (Apache 2.0)"라고 밝히고 있어 이 스킬을 Apache-2.0으로 재배포합니다.
- 같은 README의 고지: **"These skills are provided for demonstration and educational purposes only."** — 참고용이며, 같은 이름의 기능이 실제 클로드에서 다르게 동작할 수 있습니다.

## 검증 범위 (2026-11-19 · 1차 안전 확인)

- `skills/frontend-design/` 폴더는 **파일 2개뿐**(`SKILL.md` 9,390B · `LICENSE.txt` 10,174B)이며 둘 다 **전수 열람**했습니다.
- `SKILL.md`는 **순수 Markdown 지침**입니다 — 스크립트·실행 코드·외부 URL 요청·텔레메트리 **0건**, frontmatter에도 `allowed-tools`가 없습니다.
- → **검사 범위 내 의심 동작 0건**입니다. **저장소 전체(약 5.4MB · 스킬 폴더 19개) 보안 감사 보증은 아닙니다.**

## 무엇에 쓰나

- 디자인 방향·타이포·레이아웃을 **주제(subject)에서 끌어내는** 원칙: 색 토큰 4~6개, 서체 역할, ASCII 와이어프레임, 고유 원칙을 먼저 계획하고 → 브리프와 대조해 일반론으로 흐른 부분을 수정 → 그다음 코드.
- **AI 생성물의 클리셰 5종**을 명시적으로 회피합니다(크림 배경+테라코타 액센트, 검정 배경+산성 형광, 신문형 헤어라인 레이아웃, SaaS 카드 키트, 대문자 눈썹 라벨·가운뎃점 메타 문자열).
- 카피라이팅 규칙(사용자 관점 어휘, 능동태, 같은 동작은 같은 이름, 오류·빈 화면 처리)과 "여백 하나는 덜어내기" 자기 비평도 포함합니다.

## 사용 시 주의

- **가이드 문서이지 코드가 아닙니다.** 실제 UI 컴포넌트·CSS는 별도로 작성해야 합니다.
- 웹 기준으로 쓰였습니다. iOS 앱(페이스히어로·소늘이)에 적용할 때는 터치 타깃·대비 같은 수치 기준을 `skills/ui-ux-pro-max-rules/`와 함께 보는 편이 좋습니다.
- "브리프가 지정한 방향이 항상 이긴다"는 규칙이 있으므로, 창현 님의 기존 취향(심플·미니멀·연두/무채색)을 브리프에 먼저 적어 두고 쓰면 됩니다.

## ⚠️ 주의사항

⚠️ 주의사항: 1차 검토는 `skills/frontend-design/` 폴더 내 지침·`LICENSE.txt` 범위만 확인했으며(전체 저장소 아님), 디자인 가이드이므로 실제 UI 컴포넌트 코드는 별도 구현이 필요합니다.
