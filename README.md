# GDGoC-Success-Seollyongdan-aiml


본 프로젝트는 2025 GDGoc 숙명여대x성신여대x성공회대 연합 프로젝트로, 서울시 공공 데이터 활용 지역구별 정보 제공 및 커뮤니티 제공 앱의 ai 기능 레포지토리 입니다.
서울시와 관련 데이터를 전처리하고, 클러스터링 기반의 동네 추천 시스템을 구현하는 것을 목표로 합니다. 
세 개의 주요 Jupyter Notebook 파일로 구성되어 있으며, 각각의 역할은 다음과 같습니다:

---

## 파일 구성

### 1. `홈_데이터_제공.ipynb`
- **목적**: 주거 관련 원본 데이터셋을 수집하고, 기초 탐색 및 통계 분석 수행
- **주요 내용**:
  - 평균 임대료, 체육시설 수, 범죄 발생 건수 등의 시각화
  - 동별 인프라 수준 및 환경 분석
- **출력**:
  - 동별 생활 지표 정리 결과

### 2. `dataPreprocessing.ipynb`
- **목적**: 분석 및 추천을 위한 데이터 정제 및 전처리 수행
- **주요 내용**:
  - Null 처리, 스케일링, 변수 통합 및 파생변수 생성
  - 클러스터링 알고리즘 적용을 위한 입력 포맷 생성
- **출력**:
  - 정제된 데이터셋 (클러스터링용)

### 3. `clustering_recommend.ipynb`
- **목적**: KMeans 클러스터링을 활용한 동네 유형 분류 및 추천 시스템 구현
- **주요 내용**:
  - 최적 K 탐색 (Elbow method 등)
  - 군집별 특성 분석
  - 유사 동네 추천 함수 구현
- **출력**:
  - 각 동의 클러스터 라벨
  - 입력 기준과 유사한 동네 리스트

---

## 기술 스택

- Python
- Pandas, NumPy
- Scikit-learn
- Matplotlib, Seaborn
- Jupyter Notebook

---

## 참고 사항

- 데이터 출처는 서울시 공공데이터를 기반으로 합니다.
- 클러스터링은 정량적 지표(임대료, 체육시설 수, 범죄 등)를 기준으로 수행됩니다.
- 추천 결과는 사용자의 설정 조건과 가장 유사한 클러스터에 속하는 동 목록을 반환합니다.
- 사용 데이터 및 개발 과정 등은 [AI 개발 페이지](https://silver-milk-150.notion.site/AIML-17950e545d7b80759418cab3ebed7fd8?pvs=74) 를 참고해주세요.

