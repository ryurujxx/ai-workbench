# 공개 출처와 라이선스 확인 범위

이 워크벤치의 운영 문서와 STUDY 양식은 저장소 자체 지침이다. 아래 외부 자료는 이전 도구 조사와 명령 설명에서 참고했으며, 외부 저장소의 코드·스킬·템플릿은 이 저장소에 포함하지 않는다. 링크된 원문을 복제·배포할 때는 해당 버전의 라이선스와 고지를 다시 확인해야 한다.

| 출처 | 확인한 용도 | 라이선스·제한 |
|---|---|---|
| [OpenAI Skills](https://github.com/openai/skills) | notebook, browser, PDF, security 작업 지침 조사 | notebook·browser의 [Apache-2.0 원문](https://github.com/openai/skills/blob/main/skills/.curated/playwright/LICENSE.txt) 확인, 다른 항목은 각 원문 재확인 필요 |
| [Anthropic Skills](https://github.com/anthropics/skills) | frontend-design 지침 조사 | 해당 지침의 [Apache-2.0 원문](https://github.com/anthropics/skills/blob/main/skills/frontend-design/LICENSE.txt) 확인, 저장소 전체에 동일 조건을 가정하지 않음 |
| [Superpowers](https://github.com/obra/superpowers) | debugging, planning, verification 흐름 조사 | [MIT 원문](https://github.com/obra/superpowers/blob/main/LICENSE) 확인 |
| [Vercel Agent Skills](https://github.com/vercel-labs/agent-skills) | 웹 UI·React 검토 지침 조사 | 항목별 라이선스·연결 규칙 재확인 필요 |
| [OpenSpec](https://github.com/Fission-AI/OpenSpec) | 변경 단위 명세 흐름 조사 | [MIT 원문](https://github.com/Fission-AI/OpenSpec/blob/main/LICENSE) 확인 |
| [GitHub Spec Kit](https://github.com/github/spec-kit) | 명세 기반 개발 흐름 조사 | [MIT 원문](https://github.com/github/spec-kit/blob/main/LICENSE) 확인 |
| [OpenAI 개발자 명령](https://learn.chatgpt.com/docs/developer-commands?surface=cli) | Codex 입력란과 셸 명령 구분 | 공식 설명 참고, 로컬 실행 검증과 구분 |

선택형 Skill 라이브러리는 기존 WORKFLOW를 기준으로 독자 작성했다. 데이터의 의미·조인 점검은 [hephee r2-data](https://github.com/hephee/hynix-r2-skillset/blob/main/.agents/skills/r2-data/SKILL.md)와 [cofa-toolkit data-quality](https://github.com/B0neh3ad/cofa-toolkit/blob/main/skills/data-quality/SKILL.md), 가설을 분리한 원인 추적은 [cofa-toolkit systematic-debugging](https://github.com/B0neh3ad/cofa-toolkit/blob/main/skills/systematic-debugging/SKILL.md)의 일반 기법을 참고했다. 외부 Skill 본문·코드·양식은 포함하지 않았고, 모든 오류에 강제 적용하거나 고정 재시도 횟수를 요구하는 방식도 채택하지 않았다. 이전에 검토한 [cofa-starter](https://github.com/Iremos/cofa-starter)의 작은 정답·불변조건·다른 경로 검산 아이디어는 기존 WORKFLOW와 함께 검토했다.

저장 경로 판단과 `name`/`description` 형식은 [OpenAI 공식 Skill 안내](https://learn.chatgpt.com/docs/build-skills)를 확인했다. 공식 문서의 탐색 규칙과 실제 Cofa IDE의 호환성 검증은 별개다. `skills/` 직접 읽기를 기본으로 배포하며 자동 등록·하위 에이전트 동작은 검증하지 않았다.

위 도구의 설치·실행 호환성이나 시간 절감 효과는 이 저장소에서 보증하지 않는다. 외부 자료는 환경 정책이 허용할 때만 반입하고, 공개 자료 반입 허용을 내부 자료 반출 허용으로 해석하지 않는다.
