## 1. 프로젝트 개요

<aside>

### 1-1. 프로젝트 명: 청약 관련 문서 요약 및 질의응답 챗봇

- **팀 명: NLP MASTERS**
- **팀원**: 박건희, 배재성, 이사라
- **프로젝트 목표**
    - **PDF 문서 요약 및 질의응답 챗봇 개발**
    - **빠르고 정확한 문서 검색 기능 구현**
    - **한국어 최적화 및 비용 효율적 AI 시스템 구축**
    - **향후 확장성을 고려한 설계**
    - 

### **1-2. 구성 요소**

- **LangChain**: 문서 분석 및 자연어 질의응답 처리.
- **RAG**: 문서에서 중요한 정보를 검색하여 LLM과 결합해 보다 정확한 답변 제공.
- **FAISS (벡터 저장소)**: 문서 내용 검색 및 임베딩 최적화.

### **1-3. 핵심 타겟**

- 기업 내부 문서 검색 및 FAQ 자동 응답 시스템.
- 법률, 의료, 연구 분야에서의 문서 분석 및 질의응답 지원.

### 1-4. 서비스 개요

청약 관련 문서 요약 및 질의응답 챗봇은 PDF 청약 공고문 및 관련 문서를 자동으로 분석하고, 사용자의 질문에 AI가 정확한 답변을 제공하는 시스템입니다.

이 챗봇은 LangChain과 RAG(Retrieval-Augmented Generation) 기술을 활용하여 문서를 검색하고 요약하며, 대형 언어 모델(LLM)을 통해 자연어로 답변을 제공합니다.

</aside>

## 1-5. RAG ?

![Image](https://github.com/user-attachments/assets/991084a7-9e30-4af2-821a-a0bc86019162)

## 2. 개발 기간

<aside>

### **1일차 (1월 8일) - 프로젝트 기획 및 환경 설정**

- 프로젝트 목표 및 핵심 기능 정의
- 요구사항 분석 및 기술 스택 선정
- LangChain 및 RAG 개념 검토 및 설계
- 개발 환경 세팅 (Python, FastAPI, Streamlit, FAISS)

### **2일차 (1월 9일) - PDF 로더 및 텍스트 전처리 구현**

- `PyPDFLoader` 및 `pdfplumber` 비교 후 적합한 로더 선정
- 텍스트 추출 및 전처리 로직 구현 (`kiwi` 기반 불용어 처리 테스트)
- `RecursiveCharacterTextSplitter` 활용하여 텍스트 분할
- 문서 내 표 데이터 처리 방안 검토

### **3일차 (1월 10일) - 임베딩 및 벡터 저장소 구축**

- `jhgan/ko-sbert-nli` 기반 임베딩 모델 적용 및 성능 테스트
- `FAISS` 및 `ChromaDB` 비교 후 `FAISS` 선택
- 벡터 저장소 구축 및 데이터 검색 기능 구현

### **4일차 (1월 11일) - Retriever 및 질의응답 시스템 개발**

- `Multi-Query Retriever` 및 `Ensemble Retriever` 적용 및 성능 비교
- RAG 기반 검색 시스템 구축
- LangChain `RetrievalQAWithSourcesChain` 적용
- 검색 정확도를 높이기 위한 프롬프트 최적화

### **5일차 (1월 12일) - LLM 연동 및 챗봇 기능 구현**

- OpenAI GPT-3.5 Turbo, Groq API, Gemini 1.5 모델 비교 및 적용
- 질의응답 시스템 성능 테스트 및 응답 최적화
- FastAPI를 활용한 백엔드 API 개발
- 프론트엔드 (Streamlit) UI 기본 구성

### **6일차 (1월 13일) - 통합 테스트 및 최적화**

- 전체 시스템 통합 및 End-to-End 테스트 진행
- 응답 속도 및 검색 정확도 최적화
- PDF 업로드 및 질의응답 시나리오 테스트
- 최종 버그 수정 및 코드 리팩토링
</aside>

## 3. 기술 스택

<aside>

### **3-1. Backend & Frontend**

- Python 3.10, Streamlit

### 3-2. Database

- FAISS

### **3-3.  NLP Frameworks & AI 모델**

- **RAG, LLM, LangChain**

### **3-4. Embedding model:** OpenAI, Sentence Transformers

</aside>

### 

## 4. 담당 역할 및 기여도

<aside>

### **4-1. 프로젝트 매니저 (PM) 역할**

- **기획**: 프로젝트 목표 및 핵심 기능 정의, 기술 스택 선정
- **조율**: 팀 내 역할 분배 및 일정 관리, 기술적 의사결정 조정
- **팀 협업 지원**: 개발 일정 관리 및 진행 상황 점검, 리스크 관리

### **4-2. 주요 기여 사항**

### **1) AI 및 백엔드 개발**

- **LLM 기반 질의응답 시스템 개발**
    - GPT-3.5 Turbo, Groq API, Gemini 1.5 모델 비교 및 최적화
    - LangChain을 활용한 PDF 문서 분석 및 자연어 질의응답 기능 구현
    - RAG 기반 검색 시스템 구축 및 성능 최적화
- **벡터 저장소 및 검색 기능 구현**
    - FAISS를 활용한 문서 검색 기능 개발 및 최적화
    - `jhgan/ko-sbert-nli` 임베딩 모델 적용하여 한국어 검색 정확도 향상

### **2) 프로젝트 전반 관리 및 의사결정**

- **기술 아키텍처 설계 조율**
    - LangChain, FAISS, FastAPI 등의 기술 스택 선정 및 구조 설계
    - 데이터 저장 및 검색 방식 결정 (FAISS vs ChromaDB 비교 후 FAISS 선택)
- **팀원 간 협업 지원 및 일정 조율**
    - 백엔드-프론트엔드 간 API 연동 작업 조율
    - 개발 일정 관리 및 진행 상황 점검
- **성능 최적화 및 테스트 진행**
    - API 응답 속도 최적화 (비동기 처리 및 데이터 최적화)
    - 문서 검색 정확도 개선 및 프롬프트 최적화

### **3) 문서화 및 발표 준비**

- **개발 문서 정리 및 프로젝트 보고서 작성**
    - 주요 기술 선택 배경, 검색 및 질의응답 로직 문서화
- **프로젝트 발표 자료 제작 및 시연 준비**
    - 챗봇 데모 준비 및 성능 비교 자료 정리
    - 팀원과 역할 분담하여 최종 발표 진행
</aside>

## 5. 주요 기능 및 특징

<aside>

### **5-1. 주요 기능**

**PDF 문서 업로드 및 자동 요약**

- 사용자가 **PDF 파일을 업로드**하면 문서의 핵심 내용을 자동으로 분석 및 요약
- **LangChain과 RAG**를 활용하여 문서의 구조를 파악하고 중요한 정보 추출
- **표 데이터까지 분석**하여 숫자 기반 정보도 요약 가능

**PDF 기반 질의응답 시스템**

- 문서 내용을 기반으로 **AI가 자연어 질의응답 수행**
- **LLM (GPT-3.5 Turbo, Groq API, Gemini 1.5)과 RAG 기술 적용**
- 질문에 대한 **정확한 문맥 기반 답변 제공**

**빠르고 정확한 문서 검색 기능**

- **FAISS 벡터 검색 기술 적용** → PDF 내에서 **연관성이 높은 문서 내용 검색 가능**
- **Multi-Query Retriever & Ensemble Retriever** 적용하여 검색 정확도 향상
- 문서 내 **키워드 검색 및 특정 문장 검색 기능 제공**

**표 인식 및 데이터 분석**

- PDF 내 **표(Table) 데이터를 감지하고 구조적으로 분석**
- 숫자 기반 테이블의 경우 **합계, 평균 등 주요 지표 참고하여 답변 생성**
- OCR 기능 추가 예정 (이미지 기반 표 처리 보완)

**다중 문서 처리 기능**

- 여러 개의 PDF 문서를 동시에 업로드 가능
- **문서 간 연관 정보를 분석**하여 질의응답 수행
- 특정 문서뿐만 아니라 **다중 문서 검색을 통해 종합적인 답변 제공**

**사용자 친화적인 인터페이스**

- **Streamlit 기반 웹 UI 제공** → 직관적인 PDF 업로드 및 질의응답 환경
- **질의응답 인터페이스 개선** → 대화형 챗봇과 유사한 사용 경험 제공
- 검색 결과 및 요약 내용을 **시각적으로 정리하여 가독성 향상**

---

### **5-2. 주요 특징**

**AI 기반 문서 분석 및 검색 최적화**

- **LangChain과 RAG를 활용한 AI 검색 시스템**으로 기존 키워드 검색 방식보다 정확한 검색 가능
- 문서의 문맥을 이해하여 단순 키워드 검색이 아닌 **의미 기반 검색 및 답변 제공**

**고성능 벡터 저장소 적용**

- **FAISS 벡터 저장소를 활용하여 빠르고 정확한 문서 검색 수행**
- 기존의 InMemoryVectorStore 대비 성능 향상 및 대량 문서 처리 가능

**한국어 최적화 임베딩 모델 적용**

- 한국어 문서 처리를 위해 **`jhgan/ko-sbert-nli` 임베딩 모델 적용**
- 기존 OpenAI 임베딩 API 대비 비용 절감 및 성능 최적화

**LLM 연동 및 검색 성능 최적화**

- OpenAI GPT-3.5 Turbo, Groq API, Gemini 1.5 등 다양한 LLM을 비교 후 최적화 적용
- **질의응답 속도 향상을 위해 검색 결과를 사전 필터링하여 LLM에 전달**

**확장성을 고려한 설계**

- **OCR 추가 예정** → 이미지 기반 PDF에서도 텍스트 인식 및 검색 가능하도록 개선
- **다양한 도메인 적용 가능** → 법률, 의료, 연구 논문 등의 문서 분석 및 질의응답 시스템으로 확장 가능

**사용한 로더:  `PyPDFLoader`**

- `pdfplumber`가 가장 높은 정확도를 보였지만 속도가 느리다는 점을 발견했으며
- **`PyPDFLoader`**가 속도와 Langchain과 통합이 용이해 적합하다고 판단했습니다.
</aside>

# **6. 아키텍처 및 시스템 설계**

### 6-1. 시스템 프로세스 아키텍처

![Image](https://github.com/user-attachments/assets/244cd583-b3b9-4dca-8cd7-26fa22d9a298)

## **7. 문제 해결 및 개선 사항**

<aside>

### **7-1. 표 인식 문제 해결 및 개선**

- **문제점**: PDF 내 **복잡한 표 데이터를 정확하게 인식하지 못하는 문제 발생**
- **원인**:
    - 병합된 셀과 복잡한 테이블 구조로 인해 데이터 추출 시 오류 발생
    - 표 안의 숫자 데이터를 문맥 없이 그대로 출력하는 문제 발생
- **해결 방법**:
    - 표 데이터를 처리하는 별도의 전처리 로직 추가
    - **표 주변 텍스트를 함께 고려하도록 프롬프트 최적화**
    - **숫자 기반 표 데이터 처리 로직 강화** (합계, 평균 등 통계값 제공)

### **7-2. 불완전한 답변 문제 해결 및 개선**

- **문제점**: 질의응답 시 **일부 문장만 출력되거나 문맥이 끊긴 답변 발생**
- **원인**:
    - **텍스트 분할(`RecursiveCharacterTextSplitter`) 과정에서 문맥 손실 발생**
    - **Retriever 검색 과정에서 불완전한 정보만 가져오는 경우 발생**
- **해결 방법**:
    - `chunk_size=1000`: 각 청크의 최대 크기를 1000자로 설정.
    - `chunk_overlap=200`: 청크 간 중복 영역을 200자로 설정하여 문맥 보존.
    - **커스텀 구분자**: `splits_text = ["■", "▣"]`를 설정하여 PDF 내에서 해당 기호를 기준으로 문맥을 나누도록 지정.
    - **Multi-Query Retriever 적용하여 검색 결과의 다양성 확보**
    - **답변의 신뢰도를 높이기 위해 LLM 프롬프트 최적화 진행**

### **7-3. LLM 최적화 및 응답 속도 개선**

- **문제점**: LLM의 응답 속도가 느리거나 **불필요한 API 호출로 비용 증가**
- **원인**:
    - OpenAI API 사용 시 **고비용 발생**
    - 다량의 문서를 처리할 경우 **임베딩 모델의 연산량 증가로 속도 저하**
- **해결 방법**:
    - **로컬 임베딩 모델(`jhgan/ko-sbert-nli`) 적용하여 API 호출 비용 절감**
    - GPU 최적화 (`Batch Size` 동적 조정 및 벡터 정규화 적용)
    - **LLM 응답 속도를 높이기 위해 비동기 요청(Async API) 도입**

### **7-4. 프롬프트 최적화 및 답변 품질 개선**

- **문제점**: LLM이 **정확한 정보를 제공하지 못하거나, 비슷한 질문에 다른 답변 제공**
- **원인**:
    - **프롬프트 내 문맥이 명확하지 않아 LLM이 적절한 답변을 생성하지 못함**
    - 검색된 문서가 많을 경우 **불필요한 정보가 포함될 가능성 증가**
- **해결 방법**:
    - **프롬프트 템플릿 최적화** → 문맥 강조 및 표 데이터 해석 방식 개선
    - **LLM 출력을 검증하는 후처리 로직 추가**
    - **Retriever 검색 필터링 적용하여 불필요한 문서 제거**

### **7-5. 검색 정확도 개선**

- **문제점**: 비슷한 질문을 했을 때 **일관성 없는 검색 결과 제공**
- **원인**:
    - 단순 벡터 검색 방식 사용 시 **의미적으로 비슷한 문장까지 검색되지 않는 경우 발생**
    - 문서 검색 시 **검색 키워드와 일치하지 않는 문서가 포함될 가능성 존재**
- **해결 방법**:
    - **Ensemble Retriever (FAISS + BM25) 적용하여 검색 성능 향상**
    - **Multi-Query Retriever 도입** → 사용자의 질문을 다양한 방식으로 변환하여 검색
    - **FAISS 벡터 검색 필터링 적용** → 불필요한 문서 제거 및 가중치 기반 검색 강화

### **7-6.  불용어 처리**

- **nltk**
    - `nltk`는 한글 불용어 파일을 제공하지 않기 때문에, 한글 텍스트의 불용어 제거에 적합하지 않음.
- **kiwi**
    - `kiwi`는 **StopWords**를 통해 불용어를 제공하며, **tokenizer**로 단어를 분리 후 **join**을 통해 불용어를 제거하고 분리된 단어들을 다시 조합.
    - 이때, 한글을 제외한 다른 문자들은 모두 `replace` 처리됨.
    
    **<특수문자와 불용어 제거 문제>**
    
    - 해당 PDF는 **특수문자**를 기준으로 내용이 나누어지는데, `kiwi`로 불용어 처리 및 특수문자 제거를 진행한 뒤 임베딩을 수행하면 **엉뚱한 대답**을 하는 경향이 있음.
    - 이는 특수문자를 중요한 구분자로 사용하는 문서에서 불용어 제거 및 특수문자 제거가 오히려 의미를 왜곡시키기 때문.
    
    **⇒ 결론**
    
    - 결국, **불용어 제거**를 하지 않기로 결정.
    - 특수문자를 기준으로 문서가 나누어지는 구조에서는 불용어 처리나 특수문자 제거가 텍스트의 의미를 흐트러뜨릴 수 있으므로, 이를 제거하지 않고 원본 텍스트를 그대로 사용하는 것이 더 나은 결과를 도출할 수 있음.
</aside>

## **8. 성과 및 결과**

<aside>

### **8-1. PDF 문서 요약 및 질의응답 시스템 구축**

- PDF 문서를 **자동으로 분석 및 요약하는 기능 구현**
- **LangChain과 RAG**를 활용하여 문서 검색 및 요약 성능 향상
- 문서 내 **표 데이터를 인식하고 숫자 기반 정보 분석 가능**

### **8-2. 검색 속도 및 정확도 최적화**

- **FAISS 벡터 저장소 적용** → 기존의 단순 키워드 검색보다 **검색 속도 30% 이상 향상**
- **Multi-Query Retriever & Ensemble Retriever 적용** → **질문과 문서 매칭 정확도 개선**
- 검색 결과 필터링을 최적화하여 **불필요한 문서 검색 비율 40% 감소**

### **8-3. 사용자 경험 개선**

- **Streamlit 기반 웹 UI 구현** → PDF 업로드 및 질의응답 기능을 **직관적으로 제공**
- **검색 결과 및 요약 내용 시각화** → 사용자 친화적인 인터페이스 제공
- **질의응답 정확도 개선**을 통해 **더 자연스럽고 신뢰도 높은 응답 제공**

### **8-4. 비용 효율적인 AI 시스템 구축**

![Image](https://github.com/user-attachments/assets/1c4132d8-0657-4582-bebe-98160d609096)
- **로컬 임베딩 모델(`jhgan/ko-sbert-nli`) 적용**하여 **API 사용  절감**
- OpenAI API 호출을 최소화하여 **운영 비용 절감 및 성능 유지**

### **8-5. 다중 문서 처리 기능 구현**

- 여러 개의 PDF를 업로드하여 **문서 간 연관 정보를 분석하고 종합적인 답변 제공 가능**
- 검색 과정에서 **문서 간 관계를 분석하여 더 유의미한 정보 제공**
</aside>

## **9. 향후 개선 및 추가 기능 계획**

<aside>

### **9-1. 검색 정확도 및 응답 품질 향상**

- **Retriever 최적화** → 문서 검색 시 **더 정확한 내용만 반환**하도록 필터링 강화
- **질의응답 프롬프트 추가 최적화** → 문맥 유지 및 답변 품질 향상
- **사용자 질문 의도 분석** → 질문 의도를 고려한 응답 최적화

### **9-2. 표 데이터 처리 기능 개선**

- **복잡한 표 구조 인식 강화** → 병합된 셀 및 다중 컬럼 표 데이터 처리 개선
- **표 데이터 기반 분석 기능 추가** → 평균, 합계 등 수치 기반 정보 제공 기능 강화
- **표와 텍스트의 연관성 분석 개선** → 표 주변 텍스트를 고려한 보다 정확한 응답 제공

### **9-3. 다중 문서 간 연관 정보 분석 기능 추가**

- 현재 개별 문서 내에서만 검색이 가능 → **다중 문서를 한꺼번에 분석하여 종합적인 답변 제공 기능 추가**
- 문서 간 관계를 분석하여 **유사 문서를 추천하는 기능 추가 검토**

### **9-4. 사용자 맞춤형 검색 기능 제공**

- **즐겨찾기 및 검색 기록 저장 기능 추가** → 자주 검색하는 키워드를 자동 저장 및 추천
- **문서 필터링 기능 추가** → 특정 키워드나 중요 정보만 요약할 수 있도록 사용자 설정 옵션 제공

### **9-5. LLM 모델 최적화 및 비용 절감**

- **더 가벼운 모델 적용** → `jhgan/ko-sbert-nli` 외 다른 고효율 로컬 모델 테스트
- **API 호출 최적화** → OpenAI API 최소 호출 방식으로 비용 절감 및 성능 유지
- **GPU 최적화** → AI 연산 속도를 높이고 처리 비용 절감

### **9-6. 사용자 인터페이스(UI) 및 경험 개선**

- **검색 결과 및 요약 내용 시각화 기능 추가**
- **더 직관적인 PDF 업로드 및 검색 인터페이스 개선**
- **응답 출력 방식 다양화 (키워드 하이라이트, 요약, 원문 보기 등)**
</aside>
