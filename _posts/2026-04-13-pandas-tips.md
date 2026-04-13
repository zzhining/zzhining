---
layout: post
title: "Pandas 데이터 분석 실무 팁 모음"
date: 2026-04-13
category: "데이터 분석"
tags: [Python, Pandas, 데이터분석, EDA]
excerpt: "Pandas를 더 효율적으로 사용하기 위한 실무 팁들을 모았습니다. groupby 활용, 결측값 처리, 메모리 최적화까지 정리했습니다."
---

## 들어가며

Pandas를 처음 배울 때는 기본 기능만 사용하게 됩니다. 하지만 실무에서 대용량 데이터를 다루다 보면 더 효율적인 방법이 필요해집니다. 오늘은 제가 자주 사용하는 Pandas 팁들을 정리해보았습니다.

---

## 1. 데이터 탐색 빠르게 하기

```python
import pandas as pd

df = pd.read_csv('data.csv')

# 기본 정보 한번에 보기
df.info()
df.describe()
df.head()

# 결측값 현황
df.isnull().sum()
df.isnull().mean() * 100  # 결측율(%)

# 중복 확인
df.duplicated().sum()
```

---

## 2. groupby 실전 활용

```python
# 기본 집계
df.groupby('category')['sales'].agg(['sum', 'mean', 'count'])

# 여러 컬럼 동시 집계
df.groupby('category').agg({
    'sales': ['sum', 'mean'],
    'quantity': 'sum',
    'profit': 'mean'
})

# 커스텀 함수 적용
df.groupby('category')['sales'].apply(lambda x: x.nlargest(3))
```

---

## 3. 조건부 데이터 변환

```python
# np.where (삼항 연산자)
import numpy as np
df['grade'] = np.where(df['score'] >= 80, 'A', 'B')

# pd.cut 으로 구간 나누기
df['age_group'] = pd.cut(df['age'], 
                          bins=[0, 20, 30, 40, 100],
                          labels=['10대', '20대', '30대', '40대+'])

# map으로 값 변환
mapping = {'M': '남성', 'F': '여성'}
df['gender_kor'] = df['gender'].map(mapping)
```

---

## 4. 메모리 최적화

대용량 데이터를 다룰 때 메모리를 절약하는 방법입니다.

```python
# 데이터 타입 변환으로 메모리 절약
df['id'] = df['id'].astype('int32')          # int64 → int32
df['category'] = df['category'].astype('category')  # 반복값은 category 타입

# 청크(chunk) 단위로 읽기
for chunk in pd.read_csv('large_file.csv', chunksize=10000):
    process(chunk)

# 메모리 사용량 확인
df.memory_usage(deep=True).sum() / 1024**2  # MB 단위
```

---

## 5. 자주 쓰는 실용 패턴

```python
# 특정 컬럼의 유니크 값과 빈도
df['category'].value_counts(normalize=True)

# 두 DataFrame 비교
df1.compare(df2)

# 날짜 처리
df['date'] = pd.to_datetime(df['date'])
df['year'] = df['date'].dt.year
df['month'] = df['date'].dt.month
df['day_of_week'] = df['date'].dt.day_name()

# pivot table
pd.pivot_table(df, 
               values='sales',
               index='region', 
               columns='category',
               aggfunc='sum',
               fill_value=0)
```

---

## 마무리

> **팁**: `df.pipe()` 메서드를 활용하면 데이터 전처리 파이프라인을 읽기 쉽게 체이닝할 수 있습니다.

```python
result = (df
          .pipe(remove_duplicates)
          .pipe(fill_missing_values)
          .pipe(normalize_columns)
          .pipe(filter_outliers))
```

더 궁금한 Pandas 기능이 있다면 댓글로 알려주세요!
