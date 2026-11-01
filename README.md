# AI 협업 워크벤치

요구사항 정리부터 구현, 오류 해결, 검증, 보고까지 AI와 함께 작업하는 매뉴얼이다. 기존 역할 분리와 가벼운 문서 흐름을 유지하며, 시간제한 환경에서는 **확정 즉시 구현, 구현 즉시 검증, 의사결정 즉시 기록**을 적용한다. 처음에는 [START.md](START.md)만 읽고 접근·권한·시간 확인부터 시작한다.

| 파일 | 용도 |
|---|---|
| [START.md](START.md) | 첫 조사, 세 세션 운영과 다음 행동 |
| [AGENTS.md](AGENTS.md) | 공통 작업 원칙 |
| [WORKFLOW.md](WORKFLOW.md) | 단계별 판단과 기록 경로 |
| [PROMPTS.md](PROMPTS.md) | 상세 마스터 프롬프트와 짧은 후속 요청 |
| [COMMANDS.md](COMMANDS.md) | 입력 위치별 명령 안내 |
| [CHECKLIST.md](CHECKLIST.md) | 검증·저장·인계 점검 |
| [SKILL_CATALOG.md](SKILL_CATALOG.md) | 작업별 외부 스킬 8개 비교 |
| [HARNESS_CATALOG.md](HARNESS_CATALOG.md) | 개발 흐름 도구와 보조 지침 |
| [templates/REQUIREMENTS.md](templates/REQUIREMENTS.md) | 요구사항 양식 |
| [templates/DECISIONS.md](templates/DECISIONS.md) | 결정 양식 |
| [templates/STATUS.md](templates/STATUS.md) | 단일 최신 진행 상태·시간·복구 양식 |
| [templates/VERIFICATION.md](templates/VERIFICATION.md) | 실행·수동 확인 양식 |
| [templates/MVP_REPORT.md](templates/MVP_REPORT.md) | 진행 중 근거 누적·결과 보고 양식 |
| [examples/request-tracker-walkthrough.md](examples/request-tracker-walkthrough.md) | 가상 작업 흐름 |
| [references/SOURCES.md](references/SOURCES.md) | 공개 원문·라이선스·확인 범위 |
| [.gitignore](.gitignore) | 로컬 기록과 비밀 파일 제외 보조 |

## 짧은 시작 요청

실전에서는 같은 프로젝트 경로에서 터미널 세 개를 열고 각 터미널에서 `codex`를 실행한다. 구현 세션을 먼저 시작해 정본 STATUS와 시간·제출 조건을 초기화한 뒤 기획·테스트 세션을 연결한다. 전체 명령과 프롬프트는 [COMMANDS.md의 세 터미널 실전 실행](COMMANDS.md#세-터미널-실전-실행)을 사용한다.

기획 담당 시작:

```text
너는 기획 담당이야. 프로젝트와 최신 STATUS를 읽기 전용으로 확인하고 START.md를 따라 조사해. 독립적으로 확정된 요구사항은 ID·버전·H-ID 패킷으로 즉시 출력하고 나머지 분석을 계속해. 파일은 수정하지 마.
```

구현 담당 시작:

```text
너는 구현 담당이자 코드·정본의 단일 작성자야. 프로젝트·참고 문서·시간·평가·제출 조건을 확인하고 START.md를 따라 기존 STATUS를 복원하거나 없을 때만 초기화해. 전달받은 최신 ID·버전의 독립 요구사항부터 전체 기획을 기다리지 말고 구현·자체 검증한 뒤 구현 완료/미검증으로 테스트에 넘겨.
```

테스트 담당 시작:

```text
너는 테스트 담당이야. 프로젝트와 최신 STATUS를 읽기 전용으로 확인하고 구현 완료/미검증인 ID·버전부터 독립 검증해. T-ID 결과 패킷을 출력하고 코드·정본은 수정하지 마.
```

클론 위치가 허용되지 않으면 제한을 우회하지 않는다. 외부 참고 폴더는 편의 수단일 뿐 필수 런타임 의존성이 아니다. 접근할 수 없으면 [START.md의 복사·전달용 핵심 지침](START.md#복사전달용-핵심-지침), 최신 STATUS 요약과 H/T 패킷을 대화에 붙여 넣고, 실제 정본은 접근 가능한 프로젝트 작업공간 안에 둔다. 세 세션 대화는 자동 공유되지 않으며 코드와 정본은 구현 세션 하나만 수정한다.
