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
      <img src="https://github.com/user-attachments/assets/a9befe05-0cb9-4e0c-ba1f-43b4275ce55e" width="130">    <!--이진성-->
    </td>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/35c220cf-9b00-4e9a-a3e9-0e2e3e2318b7" width="120">    <!--고아연-->
    </td>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/89342c37-c1f9-4fcf-9ef9-a9fc032a807f" width="120">    <!--김재현-->
    </td>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/21d5ac6e-c2c9-47a8-867a-7cb362f05973" width="125">    <!--박성재-->
    </td>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/e10fba61-2421-4bca-b470-506f854fa909" width="120">    <!--배준서-->
    </td>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/10778e56-ea3c-4e64-8204-3ab5a5d2df36" width="120">    <!--윤소정-->
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

[🛠️ Core Pipelines & Implementation (핵심 구현 파이프라인)](#core-pipelines--implementation) <br>

[🚀 Troubleshooting & Optimization (문제 해결 및 최적화)](#troubleshooting--optimization) <br>

[👥 Team Leadership & Management (팀 리더십 및 협업)](#team-leadership--management) <br>

[📈 Retrospective & Future Work (회고 및 향후계획)](#retrospective--future-work)


## 📄 Executive Summary
### 📌 Background
  - 글로벌 규제 강화 : 최근 글로벌 ESG 공시 의무화로 인해 기업 실무진이 대응해야 할 가이드라인이 방대해지고 있습니다.
  - 수작업의 한계 : 사람이 복잡한 계산식과 수만 개의 배출 계수를 직접 계산하거나, 규제 변화가 빠르게 이루어지면서 매년 개정되는 다양한 인증 기준과 법령이 존재하여 매번 개정되는 자료를 찾아보면서 발생하는 계산 오류 리스크와 업무 지연이 핵심 페인포인트 입니다.
  - 지능형 솔루션의 필요성 : 이런 문제를 해결함과 동시에 단순 키워드 검색을 넘어 문맥을 파악하고 정형/비정형 데이터를 통합 처리하는 자동화 솔루션이 필수적입니다.

### 🎯 Objective
  - 도메인 특화 에이전트 구축 : LangChain 및 LangGraph 를 활용하여 ESG 도메인 지식을 정확히 이해하고 태스크를 수행하는 Agent Architecture 설계.
  - 신뢰성 확보 : 할루시네이션을 최소하기 위해 RAG 파이프라인과 정밀한 수치 계산 및 여러가지 분석 도구(CustomTool)를 연동.
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


## 🏗️ System Architecture
<img width="8192" height="5488" alt="Image" src="https://github.com/user-attachments/assets/17734813-7f81-4873-9ebe-5a90cf9b9e32" /> <br>
### System WorkFlow 요약
본 시스템은 사용자 질문의 의도를 분석하여 최적의 경로를 결정하고, 독립적으로 설계된 모듈형 도구들을 유기적으로 결합하여 최종 답변을 도출하는 LangGraph 기반의 ReAct 아키텍처를 채택하고 있습니다.

### 핵심 설계 전략
<b>1. 상태 관리 및 장애 격리</b>
  - <b>LangGraph 기반 상태 제어</b> : 모든 대화 기록과 도구 호출 상태를 StateGraph 구조로 관리하여 기능 간 결합도를 낮추고, 특정 파이프라인의 오류가 전체 시스템 중단으로 이어지지 않도록 설계했습니다.
  - <b>도구의 독립성 및 연쇄 작용</b> : 각 Custom Tool은 개별적인 기능을 수행하도록 독립성을 확보하되, 에이전트의 프롬프트 제어 하에 순차적인 체이닝이 가능하도록 리팩토링하여 <b>유지보수 효율성</b>을 극대화 했습니다.

<b>2. 지능형 라우팅 및 자원 최적화</b>
  - <b>Sementic Router 도입</b> : Pydantic 기반의 구조화된 출력을 활용해 질문 의도를 '일상 대화' 와 'ESG 전문 작업' 으로 즉각 분류합니다. 불필요한 도구 탐색 과정을 생략함으로써 API 호출 비용을 절감하고 응답속도를 개선했습니다.

<b>3. 데이터 무결성 및 품질 보증</b>
  - <b>Custom LLM Judge</b> : 생성된 답변의 수치 정확도와 논리적 일치 여부를 '엄격한 컨설팅 전문가' 페르소나를 가진 별도 모델이 자동으로 검증합니다. 통과/실패(0/1) 의 무관용 채점기준(2진 분류법) 기준을 적용하여 시스템의 신뢰성을 정랼적으로 관리합니다.
  - <b>동적 컨텍스트 압축</b> : 대화가 길어질 경우 이전 기록을 자동으로 요약 압축하고 최신 문맥만 보존하여, 토큰 비용 최적화와 동시에 에이전트의 단기 기억을 정확히 유지하도록 설계했습니다.

### Key Contributions
| **Category** | Details |
| :--- | :--- |
| **Role** | Technical Lead(팀 일정 조율 및 기술 스택 선정 주도, PR/Merge 관리) |
| **Core Pipelines** | Senantic Router, Custom LLM Judge |
| **Custom Tools** | Carbbon Emission Calculator(탄소 배출 계산기), Security Compliance Checklist(정보 보호 인증 규정 분석) |


## 🛠️ Core Pipelines & Implementation
