# 📘 SQL_BASIC 7주차 정규 과제

이번 주 필수 강의는 없습니다.

이번 주는 지금까지 배운 SQL 내용을 가볍게 복습하는 것으로 마무리합니다. 문제 풀이보다 중요한 것은 **내가 어떤 SQL 개념을 익혔고, 아직 어떤 부분이 헷갈리는지 정리하는 것**입니다.

완성된 과제는 Github에 업로드하고, 링크를 스프레드시트 'SQL' 시트에 입력해 제출해주세요.

**👀 수행 인증란은 필수입니다.**

---

## 📚 SQL_BASIC_7th_REVIEW

---

## ✨ 선택 강의

- 6-2. 가독성을 챙기기 위한 SQL 스타일 가이드: SQL을 더 읽기 좋게 작성하고 싶을 때 선택 수강
- 6-3. 가독성을 챙기기 위한 WITH 문 & 파티션: WITH 문과 파티션 개념을 가볍게 살펴보고 싶을 때 선택 수강
- 6-4. 데이터 결과 검증 정의: 쿼리 결과를 검증하는 관점을 알고 싶을 때 선택 수강
- 6-5. 데이터 결과 검증 예시: 결과 검증 사례를 확인하고 싶을 때 선택 수강

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
| 7주차 | 필수 강의 없음 | 6-2, 6-3, 6-4, 6-5 | ✅ |

---

<br>

<!-- 여기까진 그대로 둬 주세요-->

---

## 🔁 복습할 개념

- SELECT, FROM, WHERE
- ORDER BY, LIMIT
- GROUP BY, HAVING
- COUNT, SUM, AVG, MAX, MIN
- 문자열 함수
- 날짜/시간 함수
- CASE WHEN
- JOIN

---

# 1️⃣ 전체 개념 복습

아래 키워드 중 중요하다고 생각한 개념을 2개 이상 골라 짧게 정리해주세요. 3개보다 더 많이 정리하고 싶다면 자유롭게 항목을 추가해도 좋습니다.

복습 키워드:
- SELECT
- WHERE
- GROUP BY
- HAVING
- 문자열 함수
- 날짜/시간 함수
- CASE WHEN
- JOIN

## 01.

```
개념 이름: WHERE와 HAVING의 차이

개념 설명:
WHERE는 GROUP BY를 통해 데이터를 그룹화하기 전에 개별 행을 필터링하는 조건절이다.
HAVING은 GROUP BY로 그룹화한 후 집계 결과를 기준으로 그룹을 필터링하는 조건절이다.

예시 쿼리:
SELECT category, COUNT(*) AS book_count
FROM books
WHERE year >= 2020
GROUP BY category
HAVING COUNT(*) >= 10;
```

## 02.

```
개념 이름: JOIN

개념 설명:
JOIN은 두 개 이상의 테이블에서 관련된 데이터를 연결하여 조회하는 기능이다.
일반적으로 공통된 열을 기준으로 테이블을 연결한다.
INNER JOIN은 양쪽 테이블에 일치하는 데이터만 반환하며, LEFT JOIN은 왼쪽 테이블의 데이터를 모두 반환하고 오른쪽 테이블에 일치하는 데이터가 없으면 해당 값은 NULL로 표시한다.

예시 쿼리:
SELECT students.name, scores.score
FROM students
INNER JOIN scores
ON students.student_id = scores.student_id;
```

## (선택) 03.

```
개념 이름:
개념 설명:
아직 헷갈리는 점:
```

---

# 2️⃣ 수행 인증란

아래 중 하나 이상을 첨부해주세요.
<img width="1807" height="842" alt="image" src="https://github.com/user-attachments/assets/944460a0-a841-43fc-b4b0-897dd9f4eae5" />


- 복습 문제 정답 화면 캡처
- SQL 실행 결과 화면 캡처
- 전체 개념 정리 노트 캡처

---

# 3️⃣ 복습 문제

프로그래머스는 로그인이 필요하므로, 로그인 후 문제 풀이를 진행해주세요.

## 🧩 문제 1

문제 링크: [여러 기준으로 정렬하기](https://school.programmers.co.kr/learn/courses/30/lessons/59404)

풀이 과정:

```
- 문제 요구사항: 모든 동물의 아이디(ANIMAL_ID), 이름(NAME), 보호 시작일(DATETIME)을 조회한다.
- 첫 번째 정렬 기준: NAME을 오름차순(ASC)으로 정렬하여 이름을 사전 순으로 나열한다.
- 두 번째 정렬 기준: 이름이 같은 동물은 DATETIME을 내림차순(DESC)으로 정렬하여 보호를 나중에 시작한 동물을 먼저 보여준다.
- 복습한 점: ORDER BY에 여러 정렬 기준을 지정할 수 있다. 첫 번째 기준으로 정렬한 후, 값이 같은 경우 두 번째 기준을 적용한다. ASC는 오름차순, DESC는 내림차순을 의미한다
```

<img width="935" height="460" alt="image" src="https://github.com/user-attachments/assets/d998c37e-5378-4c30-bca4-cf0eabd2932e" />


## 🧩 문제 2

문제 링크: [동명 동물 수 찾기](https://school.programmers.co.kr/learn/courses/30/lessons/59041)

풀이 과정:

```
- 그룹화 기준: NAME을 기준으로 같은 이름을 가진 동물끼리 그룹화한다.
- 제외해야 하는 값: 이름이 NULL인 데이터는 집계에서 제외한다.
- HAVING 조건: COUNT(*) >= 2를 적용하여 두 번 이상 쓰인 이름만 조회한다.
- 복습한 점: WHERE는 그룹화하기 전에 개별 데이터를 필터링하고, HAVING은 그룹화한 후 집계 결과를 필터링한다. GROUP BY로 그룹을 만든 뒤 COUNT(*)로 각 그룹의 데이터 개수를 셀 수 있다.
```

<img width="1037" height="506" alt="image" src="https://github.com/user-attachments/assets/6b3861db-0573-4805-915a-0b66cbaa83f7" />


---

# 4️⃣ 최종 회고

7주 동안 SQL BASIC 과제를 진행하며 느낀 점을 자유롭게 작성해주세요.

```
1. SQL을 배우기 전과 비교했을 때 달라진 점:
2. 가장 도움이 되었던 과제 또는 문제 유형:
3. 가장 어려웠던 개념:
4. 앞으로 데이터 분석이나 프로젝트에서 SQL을 어떻게 활용해보고 싶은지:
5. SQL BASIC 과제에 대한 피드백:
```

정말 수고하셨습니다!
