# ESG Guide AI Agent
목적 : 복잡한 ESG 규제, 분석 및 계산 항목에 대한 처리에 어려움을 겪는 기업 실무자들을 위한 LangChain & RAG 파이프라인 기반 지능형 AI Agnet 설계

## 👨‍👧‍👦 Team 
<table align="center">
  <!-- 상단 팀원 이름 Table-->
  <tr>
    <th align="center">👑 이진성</th>
    <th align="center">🙍 고아연</th>
    <th align="center">🙍‍♂ 김재현</th>
    <th align="center">🙍‍♂ 박성재</th>
    <th align="center">🙍‍♂ 배준서</th>
    <th align="center">🙍 윤소정</th>
  </tr>
  
  <!-- 팀원 이미지 Table-->
  <tr>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/a9befe05-0cb9-4e0c-ba1f-43b4275ce55e" width="150">    <!--이진성-->
    </td>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/35c220cf-9b00-4e9a-a3e9-0e2e3e2318b7" width="120">    <!--고아연-->
    </td>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/89342c37-c1f9-4fcf-9ef9-a9fc032a807f" width="110">    <!--김재현-->
    </td>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/21d5ac6e-c2c9-47a8-867a-7cb362f05973" width="120">    <!--박성재-->
    </td>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/e10fba61-2421-4bca-b470-506f854fa909" width="110">    <!--배준서-->
    </td>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/10778e56-ea3c-4e64-8204-3ab5a5d2df36" width="110">    <!--윤소정-->
    </td>
  </tr>

  <!-- 팀원 역할 Table-->
  <tr>
    <!--이진성-->
    <td align="center">
      Custom Tool<br>
      Router<br>
      답변 성능 평가 Tool<br>
      UI 개선
    </td>
    <!--고아연-->
    <td align="center">
      RAG PipeLine<br>
      Vector DB<br>
      PDF Hybrid Search<br>
      SQLite DB
    </td>
    <!--김재현-->
    <td align="center">
      Team BaseLineCode<br>
      WebSearchTool<br>
      etc PipeLine<br>
      MiddleWare
    </td>
    <!--박성재-->
    <td align="center">
      CustomTool<br>
      Prompt Engineering
    </td>
    <!--배준서-->
    <td align="center">
      CustomTool<br>
      Prompt Engineering
    </td>
    <!--윤소정-->
    <td align="center">
      CustomTool<br>
      Prompt Engineering
    </td>
  </tr>

  <tr>
    <td align="center">
      <a href="https://github.com/wlstjd6524"><img src="https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=GitHub&logoColor=white"/></a>        <!--이진성-->
    </td>
    <td align="center">
      <a href="https://github.com/ayoun88"><img src="https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=GitHub&logoColor=white"/></a>           <!--고아연-->
    </td>
    <td align="center">
      <a href="https://github.com/KJH-0596"><img src="https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=GitHub&logoColor=white"/></a>          <!--김재현-->
    </td>
    <td align="center">
      <a href="https://github.com/sungjae3911-arch"><img src="https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=GitHub&logoColor=white"/></a>  <!--박성재-->
    </td>
    <td align="center">
      <a href="https://github.com/jun-01111"><img src="https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=GitHub&logoColor=white"/></a>         <!--배준서-->
    </td>
    <td align="center">
      <a href="https://github.com/Lucia128"><img src="https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=GitHub&logoColor=white"/></a>          <!--윤소정-->
    </td>
  </tr>

</table>

## 📂 ReadME Index 
[📄 Executive Summary (프로젝트 개요)](#executive-summary) <br>

[🏗️ System Architecture (시스템 설계 및 구조)](#system-architecture) <br>

[📱 Demo & UI (서비스 구현 화면)](#demo--ui) <br>

[🛠️ Core Pipelines & Implementation (핵심 구현 파이프라인)](#core-pipelines--implementation) <br>

[🚀 Troubleshooting & Optimization (문제 해결 및 최적화)](#troubleshooting--optimization) <br>

[👥 Team Leadership & Management (팀 리더십 및 협업)](#team-leadership--management) <br>

[📈 Retrospective & Future Work (회고 및 향후계획)](#retrospective--future-work)


<a id="executive-summary"></a>

## 📄 Executive Summary
### 📌 Background
  - 글로벌 규제 강화 : 최근 글로벌 ESG 공시 의무화로 인해 기업 실무진이 대응해야 할 가이드라인이 방대해지고 있습니다.
  - 수작업의 한계 : 사람이 복잡한 계산식과 수만 개의 배출 계수를 직접 계산하거나, 규제 변화가 빠르게 이루어지면서 매년 개정되는 다양한 인증 기준과 법령이 존재하여 매번 개정되는 자료를 찾아보면서 발생하는 계산 오류 리스크와 업무 지연이 핵심 페인포인트 입니다.
  - 지능형 솔루션의 필요성 : 이런 문제를 해결함과 동시에 단순 키워드 검색을 넘어 문맥을 파악하고 정형/비정형 데이터를 통합 처리하는 자동화 솔루션이 필수적입니다.

### 🎯 Objective
  - 도메인 특화 에이전트 구축 : `LangChain` 및 `LangGraph` 를 활용하여 ESG 도메인 지식을 정확히 이해하고 태스크를 수행하는 Agent Architecture 설계.
  - 신뢰성 확보 : 할루시네이션을 최소하기 위해 `RAG 파이프라인`과 정밀한 수치 계산 및 여러가지 분석 도구(CustomTool)를 연동.
  - 확장성 및 운영 안정성 확보 : 각 Custom Tool 의 독립성을 보장하여 단일 모듈 장애가 전체 시스템으로 전파되는 것을 방지하고, 실시간 로그 추적 미들웨어 및 'LLM Judge' 를 도입하여 지속적인 성능 모니터링과 유지보수가 가능한 파이프라인 설계.
  - 실무 활용성 기대 : ESG 도메인에 맞는 계산식 도구 또는 법령 검색, 지배구조 벤치마킹 등 실무자에게 즉각적인 도움을 주는 PipeLine 구현.

### 🔧 Tech Stack
| Category | Tech Stack |
| :--- | :--- |
| **Framework & Orchestration** | LangChain, LangGraph |
| **LLM Model** | Upstage Solar-Pro |
| **Database & Storage** | ChromaDB (Vector), SQLite (RDB), AWS S3 |
| **Data Pipeline & NLP**| BM25 (Sparse Retrieval), DocTR (OCR), KoNLPy (형태소 분석) |
| **Tools & API** | Tavily API (Web Search), OpenDartReader |
| **Monitoring & UI** | LangSmith (Tracing), Gradio (Prototype UI) |

<a id="system-architecture"></a>

## 🏗️ System Architecture
<img width="8192" height="5488" alt="Image" src="https://github.com/user-attachments/assets/17734813-7f81-4873-9ebe-5a90cf9b9e32" /> <br>
### System WorkFlow 요약
본 프로젝트는 기업의 지속가능경영 공시 대응을 지원하기 위해 내부 지식(RAG)과 외부 실시간 정보(Web Search)를 결합한 하이브리드 지능형 에이전트 시스템입니다.

### 핵심 설계 전략
1. Hybrid Data Ingestion : 내부 가이드라인(PDF)과 배출 계수 데이터(CSV)를 수집하여 `Vector DB` 와 `RDB` 에 각각 구조화합니다 . 특히 최신 규제 및 뉴스 대응 그리고 매일 바뀌는 환율 분석을 위해 실시간 `Web Search(Tavily API)` 파이프라인을 통합하여 RAG의 정보 최신성 한계를 보완했습니다.
2. Context Optimization & Routing : 사용자 질문이 입력되면 `Context Summarizer(Middleware)` 가 대화 기록을 분석하여 토큰 비용을 최적화하고 , `Semantic Router` 가 발화 의도를 일상 대화와 ESG 전문 태스크로 정밀하게 분기합니다.
3. Agentic Workflow : ReAct 아키텍처 기반의 에이전트가 질문 해결에 최적화된 도구(RAG, Web Search, 계산기 등)를 자율적으로 선택하여 수행합니다.
4. Backend Monitoring & Maintenance : 모든 추론 로그는 실시간으로 기록되며, 시스템의 지속적인 고도화를 위해 Custom LLM Judge가 백엔드에서 답변의 기술적 타당성을 평가합니다. 이는 사용자 응답 속도에 영향을 주지 않으면서도, 파이프라인별 유지보수 우선순위를 결정하는 핵심 지표로 활용됩니다.

### 🏆 Key Contributions (개인 기여 파이프라인)
| **Category** | Details |
| :--- | :--- |
| **Role** | Technical Lead(팀 일정 조율 및 협업 프로세스 주도, PR/Merge 관리) |
| **Core Pipelines** | Senantic Router, Custom LLM Judge |
| **Custom Tools** | Carbbon Emission Calculator(탄소 배출 계산기), Security Compliance Checklist(정보 보호 인증 규정 분석) |
| **Data Engineering** | CustomTool 에 필요한 실무 데이터(정형/비정형) 수집 및 LLM 이 학습을 진행할 때 효율을 높이기 위한 표준 컬럼 매핑 전처리 |

<a id="demo-ui"></a>

## 📱 Demo & UI
<img width="1493" height="875" alt="Image" src="https://github.com/user-attachments/assets/3f2072de-00ec-48aa-bad2-5f9a1e9017fc" /> <br> <br>
<img width="1492" height="179" alt="Image" src="https://github.com/user-attachments/assets/4289a11a-bc8a-4359-af08-347ae422724e" />

<a id="core-pipelines"></a>

## 🛠️ Core Pipelines & Implementation
본 섹션은 Key Contributions 을 기반으로 시스템의 두뇌 역할을 하는 의도 분석(Router), 도메인 지식이 집약된 도구 설계(Custom Tool), 그리고 데이터 기반의 품질 검증(LLM Judge) 파이프라인을 중심으로 구성되었습니다.

1. 지능형 시맨틱 라우터 (Semantic RouteR)
    - 의도 기반 트래픽 제어 : 사용자의 입력 즉시 LLM(Solar-Pro) 이 의도를 분석하여 'ESG 전문 태스크' 와 '일상 대화' 로 분기하는 최상위 라우터 노드를 설계했습니다.
    - 확정적 출력 제어 : `Pydantic` 과 `with_structured_output` 을 결합하여 에이전트가 호출할 도구와 파라미터를 JSON 형태로 확정 반환하도록 강제했습니다. 이를 통해 불필요한 도구 탐색 과정을 생략하여 <b>토큰 소모를 절감하고 응답지연을 최적화</b> 했습니다.
    - 상태 관리의 유연성 : `LangGraph` 의 `StateGraph` 구조를 활용해 에이전트 상태를 관리함으로써, 기능 노드 간 결합도를 낮추고 새로운 도구나 파이프라인을 즉시 통합할 수 있는 확장성을 확보했습니다.

2. 데이터 중심 Custom Tool 설계 및 프롬프트 가드레일
    - 데이터 무결성 전처리 : LLM이 배출 계수와 규ㅠ정 조항을 정확히 참조할 수 있도록, 수집된 정형 데이터에서 불필요한 컬럼을 제거하고 <b>표준 컬럼 매핑</b> 을 수행하는 전처리 파이프라인을 구축했습니다.
    - 할루시네이션 차단 설계
      - 강제적 도구 연쇄 : 함수 내부 독스트링에 <b>반드시 DB에서 계수를 먼저 조회하고 연산을 수행해라</b> 라는 행동 지침을 명시하여, 모델이 임의로 숫자를 날조하는 것을 원천 차단했습니다.
      - 추측금지 가드레일 : 결과값이 없을 경우 자의적인 숫자 생성을 절대 금지하고, 내부 도구명이나 파라미터 구조가 사용자에게 노출되지 않도록 <b>보안 및 데이터 은닉</b> 프롬프트를 적용했습니다.
    - 응답 포맷 표준화 : 답변 형식을 "[1단계: 상태분석] -> [2단계: 추가 정보 안내] -> [3단계: 다음 단계]"의 블록 형식으로 고정하여 일관된 UX 를 제공했습니다.

3. 자동화 답변 성능 평가 시스템 (LLM Judge)
    - 정량적 실험 체계 : 사전 구축된 평가 데이터셋을 활용하여, 파이프라인 로직 변경 시 답변 품질의 변화를 정량적으로 추적했습니다.
    - 전문가 페르소나 채점 : 추론 능력이 뛰어난 모델에 <b>엄격한 ESG 컨설팅 전문가</b> 페르소나를 부여하여, 단순 키워드 매칭이 아니라 숫자 연산의 논리적 타당성과 도메인 적합성을 자동 채점하도록 설계했습니다.
    - 무관용 평가 : 모호한 점수체가 아닌 <b>'통과(1점) / 실패(0점)'</b>의 2진 분류 방식을 적용했습니다. 숫자 연산 오류나 도메인 개념상 분류 미비 시 즉시 실패로 판정하여, 실무 배포 전 및 서비스가 배포되더라도 결함을 지속적, 보수적으로 필터링하는 파이프라인 피드백 루프를 구축했습니다.

<a id="troubleshooting"></a>

## 🚀 Troubleshooting & Optimization
### 1. 전문 도메인(ESG) 데이터 수집 및 데이터 스키마 설계의 한계 극복
#### 문제 정의
ESG는 글로벌 공시 규제와 법률적 전문성이 요구되는 생소한 도메인으로, 신뢰성 있는 학습/참조 데이터를 확보하는데 어려움이 있었습니다. 특히 글로벌 대응을 위해 해외 전문 자료를 파싱해야 하는 과정에서 데이토 소스의 불일치 문제가 발생했습니다.

#### 원인 분석
단순 검색으로는 실무자가 필요로 하는 정밀한 계산 계수와 법적 근거를 추출할 수 없었고, 도메인 지식의 깊이가 부족하여 초기 데이터 전처리 방향 설정에 혼선이 있었습니다.

#### 해결 방안
SK,LG 등 선도 기업의 ESG 지속가능경영보고서를 정밀 분석하여 실무 핵심지표를 도출하고 기존 ESG 타겟 솔루션들의 로직을 분석하고 실제로 해당 도메인을 타겟하는 여러 프로그램들이 존재하여 그 프로그램들의 방향성을 벤치마킹하여 에이전트가 필요로 하는 데이터 구조 설계를 진행하였습니다. 이를 통해 정형 데이터(계수) 와 비정형 데이터 (규제 가이드라인)의 표준을 정의하고 전처리 효율을 개선했습니다. 

#### 인사이트
<b>도메인에 대한 깊은 이해가 AI 파이프라인의 논리적 구조와, 더 양질의 데이터를 만들어 낼 수 있는 방향성 정의 그리고 최종 성능을 결정한다</b>는 원칙을 얻게되었습니다.

---

### 2. 유지보수성을 고려한 모듈 독립성 확보 및 연쇄작용 구현
#### 문제 정의
시스템의 유지보수성을 위해 각 CustomTool 은 독립적이어야 하지만, 실제 답변 생성을 위해서는 여러 도구가 유기적으로 연쇄 반응을 일으켜야 하는 설계상의 모순에 직면했습니다.

#### 원인 분석
도구 내부에 다른 도구에 대한 의존성이 직접 코딩될 경우, 하나의 모듈 수정이 전체 시스템의 오류로 전파되는 <b>강한 결합</b> 문제가 발생할 위험이 있었습니다. 또한 실제로 몇 개의 Tool 에서는 다른 Tool 을 하드코딩 하는 방식으로 Tool 구성이 이루어져 있어서 실제로 의존성 문제가 발생하였습니다.

#### 해결방안
각 Tool 은 오직 자신의 고유 기능에만 집중하도록 원자적 단위로 설계했습니다. <br>
이에 따라 도구 간의 연결 로직을 코드 레벨이 아닌, <b>LangGraph의 상태 전이와 LLM의 프롬프트 제어</b> 로 권한을 부여했습니다. 에이전트가 현재 상태를 판단하여 다음 도구를 호출하도록 유도하는 '프롬프트 가드레일' 을 구축하여 시스템의 유연성을 확보했습니다.

#### 인사이트
<b>복잡한 파이프라인일수록 로직은 원자적으로 분리하되, 흐름 제어는 오케스트레이터에 맡기는 것이 유지보수성을 극대화하는 길</b> 임을 확인했습니다.

---

### 3. 모듈 간 의존성 관리 및 인터페이스 규격화를 통한 병렬 개발 최적화
#### 문제 정의
데이터 적재 방식의 변경이 하위 Custom Tool의 호출 로직과 충돌하며 시스템 전체의 불안정성을 초래하고, 이로 인해 개발 생산성이 저하되는 병목 현상이 발생했습니다.

#### 원인 분석
프로젝트 초기, 데이터 파이프라인과 Custom Tool 파이프라인 간의 "입출력 데이터 규격" 이 엄격하게 정의되지 않은 채 개발이 진행되어, 파이프라인 통합 시 잦은 수정과 불필요한 회의가 반복되었습니다.

#### 해결 방안
각 모듈이 주고 받는 데이터 형식을 JSON 으로 선제 정의하여, 데이터 파이프라인의 변경이 Tool 로직에 미치는 영향을 최소화 하고, 팀 리더로서 각 파이프라인의 의존 관계를 재설계하고, <b>독립적 단위 테스트</b> 환경을 구축하여 팀원들이 서로의 진행 상황에 구애받지 않고 병렬로 기능을 고도화할 수 있도록 조율했습니다.

#### 인사이트
<b>협업의 효율은 단순한 대화가 아닌, 명확한 기술 규격과 문서화된 인터페이스에서 나온다</b> 는 점을 실감했습니다.

---

### 4. 에이전트 루프 중복 실행 방지 및 3분 이상의 응답 지연 개선
#### 문제 정의
특정 도구 호출 시 에이전트가 동일한 데이터 파싱 과정을 반복적으로 수행하여 응답 시간이 3분 이상 소요되거나, 타임아웃(Timeout) 에러가 발생하는 등 서비스 불가능 수준의 성능 저하가 확인되었습니다.

#### 원인 분석
프롬프트 내 제어 지시문이 모호하여 LLM이 출력 결과에 확신을 갖지 못하고 보수적으로 작동하거나, 데이터 구조를 오인하여 불필요한 연산을 재수행하는 것이 원인이었습니다.

#### 해결 방안
페르소나 부여 규칙을 엄격히 준수하고, "절대 중복 파싱을 하지 말 것" 과 같은 <b>부정 지시어</b> 와 <b>Few-shot</b> 예시를 보강하여 에이전트의 판단 경로를 단순화했습니다. <br>
또한 `Pydantic` 을 활용하여 데이터 추출 형식을 강제함으로써 LLM 의 해석 오류를 사전에 차단하고, 파이프라인의 전체 실행 시간을 획기적으로 단축하여 타임아웃 문제를 해결했습니다.

#### 인사이트
<b>코드 로직만큼이나 정교한 프롬프트 제어가 에이전트 기반 시스템의 실제 성능과 비용 효율성을 결정짓는 핵심 엔지니어링 요소임</b>을 깨달았습니다.

<a id="Team Leadership-Management"></a>

## 👥 Team Leadership & Management
프로젝트 팀장으로서 단순한 일정 관리를 넘어, 기술적 병목 현상을 제거하고 개발 효율을 극대화하기 위한 `협업시스템` 을 설계했습니다.

### GitHub 기반 코드 버전 관리
GitHub 작업 레포를 만들어 Contributors 로 팀원을 초대하고, 레포에 존재하는 Push, Merge 규칙을 "1명 이상의 작업자가 승인 시 Merge" 라는 항목을 부여하여 모든 팀원이 코드를 실시간으로 관리할 수 있게 레포 관리를 주도했습니다. <br>
[GitHub 작업레포](https://github.com/wlstjd6524/LangchainRag_01)

### 팀원간 정보 격차 관리 및 함께 성장하는 프로젝트 방향성 수립
Notion 을 활용해 도메인 지식을 관리하고, Slack 을 통해 팀원에게 프로젝트간 이행해야 할 규칙들을 명시함으로써 팀원 간의 정보 격차를 해소하고 함께 성장하는 프로젝트 목표를 수립하고자 노력하였습니다. <br>
또한 텍스트로만 주고받는 정보는 인지에 한계가 있다고 판단하여 프로젝트 진행상황 및 일정을 고려하여 Zoom 으로 실시간으로 공유하고자 하였습니다. <br>
[Notion](https://www.notion.so/ESG-Tool-23d6325e11938098aa97e22ed903393b)

<a id="Retrospective-Future Work"></a>

## 📈 Retrospective & Future Work
### 📌 회고
이번 프로젝트를 통해서 전 프로젝트를 통해 배웠던 RAG 파이프라인을 어떻게하면 더 잘 활용할 수 있는지, 또한 랭체인에 대한 전반적인 파이프라인을 이해할 수 있는 좋은 프로젝트 였던 것 같습니다. <br>
수행하면서 어려웠던 점은 바로 <b>도메인에 대한 이해</b> 와 <b>파이프라인 간의 독립성 확보</b> 그리고 <b>독립성이 확보된다 하지만 그런 부분들이 연쇄적으로 작용해야 한다는 점</b> 들이 어려웠던 점으로 작용했던 것 같습니다. <br>

보통 상품화를 할 수 있는 프로그램을 만드는 프로젝트에서 항상 고민했던 점은 "어떻게 하면 유지보수를 조금 더 쉽게 가져갈 수 있을까?" 라는 점을 기반으로 파이프라인을 구성하려고 노력하는데, 이번 프로젝트에서 "Tool 들은 그들만의 기능을 가질 수 있게 독립성을 확보해야 하지만, 다른 Tool 들과 연쇄적으로 작용 할 수 있어야 한다" 라는 접근성이 제가 항상 생각하는 "유지보수 장점에 용이" 라는 고민을 조금 더 어렵게 하지 않았나 라는 생각이 들었습니다. <br>

또한 각 Tool 들 간의 연쇄작용이 중요하다 보니 독단적으로 하나의 파이프라인을 맡아도 다른 파이프라인을 맡는 팀원들과 꾸준히 커뮤니케이션을 진행해야 한다는 점도 어려웠던 점으로 작용했던 것 같습니다. <br>
이런 작은 프로젝트에서 마저도 많은 회의를 요구했는데 실무에서는 얼마나 많은 팀회의를 걸칠지 생각해 볼 수 있는 좋은 기회 였던 것 같습니다. <br>

마지막으로 항상 생각했던 "데이터의 품질" 에 대한 중요성을 넘어서 이런 좋은 데이터의 품질의 기반은 "도메인 지식을 깊게 이해해야 한다는 점" 을 인지했고, 만만하게만 생각했던 프롬프트 와 페르소나 부여가 전체적인 파이프라인을 장악할 수 있을 정도로 영향력이 크다 라는 점도 새롭게 알고 인지하게 되었습니다.

### 📗 향후계획
제가 맡은 `LLM Judge` Tool 을 현재 프로젝트에서는 백엔드에서 개발자가 시스템 성능이 어떻게 나오는지 지표로 판단하고 서비스 품질을 향상시키기 위한 인증서로 삼기위해서 수동으로 돌려야 하는 로직을 배경으로 두고 구현을 했습니다. <br>
향후 프로젝트 고도화를 진행하게 된다면 이런 로직이 LLMOps 기반 으로 자동화 시킬 수 있는 WorkFlow 로 개선해보고 싶고, 또한 토큰 사용량이나 사용자에게 답변을 던지는 시간에 영향이 많이 가지 않는다면 LLM 이 사용자에게 답변을 던지기 전에 자체적으로 제가 구현한 `LLM Judge` Tool 을 지나고 나서 검증을 하고 난 후에 사용자에게 답변을 뱉는 자동화도 구현해보고 싶습니다. <br>

또한 처음에 해당 파이프라인으로 진행해보려고 생각해 본 `개인 자료 기반으로 직무의 핵심 역량에 맞춰 면접용 포맷으로 경량화 하는 Agent` 를 개발해보고 싶습니다. 
