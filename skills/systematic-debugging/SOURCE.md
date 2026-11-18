# 출처 · 검증 기록 — systematic-debugging

| 항목 | 내용 |
|---|---|
| 원출처 | [https://github.com/obra/superpowers](https://github.com/obra/superpowers) |
| 원본 경로 | `skills/systematic-debugging/SKILL.md`, `skills/systematic-debugging/root-cause-tracing.md` (**발췌 등록**) |
| 버전 | **v7.0.2** (원본 커밋 메시지 `Release v7.0.2`) |
| 원본 커밋 | `22f0b463e7a5e579904dd6211a520321035526f7` (2026-11-03) |
| 라이선스 | **MIT** — [`LICENSES/superpowers-LICENSE.txt`](../../LICENSES/superpowers-LICENSE.txt) (Copyright (c) 2025 Jesse Vincent) |
| 스타 | ⭐ 319,327 (2026-11-18 확인) |
| 저장(검증)일 | **2026-11-18** |

## 원문 보존

두 파일(`SKILL.md` 9,530B · `root-cause-tracing.md` 5,321B)은 원출처 파일을 **한 글자도 수정하지 않고** 올렸습니다. 등록 시 md5 대조로 원본과 완전 일치를 확인했습니다.

## ⚠️ 원문이 가리키는 다른 스킬 2개 (미포함)

`SKILL.md` Phase 4의 두 문장이 이 저장소에 없는 별도 스킬을 호출합니다. **문장은 원문 그대로 두었고**(수정 금지 원칙), 그대로 읽어도 지시 내용은 성립합니다.

| 원문 문구 | 위치 | 이 저장소에 없을 때 |
|---|---|---|
| `Use the \`superpowers:test-driven-development\` skill for writing proper failing tests` | Phase 4-1 | 같은 항목의 앞 줄이 이미 요구사항을 적고 있습니다 — "MUST have before fixing"(고치기 전 실패하는 테스트를 반드시 먼저 만든다). 그대로 따르면 됩니다. |
| `Use the \`superpowers:verification-before-completion\` skill before claiming success` | Phase 4-3 | 바로 위 "Verify Fix" 항목(테스트 통과·다른 테스트 깨짐 없음·실제로 해결)을 모두 확인한 뒤에만 완료를 선언하면 됩니다. |

두 스킬 원문이 필요하면 원출처 저장소의 `skills/test-driven-development/`, `skills/verification-before-completion/`에서 받으세요.

## 발췌 범위 (원본 폴더 6파일 29,057B → 2파일 14,851B)

| 원본 파일 | 등록 | 비고 |
|---|---|---|
| `SKILL.md` (9,530B) | ✅ | 4단계·레드플래그·합리화 표 |
| `root-cause-tracing.md` (5,321B) | ✅ | 호출 스택 역추적 |
| `defense-in-depth.md` (3,650B) | — | 근본 원인 후 다층 방어 |
| `condition-based-waiting.md` (3,516B) | — | 고정 타임아웃 → 조건 폴링 |
| `condition-based-waiting-example.ts` (5,054B) | — | 예제 코드 |
| `find-polluter.sh` (1,986B) | — | **실행 스크립트** — 이 저장소는 실행 코드 미수록 원칙 |

`SKILL.md` 맨 끝 "Supporting Techniques"가 위 3개 문서를 안내하므로, 필요할 때 원출처에서 꺼내 쓰면 됩니다.

## 검증 범위 (2026-11-18 · 1차 안전 확인)

- `skills/systematic-debugging/` 6파일 **전수 열람**, `hooks/`·`scripts/` grep에서 **텔레메트리·외부 전송 0건**, 악성 동작 미관찰 → **검사 범위 내 의심 동작 0건**입니다.
- **전체 저장소 보안 감사를 마쳤다는 보증이 아닙니다.** 원본 저장소 전체(236파일 1,600,920B)는 훅·릴리스 스크립트를 포함하며, 이번 검사는 해당 스킬 폴더와 훅·스크립트 경로의 외부 전송 여부만 봤습니다.
- 원본에 `pressure-test` 파일은 **없습니다**(저장소 전체 grep 확인). 압박 시나리오 개념은 `skills/writing-skills/references/` 쪽에만 있습니다.

## 설치 시 주의점

- **전체 플러그인 설치(`/plugin install superpowers@...`)는 권장하지 않습니다.** `hooks/hooks.json`이 `SessionStart` 훅(matcher `startup|clear|compact`)을 등록해 `skills/using-superpowers/SKILL.md`(**3,192B**)를 세션마다 컨텍스트에 자동 주입합니다. 이 발췌본은 **훅 없이 문서만** 쓰는 형태입니다.
- 원본 저장소 전체를 설치하면 236파일 1.6MB가 사용자 홈의 플러그인 폴더로 들어갑니다.

## 실전 실측 (2026-11-18)

시험 기록: `tmp/2026-11-18-skill-tests/REPORT.md`, 증거 `tmp/2026-11-18-skill-tests/evidence/`

- **오판 방지 1건**: PaceHero v22.1의 `user-scalable=no` 이슈에서 일반 요약은 "정상, 확대를 막아 두었음"으로 **오판**했으나, 4단계는 공식 문서(WebKit 블로그·MDN·QuirksBlog)를 근거로 "iOS 10+는 이 값을 무시, 앱에 대체 장치 0건"을 확인했습니다.
- **비용**: 같은 작업 토큰 **305 → 1,690 (×5.54)**. 자명한 한 줄 수정에는 과합니다.
- **적합한 곳**: 원인 불명 버그, 여러 번 고쳐도 안 되는 문제, 감사·검증 작업.
