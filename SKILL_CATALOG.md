# 외부 스킬 선별

확인일 2026-10-31. 작업별 후보는 8개다. 추가 후보의 확인 범위와 미확인 사항은 각 항목 및 SOURCES에 구분했다. 각 원본 지침을 확인했으며 설치·스크립트 실행·효율 측정은 하지 않았다. 모든 후보의 실행 호환성은 미검증, 시간 절감은 미측정이다. main 링크는 변할 수 있고 조회 날짜는 버전 고정이 아니다. 커밋 SHA는 확인하지 못했다.

기본 Codex와 [AGENTS.md](AGENTS.md)·[WORKFLOW.md](WORKFLOW.md)로 충분하면 추가 도구를 쓰지 않는다. 후보 선택 후에만 [PROMPTS.md](PROMPTS.md)의 7번으로 필요한 파일과 권한을 확인한다.

## 1. jupyter-notebook: 반복 가능한 데이터 탐색

- [원본 지침](https://github.com/openai/skills/blob/main/skills/.curated/jupyter-notebook/SKILL.md), [라이선스](https://github.com/openai/skills/blob/main/skills/.curated/jupyter-notebook/LICENSE.txt): Apache-2.0.
- 작업: 데이터 분석·탐색·교육용 노트북을 구조화한다. 일반 지침에 없는 노트북 생성 자산이 있어 우선 검토한다.
- 차이와 자산: 실험/튜토리얼 템플릿 2개, new_notebook.py 생성기, 패턴·구조·품질 참조 문서. 생성기 원문을 읽어 템플릿 로딩을 확인했다.
- 의존성: 생성기는 Python 표준 라이브러리 사용. 셀 실행에는 실제 커널과 분석 패키지가 필요하다. 데이터·API 접근은 작업별 권한을 확인한다.
- 비용·충돌: 낮음~중간으로 추정, 미측정. 원문 기본 설치·출력 경로는 현재 프로젝트 경로와 조정이 필요하다.
- 사용할 때: 노트북을 재실행·인계할 때. 사용하지 않을 때: 단순 일회성 계산이나 기존 스크립트로 충분할 때.
- 적용: 생성 자산이 필요하면 선택 파일 확보를 검토한다. 구조 원칙만 필요하면 원문 참고로 충분하다.

## 2. playwright: 실제 웹 흐름 확인

- [원본 지침](https://github.com/openai/skills/blob/main/skills/.curated/playwright/SKILL.md), [라이선스](https://github.com/openai/skills/blob/main/skills/.curated/playwright/LICENSE.txt): Apache-2.0.
- 작업: 실제 브라우저에서 입력·이동·오류를 재현한다. HTTP 검사만으로 부족한 UI 흐름에서 추가 가치가 있다.
- 차이와 자산: playwright_cli.sh 래퍼와 CLI·작업 흐름 참조 문서. 래퍼 원문에서 npx를 통한 패키지 호출을 확인했다.
- 의존성: bash, Node/npm/npx, 브라우저 런타임. 패키지와 브라우저 확보에 네트워크가 필요할 수 있고 로그인 서비스는 별도 인증·권한이 필요하다.
- 비용·충돌: 중간 이상으로 추정, 미측정. 원문은 CLI 중심이며 테스트 파일 작성 흐름과 다르다. 자동 조작·캡처는 현재 작업 정책이 허용할 때만 사용한다.
- 사용할 때: 재현해야 할 웹 흐름이 있고 도구 실행이 허용될 때. 사용하지 않을 때: UI가 없거나 수동 확인으로 충분하거나 환경 부담이 클 때.
- 적용: 이미 있는 브라우저 검증 도구를 먼저 사용한다. 이 래퍼의 도입은 필요한 경우에만 검토한다.

## 3. frontend-design: UI 시각 방향

- [원본 지침](https://github.com/anthropics/skills/blob/main/skills/frontend-design/SKILL.md), [라이선스](https://github.com/anthropics/skills/blob/main/skills/frontend-design/LICENSE.txt): Apache-2.0.
- 작업: 제품의 실제 주제·사용자에 맞는 색·서체·레이아웃을 선택한다.
- 차이와 자산: 이 워크벤치에 없는 시각 설계 관점. 이번 확인 범위에서는 실행 스크립트·완성 컴포넌트 자산을 확인하지 않았다.
- 의존성: 지침 읽기는 별도 인증 불필요. 폰트·이미지·구현 도구는 실제 프로젝트에 따라 네트워크와 라이선스 확인이 필요하다.
- 비용·충돌: 지침 참고는 낮음, 시각 반복 제작은 가변. 미측정. 표현 실험이 필수 동작·접근성·일정과 충돌하지 않게 범위를 정한다.
- 사용할 때: 새 UI의 일관된 시각 방향이 필요할 때. 사용하지 않을 때: 기존 디자인 시스템 준수가 우선이거나 화면이 없을 때.
- 적용: 설치 없이 원문 참고부터 시작한다.

## 4. systematic-debugging: 반복 오류의 심화 조사

- [원본 지침](https://github.com/obra/superpowers/blob/main/skills/systematic-debugging/SKILL.md), [라이선스](https://github.com/obra/superpowers/blob/main/LICENSE): MIT.
- 작업: 여러 계층에 걸친 재현·원인 추적·단일 가설 실험.
- 차이와 자산: 일반 흐름은 우리 지침과 중복되어 우선순위가 낮다. 원문에 root-cause-tracing·defense-in-depth·condition-based-waiting 보조 자료가 연결돼 있다. 보조 자료·스크립트 전체는 이번에 검증하지 않았다.
- 의존성: 문서 참고 자체는 낮음. 실제 진단 명령은 프로젝트에 따르며 다른 superpowers 스킬 참조도 있다.
- 비용·충돌: 조사 깊이에 따라 증가, 미측정. 원문의 엄격한 순서와 다른 스킬 요구는 작은 수정에 과할 수 있다.
- 사용할 때: 반복 수정이 실패하고 계층별 증거가 부족할 때. 사용하지 않을 때: 명확한 오탈자·단순 원인 또는 현재 지침으로 해결되는 경우.
- 적용: 필요한 보조 지침만 읽는 선택을 우선한다. 일부만 적용했다면 전체 절차를 수행했다고 주장하지 않는다.

## 추가 후보 빠른 선택

아래 비용과 효과는 원문 구조에 따른 판단이며 실측하지 않았다. 기본 Codex도 같은 작업을 할 수 있다. 스킬의 가치는 별도 지침·참고 자료로 누락을 줄이는 데 있고, 소요 시간이 항상 줄어드는 것은 아니다. 후보를 모아둔 것과 설치·적용한 것은 다르다.

| 후보 | 기본 방식 | 추가되는 관점 | 추가 부담·예상 시간 영향 | 선택 조건 |
|---|---|---|---|---|
| web-design-guidelines | 일반 코드 리뷰와 수동 화면 확인 | 폼·키보드·포커스·빈 상태 등 UI 점검 기준 | 지침 확보·리뷰 시간이 추가되나 반복 누락 수정은 줄일 수 있음 | 실제 웹 UI의 주요 흐름을 점검할 때 |
| vercel-react-best-practices | 프로젝트 관례로 React 코드 작성 | 데이터 요청·번들·렌더링 관련 우선순위와 규칙 자료 | 관련 규칙만 읽으면 부담 낮음, 전면 최적화는 시간 증가 | React/Next.js가 이미 선택된 경우 |
| pdf | Python 도구로 추출·생성 | 페이지 렌더링을 통한 레이아웃 확인 절차 | 도구가 있으면 재작업 감소 가능, Poppler 설치가 필요하면 부담 증가 | PDF가 주요 입력·출력인 경우 |
| security-best-practices | 일반 기능 검증과 코드 리뷰 | 언어·프레임워크별 보안 참고 자료 | 검토·수정 시간이 추가됨, 시간 절감 목적의 상시 도구는 아님 | 명시적으로 보안 검토가 필요하고 지원 스택에 해당할 때 |

### 5. web-design-guidelines: 사용성·접근성 점검

- [원본 지침](https://github.com/vercel-labs/agent-skills/blob/main/skills/web-design-guidelines/SKILL.md), [실제 점검 규칙](https://github.com/vercel-labs/web-interface-guidelines/blob/main/command.md).
- 새 UI의 시각 방향을 정하는 frontend-design과 달리, 구현된 화면 코드의 사용성을 검토하는 후보다. 정적 코드 리뷰만으로 실제 화면 동작을 확인했다고 보고하지 않는다.
- 원문은 매 검토 시 외부 규칙을 새로 가져오도록 요구한다. SKILL.md 한 장만 읽어서는 점검 규칙 전체를 확보한 것이 아니다. 원문의 WebFetch 도구명이 현재 환경과 같다고 가정하지 않는다.
- 의존성: 원문·규칙을 읽을 수 있는 네트워크와 파일 접근. 정적 검토 자체에는 브라우저 자동 조작이 필요하지 않다. 실제 UI 검증은 허용된 도구 또는 사용자 수동 확인으로 별도 수행한다.
- 사용 범위: 핵심 입력·저장·오류 표시 화면부터 확인한다. 표현상의 권고를 업무 규칙보다 우선하거나 모든 권고를 무조건 구현하지 않는다.
- 확인 범위: SKILL.md와 외부 규칙 본문. 해당 자료의 적용 라이선스 원문은 이번에 확인하지 못했다. 링크로만 수록하며 복제·재배포용으로 채택하지 않는다.

### 6. vercel-react-best-practices: React 구현 검토

- [원본 지침](https://github.com/vercel-labs/agent-skills/blob/main/skills/react-best-practices/SKILL.md), [규칙 디렉터리](https://github.com/vercel-labs/agent-skills/tree/main/skills/react-best-practices/rules).
- React/Next.js의 요청 흐름·번들·렌더링 검토용이다. 이 스킬을 쓰려고 기존 프로젝트를 React로 변경하지 않는다.
- 지침은 규칙별 설명·코드 예시와 확장 AGENTS.md를 참조한다. 전체 참고 파일은 이번 조사에서 읽지 않았다. 실제 적용 시 현재 버전·문제와 관련 있는 규칙을 먼저 읽는다.
- 의존성: 문서 참고 자체는 낮음. 실제 빌드·측정에는 프로젝트의 Node 환경과 기존 검증 도구가 필요하다. 원문이 제안하는 라이브러리 추가를 자동 승인으로 취급하지 않는다.
- 라이선스: SKILL.md 메타데이터는 MIT로 표시한다. 별도 라이선스 사본과 관련 자산 조건은 복제 전에 확인해야 한다.
- 적용: 변경 대상 파일과 관련된 높은 영향 규칙부터 검토하고, 작은 화면에 필요 없는 성능 작업은 보류한다.

### 7. pdf: 문서 추출·생성·시각 확인

- [원본 지침](https://github.com/openai/skills/blob/main/skills/.curated/pdf/SKILL.md).
- PDF를 이미지로 렌더링해 잘림·겹침·표·글꼴을 확인하는 절차가 핵심이다. 텍스트 추출과 페이지 시각 검증을 구분한다.
- 의존성: 작업에 따라 pdfplumber/pypdf/reportlab, 페이지 렌더링은 Poppler의 pdftoppm. 실제 설치 상태·한글 폰트·문서 구조는 확인하지 않았다.
- 단순 MD 보고서만 필요하면 사용하지 않는다. OCR이 필요한 스캔 문서를 이 지침만으로 모두 판독할 수 있다고 가정하지 않는다.
- 확인 범위: SKILL.md 본문. 폴더별 라이선스 파일 접근에 실패해 라이선스는 미확인이다. 기존의 다른 OpenAI 스킬과 동일한 라이선스라고 추정하지 않는다. 링크 참고 후보로만 유지한다.

### 8. security-best-practices: 요청받은 보안 검토

- [원본 지침](https://github.com/openai/skills/blob/main/skills/.curated/security-best-practices/SKILL.md), [참고 자료 위치](https://github.com/openai/skills/tree/main/skills/.curated/security-best-practices/references).
- 원문 대상은 Python, JavaScript/TypeScript, Go다. 명시적인 보안 검토·안전한 기본 구현 요청에서 사용하며, 일반 디버깅마다 전체 보안 감사를 실행하지 않는다.
- 관련 언어·프레임워크의 참고 문서를 읽고 코드 위치와 근거를 연결한다. 심각도별 결과를 먼저 보고하고, 범위를 넓히는 수정을 임의로 시작하지 않는다.
- 의존성: 원문·참고 자료와 코드 접근. 이 스킬 자체가 자동 취약점 스캐너나 보안 인증은 아니다. 실제 검증 도구는 프로젝트별로 다르다.
- 확인 범위: SKILL.md 전체. 연결된 모든 보안 참고 자료·실행 명령은 미검증이며 적용 라이선스 원문도 이번에는 확인하지 못했다. 링크 참고 후보로만 유지한다.

## 제외 판단과 재사용

검증 전 완료 주장 방지·계획 작성은 현재 지침과 겹쳐 작업별 스킬 8개에는 넣지 않았다. 필요할 때 볼 보조 자료는 [HARNESS_CATALOG.md](HARNESS_CATALOG.md)에 따로 정리했다. 모음 사이트의 인기도나 설치 수는 품질 근거로 쓰지 않았다. 탐색·확인 범위는 [SOURCES.md](references/SOURCES.md)에 기록했다.

원본 파일은 이 폴더에 포함하지 않는다. 나중에 코드·템플릿·지침 원문을 복제·배포하면 해당 라이선스 사본과 저작권·NOTICE 등 필요한 고지를 유지하고 수정 표시를 확인한다. MIT와 Apache-2.0을 동일 조건으로 취급하지 않는다. 이 표는 원문을 대체하는 사용 허가서가 아니다.
