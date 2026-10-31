# 📘 SQL_BASIC 6주차 정규 과제

SQL_BASIC 정규 과제는 매주 정해진 분량의 `초보자를 위한 BigQuery(SQL) 입문` 강의를 듣고, 핵심 개념을 정리한 뒤 간단한 SQL 문제를 직접 풀어보는 방식으로 진행합니다.

이번 주는 SQL 입문 과정의 핵심 고비인 `JOIN`을 학습합니다.

JOIN은 여러 테이블을 연결해서 분석 질문에 답하기 위해 반드시 필요한 개념입니다. 이번 주 과제에서는 정답 코드뿐 아니라 **어떤 테이블을 어떤 키로 연결했는지**를 꼭 기록해주세요.

완성된 과제는 Github에 업로드하고, 링크를 스프레드시트 'SQL' 시트에 입력해 제출해주세요.

**👀 수행 인증란은 필수입니다.**

---

## 📚 SQL_BASIC_6th_TIL

### 섹션 6. 다량의 자료를 연결 : JOIN

### 5-2. JOIN 이해하기

### 5-3. 다양한 JOIN 방법

### 5-4. JOIN 쿼리 작성하기

### 5-5. JOIN을 처음 공부할 때 헷갈리는 부분

---

## ✨ 선택 강의

- 5-6. JOIN 연습문제: JOIN 문제를 더 연습하고 싶을 때 선택 수강

---

## 🏁 전체 강의 수강 계획

| 주차 | 필수 강의 범위 | 선택 강의 | 완료 여부 |
| --- | --- | --- | --- |
| 1주차 | 1-1 ~ 2-1 | 1 | ✅ |
| 2주차 | 2-2 ~ 2-3 | 2-4 | ✅ |
| 3주차 | 2-5, 2-7 ~ 2-8 | 2-6 | ✅ |
| 4주차 | 3-2 ~ 4-3 | 3-4 | ✅ |
| 5주차 | 4-4 ~ 4-6 | 4-5, 4-7 | ✅ |
| 6주차 | 5-2 ~ 5-5 | 5-6 | ✅ |
| 7주차 | 필수 강의 없음 | 6-2, 6-3, 6-4, 6-5 | 🍽️ |

---

<br>

<!-- 여기까진 그대로 둬 주세요-->

---

# 1️⃣ 개념 정리

아래 키워드 중 중요하다고 생각한 개념을 2개 이상 골라 짧게 정리해주세요. 3개보다 더 많이 정리하고 싶다면 자유롭게 항목을 추가해도 좋습니다.

이번 주 키워드:
- JOIN
- INNER JOIN
- LEFT JOIN
- JOIN key
- alias
- NULL
- 다중 JOIN

## 01.

```
개념 이름:
JOIN

개념 설명:
JOIN은 두 개 이상의 테이블을 연결하여 하나의 결과로 조회하는 SQL 기능이다.

데이터베이스에서는 고객 정보, 주문 정보, 상품 정보 등을 각각 별도의 테이블로 관리하는 경우가 많다. JOIN을 사용하면 서로 다른 테이블에 저장된 데이터를 연결하여 필요한 정보를 함께 확인할 수 있다.

예시 쿼리:
SELECT *
FROM Customers
JOIN Orders
ON Customers.customer_id = Orders.customer_id;
```

## 02.

```
개념 이름:
INNER JOIN

개념 설명:
INNER JOIN은 두 테이블에서 JOIN 조건에 일치하는 데이터만 조회하는 방식이다.

즉, 두 테이블에 공통으로 존재하는 데이터를 연결한다. 한쪽 테이블에만 존재하고 다른 테이블과 연결되지 않는 데이터는 결과에 포함되지 않는다.

예시 쿼리:
SELECT Customers.name, Orders.order_date
FROM Customers
INNER JOIN Orders
ON Customers.customer_id = Orders.customer_id;
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
- JOIN 문제 풀이 정답 화면 캡처
- JOIN 전후 결과 row 수를 비교한 캡처 또는 메모
<img width="1912" height="916" alt="스크린샷 2026-10-31 203047" src="https://github.com/user-attachments/assets/2aa408fe-b2bd-4973-8645-2e0bdf5dd727" />

---

# 3️⃣ 확인 문제

프로그래머스는 로그인이 필요하므로, 로그인 후 문제 풀이를 진행해주세요.

## 🧩 문제 1

문제 링크: [조건에 맞는 도서와 저자 리스트 출력하기](https://school.programmers.co.kr/learn/courses/30/lessons/144854)

풀이 과정:

```
- 사용한 테이블: `BOOK`, `AUTHOR`
- JOIN key: `BOOK.AUTHOR_ID = AUTHOR.AUTHOR_ID`
- 날짜를 출력한 형식: `YYYY-MM-DD` (예: `2021-02-05`)
```

<img width="907" height="436" alt="image" src="https://github.com/user-attachments/assets/c1e56b98-fe0c-42bb-9ee2-d426a9d5a8c1" />


## 🧩 문제 2

문제 링크: [상품 별 오프라인 매출 구하기](https://school.programmers.co.kr/learn/courses/30/lessons/131533)

풀이 과정:

```
- 연결한 테이블: `PRODUCT`, `OFFLINE_SALE`
- JOIN key: `PRODUCT.PRODUCT_ID = OFFLINE_SALE.PRODUCT_ID`
- 집계한 값: 상품코드별 총매출액 (`판매가 × 판매량`의 합계, `SUM(PRICE * SALES_AMOUNT)`)
```

<img width="1032" height="472" alt="image" src="https://github.com/user-attachments/assets/50bbf5b7-c721-4ae2-8790-4f46a3b4da0d" />


## 🧩 문제 3

문제 링크: [없어진 기록 찾기](https://school.programmers.co.kr/learn/courses/30/lessons/59042)

풀이 과정:

```
기준이 되는 왼쪽 테이블: ANIMAL_OUTS (입양 기록 테이블)
LEFT JOIN이 필요한 이유: 입양 기록은 있지만 보호소 입소 기록이 없는 동물도 조회해야 하기 때문.
NULL이 발생하는 경우: ANIMAL_OUTS에는 동물의 입양 기록이 있지만, ANIMAL_INS에는 해당 동물의 입소 기록이 없어 두 테이블이 연결되지 않는 경우.
```

<img width="796" height="352" alt="image" src="https://github.com/user-attachments/assets/ea1a1fb7-02b1-4395-83f1-81d48a546ace" />


## 🧩 문제 4

문제 링크: [있었는데요 없었습니다](https://school.programmers.co.kr/learn/courses/30/lessons/59043)

풀이 과정:

```
사용한 테이블: ANIMAL_INS, ANIMAL_OUTS
JOIN key: ANIMAL_INS.ANIMAL_ID = ANIMAL_OUTS.ANIMAL_ID
비교한 날짜 컬럼: ANIMAL_OUTS.DATETIME(입양일) < ANIMAL_INS.DATETIME(보호 시작일)
정렬 기준: 보호 시작일(ANIMAL_INS.DATETIME) 기준 오름차순(ASC)
```

<img width="843" height="311" alt="image" src="https://github.com/user-attachments/assets/87ab7a71-58ef-4b24-9a4b-a264b97ca511" />

---

# 4️⃣ 참고 자료

JOIN 개념이 헷갈린다면 아래 자료를 함께 참고해도 좋습니다.

1. https://data-marketing-bk.tistory.com/entry/SQL-JOIN-%ED%95%9C-%EB%B0%A9%EC%97%90-%EC%A0%95%EB%A6%AC-%EA%B0%9C%EB%85%90%EB%B6%80%ED%84%B0-%EC%BD%94%EB%93%9C%EA%B9%8C%EC%A7%80-%EC%9D%B4%EA%B2%83%EB%A7%8C-%EB%B3%B4%EC%9E%90
2. https://velog.io/@wijoonwu/JOIN

---

# 5️⃣ 이번 주 회고

```
1. INNER JOIN과 LEFT JOIN의 차이를 어떻게 이해했는지: INNER JOIN은 두 테이블에 공통으로 존재하는 데이터만 연결하는 방식이고, LEFT JOIN은 왼쪽 테이블의 모든 데이터를 유지하면서 오른쪽 테이블의 일치하는 데이터를 연결하는 방식이라고 이해했다.
2. JOIN 문제를 풀 때 가장 먼저 확인해야 할 것: 어떤 테이블에 필요한 정보가 있는지 확인하고, 두 테이블을 연결할 수 있는 공통 컬럼(JOIN key)이 무엇인지 먼저 확인해야 한다. 또한 어떤 테이블을 기준으로 조회해야 하는지도 판단해야 한다.
3. JOIN 결과가 예상과 달랐던 경험이 있다면: 처음에는 JOIN을 사용하면 두 테이블의 데이터가 모두 합쳐진다고 생각했다. 하지만 LEFT JOIN과 INNER JOIN의 차이를 학습하면서 연결 조건에 따라 조회되는 데이터가 달라진다는 것을 알게 되었다. 특히 LEFT JOIN에서 오른쪽 테이블에 일치하는 데이터가 없으면 NULL이 발생한다는 점이 인상적이었다.
```

수고하셨습니다!
