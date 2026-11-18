# 출처 · 검증 기록 — caveman

| 항목 | 내용 |
|---|---|
| 원출처 | [https://github.com/JuliusBrussee/caveman](https://github.com/JuliusBrussee/caveman) |
| 원본 경로 | `skills/caveman/SKILL.md` (**원문 전체**) |
| 원본 커밋 | `a192894723a8f47e7f504c7b5041967ff1f18e55` (2026-11-17) |
| 라이선스 | **Apache-2.0** (3.0.0부터) — [`LICENSES/caveman-LICENSE.txt`](../../LICENSES/caveman-LICENSE.txt) |
| 저작자 표기 | **Copyright 2026 Julius Brussee** — Apache-2.0 §4(d) NOTICE 전문을 [`LICENSES/caveman-NOTICE.txt`](../../LICENSES/caveman-NOTICE.txt)에 함께 두었습니다. |
| 스타 | ⭐ 121,063 (2026-11-18 확인) |
| 저장(검증)일 | **2026-11-18** |

## 원문 보존

`SKILL.md` **90줄 4,678B를 한 글자도 수정하지 않고** 올렸습니다(md5 대조 일치). 이 폴더에는 `SKILL.md`와 이 `SOURCE.md` 두 파일만 있습니다.

## 라이선스 주의

- 원본은 3.0.0 이전까지 저장소가 나뉘어 있었고(MIT + Business Source 1.1), **3.0.0부터 전체가 Apache-2.0**입니다(`LICENSING.md`). 이 저장소가 옮긴 파일은 3.0.0 이후 커밋의 `skills/caveman/SKILL.md` 하나이므로 Apache-2.0 조건으로 재배포합니다.
- 원본 `NOTICE`에는 이 저장소가 함께 배포하지 않는 부분(`engine/pixel/`, `browse/`, 번들 npm 패키지, Geist 폰트 등)의 제3자 표기가 섞여 있습니다. 그 전문을 그대로 `LICENSES/caveman-NOTICE.txt`에 보존했습니다.
- "Caveman"은 저작자의 상표입니다. Apache-2.0은 상표권을 주지 않으므로, 이 파일은 **규칙 참고용**으로만 쓰고 제품·서비스 이름에 쓰지 않습니다.

## 검증 범위 (2026-11-18 · 1차 안전 확인)

- 이 스킬은 **`SKILL.md` 90줄 단독으로 완결**됩니다. 저장소에 프록시(`proxy/`)·엔진(`engine/`)·`supabase/`·CLI·확장이 있지만 모두 **별도 제품**이고, `SKILL.md`만 쓰면 설치·외부 호출이 0건입니다.
- `SKILL.md` 안에 **스크립트·외부 URL 요청·텔레메트리 0건**(본문 전체 확인). 훅은 Cursor용 `hooks/hooks-cursor.json` 하나뿐이며 강제가 아닙니다.
- → **검사 범위 내 의심 동작 0건**입니다. **저장소 전체(1,825파일 21.7MiB) 보안 감사 보증은 아닙니다.**

## 실측 — "토큰 65% 절감" 문구는 쓰지 않습니다

| 측정 | 결과 |
|---|---|
| 제작사 자체 벤치마크(`evals/snapshots/results.json`, 2026-10-02, claude-opus-5-5, 10개 프롬프트, 1회) | caveman 기본 모드 **−2.9%** (`Answer concisely.` 대조군 409 토큰 → 386). 더 길어진 프롬프트 **5/10**. megacave −9.1%, ultracave −34.7% |
| 재계산 | tiktoken o200k로 다시 세어도 위 값과 일치(README 공개 주장 3%·9%·35%와 동일) |
| 이 환경 실측(한국어 요약 2과제, n=1) | 문자·토큰 **−19.8~−39.9%**, 필수 사실 보존 10/10·8/8, 줄 번호·수치 원형 유지 |

**해석**: 절감의 정체는 문법 압축이 아니라 **의례 제거**(인사·연결어·마무리)입니다. 그래서 "토큰 대폭 절감"을 기대하고 등록하면 기대에 못 미칩니다. **"군더더기 없는 요약 문체 규칙"**으로 쓰는 것이 맞습니다. (n=1이고 양쪽 문장을 같은 모델이 썼으므로 절감 폭에는 작성자 편향이 섞일 수 있습니다.)

## 사용 시 주의

- 이 스킬은 **세션이 끝날 때까지 모드를 유지**하도록 설계됐습니다. 보고용으로 잠깐만 쓰려면 "stop caveman" / "normal mode"로 끄는 규약을 지켜야 합니다.
- "규칙을 깨는 7가지"(보안 경고, 되돌릴 수 없는 동작, 단계 순서, 질문, 외부에 남는 문서 등)는 그대로 두는 것이 안전합니다 — 브리핑·보고 사고를 막는 장치입니다.
