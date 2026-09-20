# 📘 SQL_BASIC 3주차 정규 과제

SQL_BASIC 정규 과제는 매주 정해진 분량의 `초보자를 위한 BigQuery(SQL) 입문` 강의를 듣고, 핵심 개념을 정리한 뒤 간단한 SQL 문제를 직접 풀어보는 방식으로 진행합니다.

이번 주는 집계 함수와 `GROUP BY`, `HAVING`을 학습합니다.

완성된 과제는 Github에 업로드하고, 링크를 스프레드시트 'SQL' 시트에 입력해 제출해주세요.

**👀 수행 인증란은 필수입니다.**

---

## 📚 SQL_BASIC_3rd_TIL

### 섹션 3. 데이터 탐색 - 조건, 추출, 요약

### 2-5. 집계(GROUP BY + HAVING + SUM/COUNT)

### 2-7. 정리

### 2-8. 새로운 집계 함수 소개(GROUP BY ALL, 2024-02-26에 나온 함수)

---

## ✨ 선택 강의

- 2-6. 연습 문제: 집계와 조건 조회를 더 연습하고 싶을 때 선택 수강

---

## 🏁 전체 강의 수강 계획

| 주차 | 필수 강의 범위 | 선택 강의 | 완료 여부 |
| --- | --- | --- | --- |
| 1주차 | 1-1 ~ 2-1 | 1 | ✅ |
| 2주차 | 2-2 ~ 2-3 | 2-4 | ✅ |
| 3주차 | 2-5, 2-7 ~ 2-8 | 2-6 | ✅ |
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
- COUNT
- SUM
- AVG
- MAX
- MIN
- GROUP BY
- HAVING
- 집계 기준

## 01.

```
개념 이름: COUNT
개념 설명: 데이터의 개수를 세는 함수입니다.
예시 쿼리: SELECT COUNT(*) FROM books;
```

## 02.

```
개념 이름: GROUP BY
개념 설명: 같은 값을 가진 데이터를 하나의 그룹으로 묶어 집계할 때 사용합니다.
예시 쿼리: SELECT category, COUNT(*) FROM books GROUP BY category;
```

## (선택) 03.

```
개념 이름: AVG
개념 설명: 숫자 데이터의 평균을 구하는 함수입니다.
헷갈린 점: AVG는 평균을 구하는 함수이고, COUNT는 데이터의 개수를 세는 함수라는 점을 구분해야 합니다.
```

---

# 2️⃣ 수행 인증란

아래 중 하나 이상을 첨부해주세요.

- 강의 수강 화면 캡처
- 문제 풀이 정답 화면 캡처
- SQL 실행 결과 화면 캡처
<img width="887" height="677" alt="스크린샷 2026-09-20 141112" src="https://github.com/user-attachments/assets/7efcd3cf-e4a2-400c-b7bd-34cf95a1057c" />

---

# 3️⃣ 확인 문제

프로그래머스는 로그인이 필요하므로, 로그인 후 문제 풀이를 진행해주세요.

## 🧩 문제 1

문제 링크: [최댓값 구하기](https://school.programmers.co.kr/learn/courses/30/lessons/59415)

풀이 과정:
SELECT MAX(DATETIME) AS 시간
FROM ANIMAL_INS;

```
-문제 요구사항: ANIMAL_INS 테이블에서 가장 최근에 들어온 동물의 보호 시작 날짜와 시간을 조회한다.
-사용한 SQL 절: SELECT, MAX(), FROM
-새로 배운 점: MAX()를 사용하면 특정 컬럼에서 가장 큰 값을 구할 수 있으며, 날짜/시간 데이터에서는 가장 최근 날짜와 시간을 구할 수 있다.
```

<!-- 정답을 맞추게 되면, 정답입니다. 이 부분을 캡처해서 이 주석을 지우시고 첨부해주시면 됩니다. --> <img width="1023" height="486" alt="image" src="https://github.com/user-attachments/assets/f7d7f8d4-fef9-46aa-a6c6-2a34133916ee" />


## 🧩 문제 2

문제 링크: [가장 비싼 상품 구하기](https://school.programmers.co.kr/learn/courses/30/lessons/131697)

풀이 과정:
SELECT MAX(PRICE) AS MAX_PRICE
FROM PRODUCT;

```
-사용한 집계 함수: MAX()
-집계 대상 컬럼: PRICE
-결과를 검증한 방법: 예시 데이터의 판매가 10000, 9000, 22000 중 가장 큰 값이 22000으로 출력되는지 확인했다.
```

<!-- 정답을 맞추게 되면, 정답입니다. 이 부분을 캡처해서 이 주석을 지우시고 첨부해주시면 됩니다. --> <img width="918" height="417" alt="image" src="https://github.com/user-attachments/assets/5ca55d00-6eec-4d23-93d6-faf7a46fbec9" />


## 🧩 문제 3

문제 링크: [고양이와 개는 몇 마리 있을까](https://school.programmers.co.kr/learn/courses/30/lessons/59040)

풀이 과정:

```
-그룹화 기준: ANIMAL_TYPE
-WHERE와 HAVING 중 사용한 절: 둘 다 사용하지 않음
-처음 틀렸다면 틀린 이유: 처음부터 정답을 작성했다면 해당 없음
-새로 배운 SQL 패턴: GROUP BY로 종류별로 그룹을 만든 후 COUNT(*)로 각 그룹의 개수를 구할 수 있다.
```

<!-- 정답을 맞추게 되면, 정답입니다. 이 부분을 캡처해서 이 주석을 지우시고 첨부해주시면 됩니다. --> <img width="876" height="385" alt="image" src="https://github.com/user-attachments/assets/3bf41199-0634-4f2e-bba2-0528b65503a2" />


---

# 4️⃣ 이번 주 회고

```
1. 문제를 SQL로 옮길 때 가장 어려웠던 부분: 문제에서 요구하는 조건을 GROUP BY, COUNT() 등의 SQL 문법으로 바꾸는 것이 어려웠다.
2. WHERE와 HAVING의 차이를 어떻게 이해했는지: WHERE는 그룹으로 묶기 전에 데이터 자체를 필터링하고, HAVING은 GROUP BY로 그룹을 만든 후 그룹
3. 다음 주에 더 연습하고 싶은 문제 유형: GROUP BY와 HAVING을 함께 사용해서 그룹별 조건을 적용하는 문제를 더 연습하고 싶다.
```

수고하셨습니다!
