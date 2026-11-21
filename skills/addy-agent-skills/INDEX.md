# INDEX — Addy Osmani Agent Skills 26종

> 이 파일은 이 저장소에서 만든 **안내용 목차**입니다(원문 아님). 원문·라이선스·검증 범위는 [`SOURCE.md`](SOURCE.md)에 있습니다.

수명주기 25종 + 메타 1종. 각 폴더에 원출처 `SKILL.md`가 한 글자도 고치지 않은 채 들어 있습니다. 공용 참조 문서는 [`references/`](references/)에 함께 두었습니다.

| # | 스킬 | 단계 | 쓰는 때 |
|---|---|---|---|
| 1 | [`using-agent-skills`](using-agent-skills/) | 메타 | 세션을 시작할 때, 어느 스킬·워크플로가 지금 작업에 맞는지 고를 때 |
| 2 | [`interview-me`](interview-me/) | 시작 | 요청이 흐릴 때 — 한 번에 질문 하나씩, 약 95% 확신까지 사용자의 진짜 목적을 캐낼 때 |
| 3 | [`idea-refine`](idea-refine/) | 시작 | 아이디어가 아직 뭉갤 때 — 발산·수렴으로 날카롭게 다듬을 때 |
| 4 | [`spec-driven-development`](spec-driven-development/) | 설계 | 새 프로젝트·기능을 코드 전에 스펙(PRD/요구사항)으로 확정할 때 |
| 5 | [`planning-and-task-breakdown`](planning-and-task-breakdown/) | 설계 | 스펙은 있는데 작업이 너무 커 보일 때 — 순서 있는 구현 단위로 쪼갤 때 |
| 6 | [`constraint-driven-development`](constraint-driven-development/) | 설계 | 프로젝트 품질 기준을 문서 계약으로 고정하고, 에이전트가 몰래 기준을 낮추지 못하게 할 때 |
| 7 | [`api-and-interface-design`](api-and-interface-design/) | 설계 | REST/GraphQL 엔드포인트, 모듈 경계, 공개 인터페이스를 정할 때 |
| 8 | [`context-engineering`](context-engineering/) | 설계 | 새 세션을 열 때, 출력 품질이 떨어질 때, 작업을 바꿀 때 컨텍스트를 다시 짤 때 |
| 9 | [`incremental-implementation`](incremental-implementation/) | 구현 | 여러 파일을 건드리는 변경을 얇고 검증 가능한 조각으로 나눠 붙일 때 |
| 10 | [`test-driven-development`](test-driven-development/) | 구현 | 로직·버그 수정·동작 변경 — red-green-refactor로 진행할 때 |
| 11 | [`debugging-and-error-recovery`](debugging-and-error-recovery/) | 구현 | 테스트 실패·빌드 깨짐·어제 되던 게 안 될 때 — 근본 원인부터 찾을 때 |
| 12 | [`doubt-driven-development`](doubt-driven-development/) | 구현 | 쉬운 결정이 아닐 때 — 새 컨텍스트로 가정을 적대적으로 재검토할 때 |
| 13 | [`source-driven-development`](source-driven-development/) | 구현 | 구현 전에 공식 문서로 접근이 맞는지 확인해야 할 때 |
| 14 | [`code-simplification`](code-simplification/) | 정리 | 동작은 그대로 두고 읽기 쉽게(refactor) 정리할 때 — 코드가 돌긴 하는데 손대기 어려울 때 |
| 15 | [`code-review-and-quality`](code-review-and-quality/) | 검토 | 병합 전 — 내 코드든 다른 에이전트·사람 코드든 여러 축으로 리뷰할 때 |
| 16 | [`security-and-hardening`](security-and-hardening/) | 검토 | 입력 처리·인증·데이터 저장·외부 호출을 다룰 때 취약점을 막을 때 |
| 17 | [`accessibility-engineering`](accessibility-engineering/) | 검토 | 화면·컴포넌트를 WCAG 2.2 AA로 감사하고 위반을 고칠 때 |
| 18 | [`browser-testing-with-devtools`](browser-testing-with-devtools/) | 검토 | 브라우저에서 도는 것을 실제 브라우저(Chrome DevTools MCP)로 확인할 때 |
| 19 | [`performance-optimization`](performance-optimization/) | 검토 | 성능 요구가 있거나 느려진 느낌이 들 때 — 프론트·백엔드·쿼리·DB |
| 20 | [`observability-and-instrumentation`](observability-and-instrumentation/) | 운영 | 로그·메트릭·트레이스·알림을 넣어 운영 중 동작을 보이게 할 때 |
| 21 | [`frontend-ui-engineering`](frontend-ui-engineering/) | 구현 | 화면·컴포넌트·레이아웃을 실제 제품 수준(접근성·반응형)으로 만들 때 |
| 22 | [`documentation-and-adrs`](documentation-and-adrs/) | 운영 | 설계 결정(ADR)을 기록할 때, 문서가 코드와 어긋난 것을 발견했을 때 |
| 23 | [`git-workflow-and-versioning`](git-workflow-and-versioning/) | 운영 | 커밋·브랜치·충돌 해결·엉킨 변경 분리 |
| 24 | [`ci-cd-and-automation`](ci-cd-and-automation/) | 운영 | 빌드·배포 파이프라인, 품질 게이트, 테스트 러너를 붙일 때 |
| 25 | [`deprecation-and-migration`](deprecation-and-migration/) | 운영 | 구 시스템·API·기능을 걷어내고 사용자를 새 구현으로 옮길 때 |
| 26 | [`shipping-and-launch`](shipping-and-launch/) | 출시 | 배포 전 — 출시 전 점검 목록과 준비 상태를 확인할 때 |

## 폴더 구조

```
skills/addy-agent-skills/
├── INDEX.md          # 이 파일 (안내용, 원문 아님)
├── SOURCE.md         # 출처·커밋·라이선스·검증 범위
├── references/       # 26종이 공통으로 참조하는 문서 7개 (원문)
└── <26개 스킬 폴더>/
    └── SKILL.md      # 원출처 원문 그대로
```

## 참고

- 원출처의 `hooks/`(세션 시작·파일 저장 훅 셸 스크립트), `scripts/`, `commands/`는 **수록하지 않았습니다**. 설치 전 별도 검토가 필요하다는 판단은 [`SOURCE.md`](SOURCE.md)에 적었습니다.
- 원저장소는 Addy Osmani(구글 크롬 엔지니어링 리드)의 실전 개발 워크플로 스킬팩이며, MIT 라이선스입니다.
