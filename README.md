# ESG Guide AI Agent
목적 : 복잡한 ESG 규제, 분석 및 계산 항목에 대한 처리에 어려움을 겪는 기업 실무자들을 위한 LangChain & RAG 파이프라인 기반 지능형 AI Agnet 설계


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

### 🛠️ Tech Stack
| Category | Tech Stack |
| :--- | :--- |
| **Framework & Orchestration** | LangChain, LangGraph |
| **LLM Model** | Upstage Solar-Pro |
| **Database & Storage** | ChromaDB (Vector), SQLite (RDB), AWS S3 |
| **Data Pipeline & NLP**| BM25 (Sparse Retrieval), DocTR (OCR), KoNLPy (형태소 분석) |
| **Tools & API** | Tavily API (Web Search), OpenDartReader |
| **Monitoring & UI** | LangSmith (Tracing), Gradio (Prototype UI) |


## 🏗️ System Architecture
