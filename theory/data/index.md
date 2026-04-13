---
layout: theory
title: "데이터"
description: "데이터베이스, SQL, 데이터 파이프라인, 데이터 엔지니어링 기초"
permalink: /theory/data/
---

## 데이터 엔지니어링이란?

데이터 엔지니어링은 데이터를 수집, 저장, 처리, 변환하는 인프라와 파이프라인을 구축하는 분야입니다. 데이터 분석가와 과학자가 고품질 데이터를 활용할 수 있도록 기반을 마련합니다.

---

## 주요 학습 주제

### 🗄️ 데이터베이스 기초
- 관계형 DB (RDBMS) vs 비관계형 DB (NoSQL)
- 데이터 모델링과 정규화
- 인덱스(Index)와 성능 최적화
- 트랜잭션(ACID)

### 📝 SQL 핵심
- `SELECT`, `WHERE`, `GROUP BY`, `HAVING`
- `JOIN` (INNER, LEFT, RIGHT, FULL)
- 서브쿼리와 CTE (`WITH` 절)
- 윈도우 함수 (`ROW_NUMBER`, `RANK`, `LAG`, `LEAD`)
- 집계 함수와 분석 함수

### 📦 데이터 저장소
- PostgreSQL 실습
- MySQL / MariaDB
- SQLite (Python 연동)
- MongoDB 기초 (NoSQL)

### 🔄 데이터 파이프라인
- ETL vs ELT 개념
- 배치 처리 vs 스트리밍 처리
- Apache Airflow 기초
- 데이터 품질 관리

### ☁️ 클라우드 데이터
- AWS S3, RDS 기초
- Google BigQuery
- 데이터 웨어하우스 개념
- 데이터 레이크 아키텍처

---

## SQL 핵심 패턴

```sql
-- 윈도우 함수 예시
SELECT
    name,
    score,
    RANK() OVER (PARTITION BY department ORDER BY score DESC) AS rank
FROM employees;

-- CTE 예시
WITH monthly_sales AS (
    SELECT
        DATE_TRUNC('month', order_date) AS month,
        SUM(amount) AS total
    FROM orders
    GROUP BY 1
)
SELECT * FROM monthly_sales ORDER BY month;
```

---

> SQL 쿼리 예제와 데이터 파이프라인 구현 내용을 이 폴더에 추가해보세요.
