# 개발 흐름 도구 참고

여기서 하네스는 계획·실행·검증을 연결하는 개발 흐름 도구를 넓게 가리킨다. 아래 프로젝트들은 독립 에이전트 실행기와 완전히 같은 종류가 아니다. 현재 워크벤치는 가벼운 문서 흐름을 기본으로 유지한다. 목록에 있다고 설치되거나 활성화되는 것은 아니다.

## 비교와 선택

| 도구 | 추가 가치 | 기본 방식과 차이 | 적합한 상황 | 부담·중복 판단 |
|---|---|---|---|---|
| OpenSpec | 변경별 제안·요구사항 시나리오·설계·작업 목록 | 대화와 수동 기록을 변경 단위 산출물로 관리 | 기존 앱을 계속 고치며 요구사항이 자주 바뀔 때 | 정본 경로가 이중화되지 않게 해야 함. 초기 설정·학습 시간 추가 |
| GitHub Spec Kit | 명세 기반 과정·템플릿·에이전트 통합 | 반복 가능한 명세→계획→작업→구현 흐름 | 오래 유지할 제품·팀 프로젝트 | 기존 템플릿과 중복이 큼. 설정·문서 관리 비용 검토 |
| Superpowers | 계획·TDD·디버깅·검증 스킬의 개발 방법론 | 단계별 스킬 사용과 리뷰 흐름을 묶음 | 여러 단계의 개발을 반복하는 프로젝트 | 현재 지침과 중복, 자동 발동·관련 스킬·하위 에이전트 요구 확인 |

이 표의 적합성과 부담은 원문을 바탕으로 한 판단이다. 설치·실행·시간 절감은 측정하지 않았다. 짧은 작업에서는 기존 프롬프트가 더 적은 준비로 끝날 수 있고, 장기 작업에서는 변경 추적과 인계 비용을 줄일 가능성이 있다. 세 도구를 동시에 기본 활성화하지 않는다.

## OpenSpec

- [저장소와 공식 안내](https://github.com/Fission-AI/OpenSpec), [라이선스](https://github.com/Fission-AI/OpenSpec/blob/main/LICENSE): MIT 원문 확인.
- README는 Codex 통합과 변경 단위 Markdown 산출물을 설명한다. 바이너리 설치와 npm 설치 경로가 있으며 npm 경로는 Node.js 20.19.0 이상을 요구한다. 모든 설치 방식이 Node를 요구하는 것은 아니다.
- 초기화·명령 생성·자동 인식은 현재 환경에서 검증하지 않았다. 설치 안내가 외부 스크립트 실행을 제안하더라도 이번 정리에서는 실행하지 않았다.
- 도입한다면 프로젝트 지정 경로를 조사하고, OpenSpec 산출물과 기존 REQUIREMENTS·STATUS 중 각 정보의 정본을 하나로 정한다. 같은 내용을 두 문서에서 따로 편집하지 않는다.

## GitHub Spec Kit

- [저장소](https://github.com/github/spec-kit), [Codex 통합 문서](https://github.com/github/spec-kit/blob/main/docs/integrations/codex.md), [라이선스](https://github.com/github/spec-kit/blob/main/LICENSE): MIT 원문 확인.
- README 기준 Python 3.11+, uv, 지원 코딩 에이전트가 필요하다. Codex 통합은 프로젝트에 스킬을 생성하는 방식을 설명한다.
- 버전에 따라 초기화 인수·호출 문법·생성 경로가 바뀔 수 있다. 연결된 최신 문서와 실제 도움말을 확인한 뒤 적용한다. 현재 환경에서 명령을 실행하지 않았다.
- 프로젝트 설정·이벤트 처리·추가 확장을 한 번에 도입하지 않는다. 기존 작업 원칙과 겹치는 항목을 비교한 뒤 필요한 과정 하나부터 선택한다.

## Superpowers

- [저장소](https://github.com/obra/superpowers), [라이선스](https://github.com/obra/superpowers/blob/main/LICENSE): MIT 원문 확인.
- README는 요구사항 대화·계획·TDD·구현·리뷰 흐름과 Codex 통합 경로를 안내한다. 실제 클라이언트 지원·설정·자동 발동은 미검증이다.
- 전체 구성은 일부 흐름에서 하위 에이전트·다른 스킬·별도 기록 위치를 사용한다. 현재 권한·사용자의 실행 방식·비용 제한을 먼저 확인한다.
- 현재 워크벤치와 많이 겹친다. 당장 전체 도입을 기본값으로 삼지 않고, 아래 보조 지침의 추가 가치가 있을 때 참고한다.

## 보조 지침 두 가지

| 지침 | 언제 유용한가 | 현재 지침과 겹치는 부분 | 선택 기준 |
|---|---|---|---|
| [writing-plans](https://github.com/obra/superpowers/blob/main/skills/writing-plans/SKILL.md) | 계획을 다른 구현 세션에 넘길 때 | PROMPTS 5의 계획 수립 | 파일·인터페이스·작업별 검증 정보가 빠질 때만 추가 참고 |
| [verification-before-completion](https://github.com/obra/superpowers/blob/main/skills/verification-before-completion/SKILL.md) | 완료 보고 전 근거를 확인할 때 | PROMPTS 10·CHECKLIST | 완료 주장과 실제 실행 근거가 자주 어긋날 때 참고 |

두 SKILL.md 본문과 저장소 MIT 원문을 확인했다. writing-plans의 TDD·커밋·관련 스킬 참조, verification-before-completion의 엄격한 재검증 요구는 현재 프로젝트의 작업 규모·검증 기준과 비교해야 한다. 원문 일부만 참고했다면 전체 스킬 절차를 수행했다고 기록하지 않는다.

## 도입 전 최소 확인

먼저 기본 방식으로 충분한지 판단한다. 도입할 하나를 정한 뒤 원본 버전, 필요한 파일·설정 변경·의존성·권한, 실패 시 기본 방식으로 돌아갈 방법을 확인한다. 원본 main 링크는 변경될 수 있으며 이번 조사에서 커밋 SHA는 고정하지 않았다. 설치와 실행을 검증했다고 표현하지 않는다.
