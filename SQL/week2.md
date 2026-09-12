# 📘 SQL_BASIC 2주차 정규 과제

SQL_BASIC 정규 과제는 매주 정해진 분량의 `초보자를 위한 BigQuery(SQL) 입문` 강의를 듣고, 핵심 개념을 정리한 뒤 간단한 SQL 문제를 직접 풀어보는 방식으로 진행합니다.

이번 주는 저장된 데이터를 확인하는 방법과 `SELECT`, `FROM`, `WHERE`의 기본 구조를 학습합니다.

완성된 과제는 Github에 업로드하고, 링크를 스프레드시트 'SQL' 시트에 입력해 제출해주세요.

**👀 수행 인증란은 필수입니다.**

---

## 📚 SQL_BASIC_2nd_TIL

### 섹션 3. 데이터 탐색 - 조건, 추출, 요약

### 2-2. 저장된 데이터 확인하기(데이터베이스, 데이터 웨어하우스, ERD)

### 2-3. 데이터 탐색(SELECT, FROM, WHERE)

---

## ✨ 선택 강의

- 2-4. SELECT 연습 문제: SELECT, FROM, WHERE를 더 연습하고 싶을 때 선택 수강

---

## 🏁 전체 강의 수강 계획

| 주차 | 필수 강의 범위 | 선택 강의 | 완료 여부 |
| --- | --- | --- | --- |
| 1주차 | 1-1 ~ 2-1 | 1 | ✅ |
| 2주차 | 2-2 ~ 2-3 | 2-4 | ✅ |
| 3주차 | 2-5, 2-7 ~ 2-8 | 2-6 | 🍽️ |
| 4주차 | 3-2 ~ 4-3 | 3-4 | 🍽️ |
| 5주차 | 4-4 ~ 4-6 | 4-5, 4-7 | 🍽️ |
| 6주차 | 5-2 ~ 5-5 | 5-6 | 🍽️ |
| 7주차 | 필수 강의 없음 | 6-2, 6-3, 6-4, 6-5 | 🍽️ |

---

<br>

<!-- 여기까진 그대로 둬 주세요-->

---

# 1️⃣ 개념 정리

아래 키워드 중 중요하다고 생각한 개념을 2개 이상 골라 짧게 정리해주세요. 3개보다 더 많이 정리하고 싶다면 자유롭게 항목을 추가해도 좋습니다.

이번 주 키워드:
- SELECT
- FROM
- WHERE
- 조건식
- ORDER BY
- LIMIT
- 테이블 구조 확인

## 01.

```
개념 이름: SELECT
개념 설명: SELECT는 테이블에서 어떤 열(Column)을 가져올지 지정하는 명령어이다.
예시 쿼리: SELECT id AS pekemon_id, kor_name,type1, total
```

## 02.

```
개념 이름: FROM
개념 설명: FROM은 데이터를 가져올 테이블을 지정한다.
예시 쿼리: FROM basic.poketmon
```

## (선택) 03.

```
개념 이름:
개념 설명:
헷갈린 점:
```

---

# 2️⃣ 수행 인증란

아래 중 하나 이상을 첨부해주세요.

- 강의 수강 화면 캡처 
- 문제 풀이 정답 화면 캡처
- SQL 실행 결과 화면 캡처

  <img width="1887" height="897" alt="SQL 과제 증명" src="https://github.com/user-attachments/assets/4a853140-fd07-45ed-ac89-1173cf3e3c0d" />


---

# 3️⃣ 확인 문제

프로그래머스는 로그인이 필요하므로, 로그인 후 문제 풀이를 진행해주세요.

## 🧩 문제 1

문제 링크: [모든 레코드 조회하기](https://school.programmers.co.kr/learn/courses/30/lessons/59034)

풀이 과정:

```
- 테이블에서 확인한 컬럼: ANIMAL_ID , ANIMAL_TYPE	, DATETIME ,	INTAKE_CONDITION	, NAME ,	SEX_UPON_INTAKE
- SELECT와 FROM을 작성한 방식:
SELECT *
FROM ANIMAL_INS
ORDER BY ANIMAL_ID;
- 새로 배운 점: SELECT *를 사용하면 테이블의 모든 컬럼을 조회할 수 있고, ORDER BY를 사용하면 원하는 컬럼을 기준으로 데이터를 정렬할 수 있다는 점을 배웠다.
```

<img width="1387" height="555" alt="SQL 과제 증명 1" src="https://github.com/user-attachments/assets/43129721-b715-46cd-9056-e3b76c757ccd" />

## 🧩 문제 2

문제 링크: [아픈 동물 찾기](https://school.programmers.co.kr/learn/courses/30/lessons/59036)

풀이 과정:

```
- 문제에서 요구한 조건: 보호소에 들어온 동물 중 상태가 Sick인 동물만 골라 ANIMAL_ID와 NAME을 조회하고, 결과를 ANIMAL_ID 순으로 정렬해야 한다
- WHERE 절로 옮긴 방식:
SELECT ANIMAL_ID, NAME
FROM ANIMAL_INS
WHERE INTAKE_CONDITION = 'Sick'
ORDER BY ANIMAL_ID;
- 정렬 기준이 있다면 사용한 기준: ANIMAL_ID
- 새로 배운 점: WHERE절을 사용하면 특정 조건에 맞는 데이터만 조회할 수 있고, 문자열 조건을 지정할 때는 'Sick'처럼 작은따옴표를 사용한다.
```

<img width="972" height="462" alt="2" src="https://github.com/user-attachments/assets/39eff5fb-aca1-4642-8d39-3cd9f145b6bb" />


---

# 4️⃣ 이번 주 회고

```
1. SELECT, FROM, WHERE 중 가장 헷갈린 개념: SELECT와 WHERE의 역할이 헷갈렸다. SELECT는 어떤 컬럼을 가져올지 정하고, WHERE은 어떤 조건의 행을 가져올지 정한다는 차이를 배웠다.
2. 문제를 풀 때 가장 자주 확인하게 된 부분: 문제에서 어떤 컬럼을 출력해야 하는지와 어떤 조건으로 데이터를 걸러야 하는지를 가장 자주 확인했다
3. 다음 주 문제 풀이에서 의식하고 싶은 습관: SQL문을 바로 작성하기 전에 먼저 출력할 컬럼, 사용할 테이블, 조건, 정렬 기준을 순서대로 정리한 뒤 쿼리를 작성하는 습관을 들이고 싶다.
```

수고하셨습니다!
