# AI 협업 워크벤치

요구사항 정리부터 구현, 오류 해결, 검증, 보고까지 AI와 함께 작업하는 매뉴얼이다. 처음에는 [START.md](START.md)를 읽고 필요한 문서만 선택한다.

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
| [templates/MVP_REPORT.md](templates/MVP_REPORT.md) | 결과 보고 양식 |
| [examples/request-tracker-walkthrough.md](examples/request-tracker-walkthrough.md) | 가상 작업 흐름 |
| [references/SOURCES.md](references/SOURCES.md) | 공개 원문·라이선스·확인 범위 |
| [.gitignore](.gitignore) | 로컬 기록과 비밀 파일 제외 보조 |

## 짧은 시작 요청

기획 담당 시작:

```text
너는 기획 담당이야. https://github.com/ryurujxx/ai-workbench 를 허용된 작업공간 안의 현재 프로젝트 밖 별도 폴더에 클론하고 START.md에 따라 초기 조사해줘. 프로젝트 파일은 수정하지 마.
```

구현 담당 시작:

```text
너는 구현 담당이야. 참고 폴더 [실제 경로]의 START.md에 따라 아래 확정 요청을 구현·검증해줘. [확정 요청]
```

클론 위치가 허용되지 않으면 제한을 우회하지 않고 허용 위치를 확인한다. 기존 참고 폴더가 있으면 출처·내용·로컬 변경을 먼저 확인하고 덮어쓰기·중복 클론을 하지 않는다.
