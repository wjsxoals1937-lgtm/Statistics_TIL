# 📘 SQL_BASIC 5주차 정규 과제

SQL_BASIC 정규 과제는 매주 정해진 분량의 `초보자를 위한 BigQuery(SQL) 입문` 강의를 듣고, 핵심 개념을 정리한 뒤 간단한 SQL 문제를 직접 풀어보는 방식으로 진행합니다.

이번 주는 날짜/시간 데이터와 조건문을 학습합니다. 특히 `CASE WHEN`은 SQL 문제 풀이와 데이터 분석에서 자주 사용되므로, 직접 분류 기준을 만들고 결과를 확인하는 연습을 해주세요.

완성된 과제는 Github에 업로드하고, 링크를 스프레드시트 'SQL' 시트에 입력해 제출해주세요.

**👀 수행 인증란은 필수입니다.**

---

## 📚 SQL_BASIC_5th_TIL

### 섹션 5. 데이터 탐색 - 변환

### 4-4. 날짜 및 시간 데이터 이해하기

### 4-6. 조건문(CASE WHEN, IF)

---

## ✨ 선택 강의

- 4-5. 시간 데이터 연습문제: 날짜/시간 함수를 더 연습하고 싶을 때 선택 수강
- 4-7. 조건문 연습문제: CASE WHEN과 IF를 더 연습하고 싶을 때 선택 수강

---

## 🏁 전체 강의 수강 계획

| 주차 | 필수 강의 범위 | 선택 강의 | 완료 여부 |
| --- | --- | --- | --- |
| 1주차 | 1-1 ~ 2-1 | 1 | ✅ |
| 2주차 | 2-2 ~ 2-3 | 2-4 | ✅ |
| 3주차 | 2-5, 2-7 ~ 2-8 | 2-6 | ✅ |
| 4주차 | 3-2 ~ 4-3 | 3-4 | ✅ |
| 5주차 | 4-4 ~ 4-6 | 4-5, 4-7 | ✅ |
| 6주차 | 5-2 ~ 5-5 | 5-6 | 🍽️ |
| 7주차 | 필수 강의 없음 | 6-2, 6-3, 6-4, 6-5 | 🍽️ |

---

<br>

<!-- 여기까진 그대로 둬 주세요-->

---

# 1️⃣ 개념 정리

아래 키워드 중 중요하다고 생각한 개념을 2개 이상 골라 짧게 정리해주세요. 3개보다 더 많이 정리하고 싶다면 자유롭게 항목을 추가해도 좋습니다.

이번 주 키워드:
- DATE
- DATETIME
- TIMESTAMP
- EXTRACT
- DATETIME_TRUNC
- FORMAT_DATETIME
- CASE WHEN
- IF

## 01.

```
개념 이름: DATE

개념 설명:
날짜만 저장하거나 다룰 때 사용하는 데이터 타입이다.
연도, 월, 일만 필요하고 시간은 필요하지 않을 때 사용한다.

예시 쿼리:
SELECT DATE '2026-09-28' AS date;
```

## 02.

```
개념 이름: DATETIME

개념 설명:
날짜와 시간을 함께 저장하거나 다룰 때 사용하는 데이터 타입이다.
연도, 월, 일뿐만 아니라 시, 분, 초까지 표현할 수 있다.

예시 쿼리:
SELECT DATETIME '2026-09-28 10:30:00' AS datetime;
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

---

# 3️⃣ 확인 문제

프로그래머스는 로그인이 필요하므로, 로그인 후 문제 풀이를 진행해주세요.

## 🧩 문제 1

문제 링크: [자동차 대여 기록에서 장기/단기 대여 구분하기](https://school.programmers.co.kr/learn/courses/30/lessons/151138)

풀이 과정:
SELECT
    HISTORY_ID,
    CAR_ID,
    START_DATE,
    END_DATE,
    CASE
        WHEN DATEDIFF(END_DATE, START_DATE) + 1 >= 30
            THEN '장기 대여'
        ELSE '단기 대여'
    END AS RENT_TYPE
FROM CAR_RENTAL_COMPANY_RENTAL_HISTORY
WHERE START_DATE >= '2022-09-01'
  AND START_DATE < '2022-10-01'
ORDER BY HISTORY_ID DESC;


```
-장기/단기 대여를 나눈 기준: 대여 기간이 30일 이상이면 '장기 대여', 30일 미만이면 '단기 대여'로 구분하였다.
-사용한 날짜 계산 방식: DATEDIFF(END_DATE, START_DATE) + 1을 사용하여 시작일과 종료일을 모두 포함한 대여 기간을 계산하였다.
-CASE WHEN으로 만든 컬럼: CASE WHEN을 사용하여 대여 기간이 30일 이상이면 '장기 대여', 그렇지 않으면 '단기 대여'로 표시하는 RENT_TYPE 컬럼을 만들었다.
```

<!-- 정답을 맞추게 되면, 정답입니다. 이 부분을 캡처해서 이 주석을 지우시고 첨부해주시면 됩니다. -->

## 🧩 문제 2

문제 링크: [한 해에 잡은 물고기 수 구하기](https://school.programmers.co.kr/learn/courses/30/lessons/298516)

풀이 과정:
SELECT COUNT(*) AS FISH_COUNT
FROM FISH_INFO
WHERE TIME >= '2021-01-01'
  AND TIME < '2022-01-01';
```
-문제에서 요구한 연도: 2021년
-사용한 날짜 조건: TIME이 2021년 1월 1일부터 2021년 12월 31일까지인 데이터를 조건으로 설정하였다.
-집계한 대상: 2021년에 잡은 물고기의 수를 COUNT(*)로 집계하였다.
```

<!-- 정답을 맞추게 되면, 정답입니다. 이 부분을 캡처해서 이 주석을 지우시고 첨부해주시면 됩니다. -->

## 🧩 문제 3

문제 링크: [조건에 부합하는 중고거래 상태 조회하기](https://school.programmers.co.kr/learn/courses/30/lessons/164672)

풀이 과정:

```
-날짜 조건: 2022-10-05에 등록된 게시물
-CASE WHEN으로 바꾼 값: SALE → 판매중, RESERVED → 예약중, DONE → 거래완료
-ELSE에 해당하는 경우: 위 3가지 상태가 아닌 경우
-정렬 기준: BOARD_ID 기준 내림차순(DESC)
```

<!-- 정답을 맞추게 되면, 정답입니다. 이 부분을 캡처해서 이 주석을 지우시고 첨부해주시면 됩니다. -->

## 🧩 문제 4

문제 링크: [자동차 평균 대여 기간 구하기](https://school.programmers.co.kr/learn/courses/30/lessons/157342)

풀이 과정:
SELECT
    CAR_ID,
    ROUND(AVG(DATEDIFF(END_DATE, START_DATE) + 1), 1) AS AVERAGE_DURATION
FROM CAR_RENTAL_COMPANY_RENTAL_HISTORY
GROUP BY CAR_ID
HAVING AVG(DATEDIFF(END_DATE, START_DATE) + 1) >= 7
ORDER BY AVERAGE_DURATION DESC, CAR_ID DESC;

```

```

<!-- 정답을 맞추게 되면, 정답입니다. 이 부분을 캡처해서 이 주석을 지우시고 첨부해주시면 됩니다. -->

---
GROUP BY 기준: CAR_ID

평균을 계산한 방식: 대여 일수를 구한 후 AVG()로 평균 계산

HAVING에 사용한 조건: 평균 대여 기간이 7일 이상

처음 헷갈렸던 점: DATEDIFF()는 시작일을 포함하지 않아 +1을 해야 함.




# 4️⃣ 이번 주 회고

```
날짜 함수 중 가장 헷갈린 함수: DATEDIFF() — 시작일과 종료일 중 하루가 포함되는지 헷갈렸다.
CASE WHEN을 사용할 때 기억해야 할 문법: CASE WHEN 조건 THEN 결과 ELSE 결과 END 순서로 작성한다.
날짜/시간 데이터나 조건문을 활용해보고 싶은 분석 상황: 고객의 가입 기간별 구매 패턴이나 시간대별 매출을 분석해보고 싶다.
```

수고하셨습니다!
