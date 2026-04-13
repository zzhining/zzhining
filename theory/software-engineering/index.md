---
layout: theory
title: "소프트웨어엔지니어링"
description: "설계 패턴, 클린코드, Git 전략, DevOps, 테스트 등 SW 공학 지식"
permalink: /theory/software-engineering/
---

## 소프트웨어 엔지니어링이란?

소프트웨어 엔지니어링은 체계적이고 규율화된 방법으로 소프트웨어를 개발, 운용, 유지보수하는 학문입니다. 좋은 코드를 작성하고 협업하며 지속 가능한 시스템을 만드는 방법을 다룹니다.

---

## 주요 학습 주제

### 🧹 클린 코드
- 의미 있는 네이밍 규칙
- 함수는 한 가지 일만 (SRP)
- 주석은 코드가 설명하지 못할 때만
- 리팩토링 기법

### 🏛️ 설계 원칙 (SOLID)
- **S**ingle Responsibility Principle — 단일 책임 원칙
- **O**pen/Closed Principle — 개방-폐쇄 원칙
- **L**iskov Substitution Principle — 리스코프 치환
- **I**nterface Segregation Principle — 인터페이스 분리
- **D**ependency Inversion Principle — 의존성 역전

### 🎨 디자인 패턴
- 생성 패턴: Singleton, Factory, Builder
- 구조 패턴: Adapter, Decorator, Facade
- 행위 패턴: Observer, Strategy, Command

### 🔧 Git & 협업
- Git 브랜치 전략 (Git Flow, GitHub Flow)
- 의미 있는 커밋 메시지 작성
- PR(Pull Request) 리뷰 문화
- `.gitignore`, `.gitattributes`

### 🧪 테스트
- 유닛 테스트 (pytest)
- 통합 테스트
- TDD (테스트 주도 개발)
- 테스트 커버리지

### 🚀 DevOps 기초
- CI/CD 파이프라인 (GitHub Actions)
- Docker 컨테이너 기초
- 환경 변수와 설정 관리
- 로깅과 모니터링

---

## 좋은 코드의 기준

| 기준 | 설명 |
|------|------|
| 가독성 | 타인이 쉽게 이해할 수 있는 코드 |
| 유지보수성 | 변경이 쉽고 사이드이펙트가 적은 코드 |
| 테스트 가능성 | 단위 테스트가 쉬운 구조 |
| 성능 | 불필요한 연산이 없는 효율적인 코드 |
| 일관성 | 팀 컨벤션을 따르는 코드 |

---

> 설계 패턴 구현 예제와 리팩토링 사례를 이 폴더에 추가해보세요.
