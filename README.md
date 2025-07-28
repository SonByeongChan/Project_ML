# 🍷 Wine Quality Analysis Project

## 📌 프로젝트 개요
- **목적**: 화이트 와인의 화학 성분 데이터를 기반으로 품질을 예측
- **데이터 출처**: UCI Machine Learning Repository
- **데이터 파일**
  - `winequality-white.csv` (4,898개 샘플)
  - `winequality-red.csv` (1,598개 샘플)

---

## 🧪 데이터셋 정보

| Feature                 | Description           |
|------------------------|-----------------------|
| fixed acidity          | 고정산도               |
| volatile acidity       | 휘발산도               |
| citric acid            | 구연산                 |
| residual sugar         | 잔당                   |
| chlorides              | 염화물                 |
| free sulfur dioxide    | 자유 이산화황          |
| total sulfur dioxide   | 총 이산화황            |
| density                | 밀도                   |
| pH                     | 산도                   |
| sulphates              | 황산염                 |
| alcohol                | 알코올 함량            |
| quality                | 품질 등급 (3~9점)      |

---

## 🔍 분석 프로젝트 구성

### 1. 와인 등급 분류 (Multi-class Classification)
- `wine_white_class.ipynb`
- **목표**: 품질을 3~9점으로 예측
- **이슈**: 클래스 불균형 → SMOTE로 해결
- **최고 성능**: Random Forest (SMOTE 적용) → **Accuracy: 69.8%**

### 2. 와인 맛 분류 (Binary Classification)
- `wine_white_taste.ipynb`
- **목표**: 좋은 맛(1), 나쁜 맛(0) 이진 분류 (기준: quality > 6)
- **최고 성능**: Random Forest (SMOTE 적용) → **Accuracy: 89.5%**

---

## 🤖 사용된 모델들

- Random Forest (Best Performance)
- XGBoost (Tuned)
- Logistic Regression
- SVM
- KNN
- Naive Bayes
- Decision Tree
- Voting Classifier (Ensemble)

---

## 📈 성능 요약

### 등급 분류 (다중 분류)
- Accuracy: 69.8%

### 맛 분류 (이진 분류)
- Accuracy: 89.5%
- Precision: 90% (좋은 맛), 86% (나쁜 맛)
- Recall: 97% (좋은 맛), 66% (나쁜 맛)

---

## 🛠️ 기술 스택 및 처리 방법

- **전처리**: 결측치 확인, 특성 중요도 분석, 시각화
- **불균형 처리**: SMOTE 적용
- **모델 튜닝**: GridSearchCV
- **앙상블 기법**: Voting Classifier
- **모델 저장**: `joblib.dump()`
  - `random_forest_model_with_smote.pkl` (19MB)
  - `random_forest_model_with_smote1.pkl` (73MB)

---

## 🎯 프로젝트 강점

- 전체 머신러닝 파이프라인 구현
- 다양한 모델 실험 및 비교
- 시각화 및 분석 기반 의사결정
- 저장 가능한 모델 제공

---

## 🔧 개선 가능 포인트

- 특성 엔지니어링 강화
- 교차 검증으로 일반화 성능 확보
- 하이퍼파라미터 탐색 범위 확대
- 다양한 앙상블 기법 도입

---

## 🧠 회고

실용적인 도메인(와인 품질 예측)에 대해 체계적인 분석과 성능 개선을 실현했습니다. 특히 SMOTE 적용과 앙상블 학습을 통해 실무적으로 적용 가능한 구조를 구성했습니다.
