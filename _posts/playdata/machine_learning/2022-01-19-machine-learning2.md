---
laout : single
title: "붓꽃 품종 예측하기"
excerpt : "붓꽃 품종 예측하기"
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

첫 번째 머신러닝 붓꽃 품종 예측하기

- 붓꽃 데이터 세트로 붓꽃의 품종을 분류(Classification)
- 데이터 세트의 특성(Feature)은 꽃잎의 길이와 너비, 꽃받침의 길이와 너비
- 다양한 붓꽃의 특성들과 그에 따른 붓꽃 종류로 학습 후 새로운 붓꽃 데이터가 어떤 붓꽃 종류(Class)일지 예측
- 품종은 Setosa, Vesicolor, Virginica

## 데이터 적재

사이킷런 버전 확인 및 모듈 로딩
```
import sklearn
sklearn.__version__ # '0.24.2'
```

```
from sklearn.datasets import load_iris
from sklearn.neighbors import KNeighborsClassifier
from sklearn.model_selection import train_test_split
import numpy as np
import pandas as pd
```

붓꽃 데이터 세트 로딩
```
iris_dataset = load_iris()
type(iris_dataset) # sklearn.utils.Bunch
```

붓꽃 데이터 살펴보기
```
In  : iris_dataset.keys()

Out : dict_keys(['data', 'target', 'frame', 'target_names', 'DESCR', 'feature_names', 'filename'])
```

```
In  : iris_dataset["data"].shape

Out : (150, 4)
```

target은 붓꽃의 품종

```
In  : iris_dataset["target_names"]

Out : array(['setosa', 'versicolor', 'virginica'], dtype='<U10')
```

```
In  : iris_dataset["feature_names"]

Out : ['sepal length (cm)',
       'sepal width (cm)',
       'petal length (cm)',
       'petal width (cm)']
```

DESCR : 데이터세트에 대한 설명과 값

```
iris_dataset["DESCR"]
```

## 데이터 시각화(Visualize)

```
iris_df = pd.DataFrame( data=iris_dataset["data"], columns=iris_dataset["feature_names"])
iris_df
```

<img src="/assets/post_photo/machine-learning/iris1.jpg" width="70%">

```
# pd.plotting.scatter_matrix
# target이 3가지여서 마커도 3종류로 나타난다
iris_df.plot(kind="scatter", c=iris_dataset["target"], x=iris_df.columns[0], y=iris_df.columns[1] , cmap="plasma")
```

<img src="/assets/post_photo/machine-learning/iris2.jpg" width="70%">
