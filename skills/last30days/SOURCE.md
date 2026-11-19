# 출처 · 검증 기록 — last30days

| 항목 | 내용 |
|---|---|
| 원출처 | [https://github.com/mvanhorn/last30days-skill](https://github.com/mvanhorn/last30days-skill) |
| 원본 경로 | `skills/last30days/SKILL.md` (**원문 전체 · v4.3.2**) |
| 원본 커밋 | `a854f3bcb2c4344d7498426d653378510f8b253a` (2026-11-17) |
| 라이선스 | **MIT** — Copyright (c) 2026 Matt Van Horn — [`LICENSES/last30days-LICENSE.txt`](../../LICENSES/last30days-LICENSE.txt) |
| 스타 | ⭐ 70,012 (2026-11-19 확인) |
| 저장(검증)일 | **2026-11-19** (창현 님 승인: 텔레그램 1308번 · **조건부** 등록) |

## 원문 보존

`SKILL.md` **260줄 31,609B를 한 글자도 수정하지 않고** 올렸습니다(md5 `a7fc404da5d246c55e0627bfa1218c56` 대조 일치). 이 폴더에는 `SKILL.md`와 이 `SOURCE.md` 두 파일만 있습니다.

## 이 저장소에 넣은 것 / 넣지 않은 것

| 원본 파일 | 등록 | 비고 |
|---|---|---|
| `SKILL.md` (31,609B) | ✅ | 프롬프트·워크플로·출력 계약·보안 고지 |
| `scripts/last30days.py` (240,497B) | ❌ | **실행 엔진** — 코드 감사 전 실행 금지 |
| `scripts/box_chrome_login.py` (8,141B) 외 `scripts/` 14개 | ❌ | 브라우저 쿠키 로그인 경로 포함 |
| `references/` 16개 (research-runbook.md 73,910B · setup-wizard.md 45,941B · synthesis.md 27,312B 등, 합계 약 300KB) | ❌ | `SKILL.md`가 단계마다 전문 열람을 요구하는 하위 문서 |
| `agents/` · `assets/`(약 11MB 이미지·음원) | ❌ | 실행·자료 파일 |

**그래서 이 등록본은 "실행 도구"가 아니라 읽는 문서입니다.** `SKILL.md`는 스스로 "Python 3.12+ 엔진을 실행하라"고 지시하는 **디스패치 계약**이라, `references/`와 `scripts/` 없이 설치하면 그대로는 동작하지 않습니다. 프롬프트 규칙(출력 계약 LAW 1~11, 제출 전 자기 점검 9항)과 소스별 무료/유료 구분을 참고하는 용도입니다.

## 검증 범위 (2026-11-19 · 1차 안전 확인)

- `SKILL.md` 본문 전체를 열람하고, 원본이 스스로 적은 **"Security & Permissions"** 절을 대조했습니다. 외부 전송 대상이 스스로 열거돼 있습니다: ScrapeCreators(api.scrapecreators.com — TikTok·Instagram·일부 Reddit), X API v2(api.x.com) · xAI · Xquik, (레거시) OpenAI Responses API, Algolia HN Search, dev.to, Polymarket Gamma, Wikidata, USPTO 특허, `yt-dlp` 로컬 YouTube, 선택 시 Brave/Parallel/Perplexity/OpenRouter.
- 쿠키 접근: `reddit_session` 쿠키는 **`REDDIT_BROWSER_CONSENT=true` 명시 동의일 때만** 읽는다고 `SKILL.md`가 밝히고 있고, `scripts/box_chrome_login.py`는 브라우저 로그인으로 쿠키를 가져오는 별도 경로입니다. **둘 다 이번 등록 범위 밖이며, 동의 없이 쓰지 않습니다.**
- 악성 동작은 관찰하지 않았습니다(지침 문서만 열람). 다만 **엔진 코드 240KB는 감사하지 않았으므로 "의심 동작 0건"은 엔진에 대해 말하는 것이 아닙니다.**

## 실제로 키 없이 도는 소스 (원본 README 기준, 2026-11-19 확인)

| 소스 | 조건 |
|---|---|
| Reddit(댓글 포함) · Hacker News · Polymarket · GitHub | **키 없이 즉시 동작** |
| 미국 특허 출원 · 기업 채용 페이지 | 기업·인물 주제에서 **키 없이 동작** |
| StockTwits | 티커·코인 주제에서 자동 |
| arXiv · Techmeme · Yahoo Finance | **무료 CLI**(첫 실행 설치, PATH 필요) |
| X · YouTube · TikTok · Instagram · Threads · Pinterest · LinkedIn | 키 또는 로그인 필요 (ScrapeCreators는 10,000콜 무료 후 유료) |

## 실전 가치 — 프롬프트 규칙으로 재사용

- **출력 계약 LAW 1~11**: 인용은 문장 안에(중복 `Sources:` 목록 금지), 가짜 제목 줄 금지, em/en 대시 금지, 본문 `##` 헤더 금지, 엔진 푸터 그대로 전달, 근거 없는 순위 클러스터 노출 금지, 고유명사 주제는 계획(`--plan`) 필수, 호스트별 인용 표기, 커뮤니티 인용 우선, **1차(당사자) 글을 1급 근거로**, 발견·트렌드 판정은 호스트가 직접.
- **제출 전 자기 점검 9항**과 "증거 없는 항목은 만들어 내지 말고 부족하다고 말한다"는 원칙은 우리 브리핑에도 그대로 쓸 수 있습니다.
- 라이브러리(로컬 SQLite)·HTML 브리프·Atom 피드·`ht-ml.app` 게시 같은 부가 기능은 **게시는 명시적 옵트인**이라고 적혀 있습니다.

## ⚠️ 주의사항

⚠️ 주의사항: 240KB 파이썬 엔진(last30days.py) 및 scripts/(box_chrome_login.py 브라우저 쿠키 읽기 경로 포함)는 코드 감사 전 실행 금지이며, 유료 API(ScrapeCreators 등) 가입 권유·X/YouTube/TikTok 등 유료·로그인 확장 소스는 사용 범위에서 제외하고 무료 소스·프롬프트 워크플로만 참고하세요.
