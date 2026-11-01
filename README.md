# AI 협업 워크벤치

요구사항 정리부터 구현, 오류 해결, 검증, 보고까지 AI와 함께 작업하는 매뉴얼이다. 기존 역할 분리와 가벼운 문서 흐름을 유지하며, 처음에는 [START.md](START.md)만 읽고 접근 확인부터 시작한다.

| 파일 | 용도 |
|---|---|
| [START.md](START.md) | 첫 조사와 다음 행동 |
| [AGENTS.md](AGENTS.md) | 공통 작업 원칙 |
| [WORKFLOW.md](WORKFLOW.md) | 단계별 판단과 기록 경로 |
| [PROMPTS.md](PROMPTS.md) | 상세 마스터 프롬프트와 짧은 후속 요청 |
| [COMMANDS.md](COMMANDS.md) | 입력 위치별 명령 안내 |
| [CHECKLIST.md](CHECKLIST.md) | 검증·저장·인계 점검 |
| [SKILL_CATALOG.md](SKILL_CATALOG.md) | 작업별 외부 스킬 8개 비교 |
| [HARNESS_CATALOG.md](HARNESS_CATALOG.md) | 개발 흐름 도구와 보조 지침 |
| [templates/REQUIREMENTS.md](templates/REQUIREMENTS.md) | 요구사항 양식 |
| [templates/DECISIONS.md](templates/DECISIONS.md) | 결정 양식 |
| [templates/STATUS.md](templates/STATUS.md) | 정본 경로와 상태 양식 |
| [templates/VERIFICATION.md](templates/VERIFICATION.md) | 실행·수동 확인 양식 |
| [templates/MVP_REPORT.md](templates/MVP_REPORT.md) | 진행 중 근거 누적·결과 보고 양식 |
| [examples/request-tracker-walkthrough.md](examples/request-tracker-walkthrough.md) | 가상 작업 흐름 |
| [references/SOURCES.md](references/SOURCES.md) | 공개 원문·라이선스·확인 범위 |
| [.gitignore](.gitignore) | 로컬 기록과 비밀 파일 제외 보조 |

## 짧은 시작 요청

기획 담당 시작(참고 폴더 경로를 모르면 URL부터 전달):

```text
너는 기획 담당이야. https://github.com/ryurujxx/ai-workbench 의 START.md를 읽을 수 있는지 먼저 확인하고, 읽을 수 있으면 그 절차에 따라 현재 프로젝트를 수정 없이 조사해줘. 별도 폴더가 필요하면 허용된 작업공간 안에서만 사용해.
```

구현 담당 시작:

```text
너는 구현 담당이야. 프로젝트 [실제 경로]와 참고 폴더 [실제 경로]의 접근 여부를 먼저 확인해. START.md를 읽을 수 있으면 따르고, 읽을 수 없으면 아래 복사된 핵심 지침과 인계 묶음을 정본 기록에 반영한 뒤 구현·검증해줘. [핵심 지침] [확정 인계 묶음]
```

클론 위치가 허용되지 않으면 제한을 우회하지 않는다. 외부 참고 폴더는 편의 수단일 뿐 필수 런타임 의존성이 아니다. 접근할 수 없으면 [START.md의 복사·전달용 핵심 지침](START.md#복사전달용-핵심-지침)과 확정 인계 묶음을 대화에 붙여 넣고, 실제 정본은 접근 가능한 프로젝트 작업공간 안에 둔다. 기존 참고 폴더가 있으면 출처·내용·로컬 변경을 먼저 확인하고 덮어쓰기·중복 클론을 하지 않는다.
