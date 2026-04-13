---
layout: theory
title: "머신러닝/딥러닝"
description: "ML 알고리즘 원리, 딥러닝 구조, PyTorch·TensorFlow 실습"
permalink: /theory/ml-dl/
---

## 머신러닝과 딥러닝이란?

머신러닝(ML)은 데이터로부터 패턴을 학습하여 예측이나 분류를 수행하는 AI 기술입니다. 딥러닝(DL)은 인공신경망을 여러 층으로 쌓아 복잡한 패턴을 학습하는 머신러닝의 한 분야입니다.

---

## 주요 학습 주제

### 🎯 머신러닝 기초
- 지도학습 / 비지도학습 / 강화학습
- 훈련/검증/테스트 데이터 분리
- 과적합(Overfitting)과 정규화
- 교차 검증(Cross Validation)

### 📐 주요 알고리즘
- **분류**: 로지스틱 회귀, SVM, KNN, 결정 트리, 랜덤 포레스트
- **회귀**: 선형 회귀, Ridge, Lasso
- **클러스터링**: K-Means, DBSCAN
- **앙상블**: Boosting (XGBoost, LightGBM), Bagging

### 🧠 딥러닝 개념
- 인공신경망 구조 (입력층, 은닉층, 출력층)
- 활성화 함수 (ReLU, Sigmoid, Softmax)
- 역전파(Backpropagation)와 경사하강법
- 배치 정규화(Batch Normalization)

### 🔬 딥러닝 아키텍처
- CNN (Convolutional Neural Network) — 이미지 처리
- RNN, LSTM — 시계열/텍스트
- Transformer — 자연어 처리
- 오토인코더(Autoencoder)

### ⚙️ PyTorch 실습
- 텐서(Tensor) 기본 연산
- `nn.Module`로 모델 정의
- DataLoader와 Dataset
- 학습 루프 구현

### 📊 모델 평가
- 분류: Accuracy, Precision, Recall, F1, ROC-AUC
- 회귀: MAE, MSE, RMSE, R²
- 혼동 행렬(Confusion Matrix)

---

## 학습 로드맵

```
수학 기초 (선형대수, 통계, 미적분)
        ↓
머신러닝 기초 (Scikit-learn)
        ↓
딥러닝 이론 (신경망, 역전파)
        ↓
PyTorch / TensorFlow 실습
        ↓
특화 분야 (CV, NLP, 강화학습)
```

---

> 각 알고리즘의 구현 코드와 실험 결과를 이 폴더에 추가해보세요.
