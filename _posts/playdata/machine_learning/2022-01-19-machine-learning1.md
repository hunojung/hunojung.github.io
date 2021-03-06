---
laout : single
title: "머신러닝 시작하기"
excerpt : "머신러닝과 파이썬, 사이킷런"
categories :
- Machine Learning
tags :
- [Playdata , Python, Machine Learning]
toc: true #Table of contents 옆에 목록이 생성됨
toc_sticky: true #toc가 화면을 따라 내려옴
toc_label: 목차 #toc 상단에 써있는 제목

date: 2022-01-19
last_modified_at: 2022-01-19
---

머신러닝은 명시적인 프로그래밍 없이 컴퓨터가 학습하는 능력을 갖추게 하는 연구 분야다.

## 머신러닝이 유용한 분야 예시

- 기존 솔루션으로는 많은 수동 조정과 규칙이 필요한 문제
- 전통적인 방법으로는 전혀 해결 방법이 없는 복잡한 문제 ( 음성인식, 얼굴인식 )
- 변화하는 환경에 적응해야 하는 문제
- 복잡한 문제와 대량의 데이터에서 통찰 얻기(데이터 마이닝)

## 머신러닝과 데이터 마이닝

- 데이터 마이닝은 데이터 안에서 알려지지 않은 속성을 찾는 것이 주 목적
- 머신 러닝은 데이터의 알려진 속성들을 학습하여 예측 모델을 만드는것이 목적

## 파이썬과 머신 러닝

- 장점
  - 데이터 분석( 적재, 시각화, 통계 등) 측면이나 범용적( 그래픽 처리, 웹 서비스 등) 측면에서 편리
  - 유수의 딥러닝 Framework, Tutorial이 파이썬으로 작성되어 제공 됨

- 단점
  - 속도가 느림

## 사이킷런(scikit-learn)

머신러닝에 필요한 다양한 알고리즘과 편리한 프레임워크, API 제공

### 사이킷런 설계 철학

- 일관성
  - 추정기estimator : 데이터셋을 기반으로 일련의 모델 파라미터들을 추정하는 객체
  - fit(X, [y])
  - 변환기transformer : 데이터셋을 변환하는 추정기
  - transform(X), fit_transform(X, [y])
  - 예측기predictor : 주어진 데이터셋에 대해 예측을 만들 수 있는 추정기
  - predict(X), score(X, y)

- 검사가능: 모델 파라미터와 하이퍼파라미터를 공개 변수로 접근 가능
- 클래스 남용 방지: 기본 데이터 타입으로 넘파이 배열을 사용
- 조합성 : Pipeline 클래스
- 합리적 기본값 : 모든 매개변수에 합리적인 기본값을 둠

## 머신러닝 분류 예측 프로세스

1. 데이터 세트 분리
  - 데이터를 훈련 데이터와 테스트 데이터로 분리

2. 모델 학습
  - 훈련 데이터를 기반으로 머신러닝 알고리즘을 적용해 모델 학습

3. 예측 수행
  - 훈련된 머신 러닝 모델을 이용해 테스트 데이터 분류를 예측

4. 평가
  - 예측된 결과값과 테스트 데이터의 실제 결과값을 비교해 머신 러닝 모델의 성능을 평
