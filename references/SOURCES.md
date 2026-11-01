# 공개 출처와 확인 범위

확인일 2026-10-31. 문서의 협업 절차와 양식은 현재 요구에 맞춰 작성했으며 외부 스킬 비교는 아래 원문을 참고했다. 외부 저자의 스킬·코드·템플릿을 이 폴더에 재배포하거나 독자 제작 자산으로 표시하지 않는다.

## 탐색 출발점

| 출처 | 확인 범위 | 사용 방식 |
|---|---|---|
| [OpenAI Skills](https://github.com/openai/skills) | 저장소 개요와 아래 후보 원문 | 노트북·웹 검증 후보 탐색 |
| [Anthropic Skills](https://github.com/anthropics/skills) | 개요와 frontend-design 원문 | UI 지침 후보 |
| [Superpowers](https://github.com/obra/superpowers) | 개요와 systematic-debugging 원문 | 중복·심화 조사 판단 |
| [Awesome Copilot](https://github.com/github/awesome-copilot) | 공개 개요·구성 | 발견용, 본문 절차의 근거로 사용하지 않음 |
| [Awesome Agent Skills](https://github.com/VoltAgent/awesome-agent-skills) | 공개 개요·목록 | 발견용, 품질·실행 보증으로 쓰지 않음 |

## 직접 확인한 원문

- [jupyter-notebook/SKILL.md](https://github.com/openai/skills/blob/main/skills/.curated/jupyter-notebook/SKILL.md), [new_notebook.py](https://github.com/openai/skills/blob/main/skills/.curated/jupyter-notebook/scripts/new_notebook.py), [Apache-2.0 원문](https://github.com/openai/skills/blob/main/skills/.curated/jupyter-notebook/LICENSE.txt).
- [playwright/SKILL.md](https://github.com/openai/skills/blob/main/skills/.curated/playwright/SKILL.md), [playwright_cli.sh](https://github.com/openai/skills/blob/main/skills/.curated/playwright/scripts/playwright_cli.sh), [Apache-2.0 원문](https://github.com/openai/skills/blob/main/skills/.curated/playwright/LICENSE.txt).
- [frontend-design/SKILL.md](https://github.com/anthropics/skills/blob/main/skills/frontend-design/SKILL.md), [Apache-2.0 원문](https://github.com/anthropics/skills/blob/main/skills/frontend-design/LICENSE.txt).
- [systematic-debugging/SKILL.md](https://github.com/obra/superpowers/blob/main/skills/systematic-debugging/SKILL.md), [MIT 원문](https://github.com/obra/superpowers/blob/main/LICENSE).
- [OpenAI 개발자 명령](https://learn.chatgpt.com/docs/developer-commands?surface=cli): /status·/model 설명과 셸/입력란 구분에 참고.

확인한 main 링크는 이후 변경될 수 있다. 커밋 SHA는 확인하지 못했으며 날짜는 버전 고정을 뜻하지 않는다. 연결된 보조 문서와 모든 템플릿을 전부 읽거나 실행한 것은 아니다.

## 실행 확인의 범위

로컬 Codex의 버전·도움말 조회는 실행했으며 0.165.0과 Usage 출력을 확인했다. 임시 경로 권한 경고가 동반됐다. 대화 기능·스킬 자동 등록·프로젝트 실행·브라우저 검증은 미검증이다. 외부 키트·스킬 스크립트는 다운로드·설치·실행하지 않았다. 시간 절감은 측정하지 않았다.

검색 중 OpenAI 카탈로그의 추정 spreadsheet 경로는 404여서 후보로 채택하지 않았다. 접근하지 못한 원문을 확인했다고 표시하지 않는다.

## 추가 조사: 작업별 후보와 개발 흐름 도구

이번 추가 조사에서는 원문을 열어 확인한 범위를 아래에 기록했다. 이전 절의 확인 결과를 새로 실행한 것으로 바꾸지 않았다. 외부 원본 파일은 이 묶음에 포함하지 않는다.

| 출처 | 읽은 범위 | 남은 제한 |
|---|---|---|
| [web-design-guidelines](https://github.com/vercel-labs/agent-skills/blob/main/skills/web-design-guidelines/SKILL.md) 및 [command.md](https://github.com/vercel-labs/web-interface-guidelines/blob/main/command.md) | 지침 및 점검 규칙 본문 | 적용 라이선스 원문 미확인, 실행 안 함 |
| [react-best-practices](https://github.com/vercel-labs/agent-skills/blob/main/skills/react-best-practices/SKILL.md) | 지침 본문, 메타데이터 MIT 표시 | 규칙별 파일 전체·별도 라이선스 사본 미확인 |
| [pdf](https://github.com/openai/skills/blob/main/skills/.curated/pdf/SKILL.md) | 지침 본문 | 라이선스 파일 접근 실패, 패키지·렌더링 실행 안 함 |
| [security-best-practices](https://github.com/openai/skills/blob/main/skills/.curated/security-best-practices/SKILL.md) | 지침 본문 | 참고 자료 전체·라이선스 원문 미확인, 보안 검증 안 함 |
| [OpenSpec](https://github.com/Fission-AI/OpenSpec) | README와 MIT LICENSE | 설치·통합·확장·스크립트 전체 미검증 |
| [Spec Kit](https://github.com/github/spec-kit) | README, Codex 통합 문서, MIT LICENSE | 설치·설정·확장·실행 미검증 |
| [Superpowers](https://github.com/obra/superpowers) | README, writing-plans 및 verification-before-completion 본문, MIT LICENSE | 하위 스킬 전체·실행·클라이언트 호환성 미검증 |

추가 후보의 공식·원저자 저장소를 우선했다. 인기 수치·사용 후기·검증되지 않은 성능 주장을 효과의 근거로 삼지 않았다. 확인된 실제 운영 사례는 확보하지 못했으며, 효용 판단은 기능·부담·현재 문서와의 중복에 따른 판단이다. main 링크는 변경될 수 있고 커밋 SHA는 고정하지 않았다.

추정한 OpenAI spreadsheet·doc 경로는 유효한 본문을 확보하지 못해 추가하지 않았다. Anthropic 문서 스킬은 저장소 개요가 source-available과 일반 오픈소스 스킬을 구분하므로, 저장소 전체에 동일한 라이선스가 적용된다고 가정하지 않았다. 해당 문서 스킬 원본은 수록하지 않았다.
