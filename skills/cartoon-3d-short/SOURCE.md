# 출처 · 검증 기록 — cartoon-3d-short (저장소 이름: Claude Animated Shorts)

| 항목 | 내용 |
|---|---|
| 원출처 | [https://github.com/mromidev/claude-animated-shorts](https://github.com/mromidev/claude-animated-shorts) |
| 원본 경로 | `SKILL.md` (**원문 전체**, frontmatter `name: cartoon-3d-short`) |
| 원본 커밋 | `e3b817b6afc6cd413466d43f11ba31209e034bbf` (2026-11-01) |
| 라이선스 | **MIT** — Copyright (c) 2026 Mr omi — [`LICENSES/cartoon-3d-short-LICENSE.txt`](../../LICENSES/cartoon-3d-short-LICENSE.txt) (원본 `LICENSE` 1,063B) |
| 스타 | ⭐ 4,256 (2026-11-20 `gh api` 확인) |
| 저장(검증)일 | **2026-11-20** (창현 님 승인: 텔레그램 1664번 "딱히 이상없으면 기록해") |

> 폴더명은 원저장소 이름(`claude-animated-shorts`)이 아니라 **스킬 자신의 이름(`cartoon-3d-short`)** 을 따랐습니다. 이 저장소의 다른 스킬(`last30days`, `prompt-master`)과 같은 규칙이고, `SKILL.md` frontmatter의 `name`과 폴더명이 일치해야 클로드가 자동 인식합니다.

## 원문 보존

`SKILL.md` **166줄 15,131B를 한 글자도 수정하지 않고** 올렸습니다(md5 `ce9a309e0aa58082fd1a46049fcf3d8d` 대조 일치). 이 폴더에는 `SKILL.md`와 이 `SOURCE.md` 두 파일만 있습니다.

## 이 저장소에 넣은 것 / 넣지 않은 것

| 원본 파일 | 등록 | 비고 |
|---|---|---|
| `SKILL.md` (15,131B) | ✅ | 11단계 파이프라인(사실→대본→음성→샷 플랜→월드→캐릭터→포스트→사운드→룩 검사→최종 렌더→전달) + 최종 룩 수치 + 함정 목록 |
| `templates/bridge/` — 브리지 쇼츠 실제 소스(world·characters·ink·lens·grade·story) | ❌ | **빼면 이 스킬은 그대로 돌지 않습니다.** 원출처에서 함께 받아야 합니다 |
| `templates/audio/` · `templates/scripts/` (stills·sbs_sheet·merge·QA) | ❌ | 실행 코드 |
| `references/STYLE_BIBLE.md` · `reports/` 7종(545줄 상당) · `frames/` 38장 · `sheets/` 20장(1,200프레임, 합계 18MB) | ❌ | **스타일 학습용 참고 자료** — 원저작자도 "style study only"로 한정 |
| `README.md` | ❌ | 설치·구성 안내 |

## 검증 범위 (2026-11-20 · 1차 안전 확인)

- `SKILL.md` 본문 **전수 열람**: 지침·수치 문서이며, 이 파일 안에 실행 코드나 외부 호출은 **0건**입니다. 언급되는 실행 경로는 모두 로컬 명령(`npx remotion render`, `node scripts/*.mjs`, `python scripts/*.py`)과 사용자가 따로 준비하는 음성 파일입니다.
- `README.md` **열람**: 설치 요건(Remotion + `@remotion/three`, Node, Python 3, ffmpeg)과 `public/` 복사·임시 폴더 주의를 확인했습니다.
- `references/`·`templates/`·`scripts/`는 **열람하지 않았고 등록하지도 않았습니다.**
- → **검사 범위 내 의심 동작 0건**입니다. **저장소 전체(98개 파일) 감사나 렌더 실행 검증을 하지 않았습니다.**

## 무슨 스킬인가 — 세로 스토리 쇼츠 제작 파이프라인

| 요소 | 내용 |
|---|---|
| 결과물 | 55~70초 세로 쇼츠(1080x1920 30fps → 최종 2K 1440x2560), 2D 빈대머리 캐릭터 + 3D 페인티드 배경 + 먹선 |
| 도구 | **three.js를 Remotion 안에서** 렌더, **AI 영상 생성기 미사용**, 로컬 렌더 |
| 대본 공식 | 훅 → 배경 → 3단 고조 → 붕괴 → 데드팬 두 줄 → 생활 비유로 설명 → 결과 규칙 → 콜백 |
| 음성 | **별도 준비** — 녹음 또는 생성한 `voice.wav` + 단어 타임스탬프 `words.json`을 직접 손보정 |
| 사운드 | 합성 SFX + 오리지널 행진곡, 음악 +3dB / SFX −6dB / 음성 그대로 |

## 이 저장소에서 쓸 때

- **ASMR 채널(`Soneuli ASMR`)용이 아닙니다.** 스토리·내레이션이 있는 별도 쇼츠 후보로만 검토하세요. ASMR은 Google Flow 쪽 파이프라인을 씁니다.
- 이 폴더만 복사하면 `templates/bridge/`가 없어 렌더가 불가능합니다. 실제 제작은 원출처 전체 클론이 전제입니다.

## ⚠️ 주의사항

⚠️ 주의사항: ASMR 영상용이 아니라 **스토리 쇼츠(55~70초·내레이션·음성 별도 준비)** 후보이며, 원출처 `templates/`·`scripts/`를 함께 받아야만 동작합니다. Remotion은 번들마다 `public/`(약 1.3GB)를 임시 폴더로 복사하므로 **디스크 여유를 확인하고 `TEMP`/`TMP`를 큰 드라이브로 지정**해야 하며(원저작자도 60GB 이상 차서 렌더가 죽었다고 기록), 2K 렌더는 약 4fps로 67초 영상에 **10분 내외** 걸립니다. `references/`의 참고 프레임·콘택트시트는 **스타일 학습용**이므로 그대로 복사·업로드·공개하지 말고, 스토리·캐릭터·음성은 반드시 직접 만드세요. 1차 안전 확인(SKILL.md·README 읽은 범위 내 의심 동작 0건)만 했고 전체 코드 감사·실행 검증은 하지 않았습니다.
