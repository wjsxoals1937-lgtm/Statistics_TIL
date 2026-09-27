# 📘 SQL_BASIC 4주차 정규 과제

SQL_BASIC 정규 과제는 매주 정해진 분량의 `초보자를 위한 BigQuery(SQL) 입문` 강의를 듣고, 핵심 개념을 정리한 뒤 간단한 SQL 문제를 직접 풀어보는 방식으로 진행합니다.

이번 주는 SQL 쿼리를 작성하는 흐름, 쿼리 작성 템플릿, 데이터 타입 변환, 문자열 함수를 학습합니다.

완성된 과제는 Github에 업로드하고, 링크를 스프레드시트 'SQL' 시트에 입력해 제출해주세요.

**👀 수행 인증란은 필수입니다.**

---

## 📚 SQL_BASIC_4th_TIL

### 섹션 4. SQL 쿼리 잘 작성하기, 쿼리 작성 템플릿 및 오류를 잘 디버깅하기

### 3-2. SQL 쿼리를 작성하는 흐름

### 3-3. 쿼리 작성 템플릿과 생산성 도구

### 섹션 5. 데이터 탐색 - 변환

### 4-1. INTRO

### 4-2. 데이터 타입과 데이터 변환(CAST, SAFE_CAST)

### 4-3. 문자열 함수(CONCAT, SPLIT, REPLACE, TRIM, UPPER)

---

## ✨ 선택 강의

- 3-4. 오류를 디버깅하는 방법: 오류 메시지 해석과 디버깅 흐름을 더 익히고 싶을 때 선택 수강

---

## 🏁 전체 강의 수강 계획

| 주차 | 필수 강의 범위 | 선택 강의 | 완료 여부 |
| --- | --- | --- | --- |
| 1주차 | 1-1 ~ 2-1 | 1 | ✅ |
| 2주차 | 2-2 ~ 2-3 | 2-4 | ✅ |
| 3주차 | 2-5, 2-7 ~ 2-8 | 2-6 | ✅ |
| 4주차 | 3-2 ~ 4-3 | 3-4 | ✅ |
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
- 쿼리 작성 순서
- 쿼리 작성 템플릿
- 데이터 타입
- CAST
- SAFE_CAST
- CONCAT
- REPLACE
- TRIM

## 01.

```
개념 이름: 쿼리 작성 순서
개념 설명: SQL 쿼리는 데이터를 원하는 형태로 만들기 위해 일정한 순서로 작성합니다.
기본적인 작성 순서는 SELECT → FROM → WHERE → GROUP BY → HAVING → ORDER BY입니다.

SELECT는 어떤 컬럼을 가져올지 정하고,
FROM은 어떤 테이블에서 데이터를 가져올지 정합니다.
WHERE는 원하는 조건의 데이터만 필터링하고,
GROUP BY는 데이터를 특정 기준으로 그룹화합니다.
HAVING은 그룹화한 결과에 조건을 적용하고,
ORDER BY는 최종 결과를 원하는 순서로 정렬합니다.

예시 쿼리:
SELECT
  category,
  COUNT(*) AS order_count
FROM `project.dataset.orders`
WHERE order_date >= '2026-01-01'
GROUP BY category
HAVING COUNT(*) >= 10
ORDER BY order_count DESC;
```

## 02.

```
개념 이름: CAST와 SAFE_CAST
개념 설명:
CAST와 SAFE_CAST는 데이터의 타입을 다른 타입으로 변환할 때 사용합니다.
예를 들어 숫자로 저장된 데이터를 문자열로 바꾸거나,
문자열로 저장된 숫자를 실제 숫자 데이터로 바꿀 때 사용할 수 있습니다.
CAST는 변환할 수 없는 값이 있으면 오류가 발생합니다.
반면 SAFE_CAST는 변환할 수 없는 값이 있어도 오류를 발생시키지 않고
해당 값을 NULL로 반환합니다.
따라서 데이터에 어떤 값이 들어있는지 확실하지 않을 때는
SAFE_CAST를 사용하면 오류를 줄일 수 있습니다.

예시 쿼리:
SELECT
  CAST('100' AS INT64) AS number,
  SAFE_CAST('abc' AS INT64) AS safe_number;
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
- <img width="1831" height="906" alt="1" src="https://github.com/user-attachments/assets/fe558017-3926-476c-9a5f-29bc110bfa78" />


---

# 3️⃣ 확인 문제

프로그래머스는 로그인이 필요하므로, 로그인 후 문제 풀이를 진행해주세요.

## 🧩 문제 1

문제 링크: [특정 옵션이 포함된 자동차 리스트 구하기](https://school.programmers.co.kr/learn/courses/30/lessons/157343)

풀이 과정: 
SELECT *
FROM CAR_RENTAL_COMPANY_CAR
WHERE OPTIONS LIKE '%네비게이션%'
ORDER BY CAR_ID DESC;

```
- 찾으려는 문자열 조건: OPTIONS에 '네비게이션'이 포함된 자동차
- 사용한 문자열 조건 문법: LIKE '%네비게이션%'
- 정렬 기준: CAR_ID 기준 내림차순(DESC)
```

<!-- 정답을 맞추게 되면, 정답입니다. 이 부분을 캡처해서 이 주석을 지우시고 첨부해주시면 됩니다. --> <img width="922" height="455" alt="image" src="https://github.com/user-attachments/assets/08ee87f0-516e-4ab0-82a8-1edff03f68bf" />


## 🧩 문제 2

문제 링크: [강원도에 위치한 생산공장 목록 출력하기](https://school.programmers.co.kr/learn/courses/30/lessons/131112)

풀이 과정:

```
- 문제에서 요구한 조건: ADDRESS에 '강원도'가 포함된 식품공장의 FACTORY_ID, FACTORY_NAME, ADDRESS 조회
- WHERE 절로 옮긴 방식: ADDRESS LIKE '강원도%'
- 정렬 기준: FACTORY_ID 기준 오름차순(ASC)
```

<!-- 정답을 맞추게 되면, 정답입니다. 이 부분을 캡처해서 이 주석을 지우시고 첨부해주시면 됩니다. --> <img width="818" height="382" alt="image" src="https://github.com/user-attachments/assets/f53cefde-5404-4dee-9132-3970bcbe0d57" />


## 🧩 문제 3

문제 링크: [이름에 el이 들어가는 동물 찾기](https://school.programmers.co.kr/learn/courses/30/lessons/59047)

풀이 과정:
SELECT ANIMAL_ID, NAME
FROM ANIMAL_INS
WHERE ANIMAL_TYPE = 'Dog'
  AND LOWER(NAME) LIKE '%el%'
ORDER BY NAME ASC, ANIMAL_ID ASC;

```
- 찾으려는 문자열 패턴: 이름에 'el'이 포함된 개
- 대소문자를 처리한 방식: LOWER(NAME)으로 이름을 소문자로 변환한 후 LIKE '%el%' 사용
- 정렬 기준: NAME 기준 오름차순, 이름이 같으면 ANIMAL_ID 기준 오름차순
```

<!-- 정답을 맞추게 되면, 정답입니다. 이 부분을 캡처해서 이 주석을 지우시고 첨부해주시면 됩니다. --> <img width="872" height="426" alt="image" src="https://github.com/user-attachments/assets/b4747e0b-338c-4ced-aab1-bc4e0f64e440" />


## 🧩 문제 4

문제 링크: [카테고리 별 상품 개수 구하기](https://school.programmers.co.kr/learn/courses/30/lessons/131529)

풀이 과정: 
SELECT LEFT(PRODUCT_CODE, 2) AS CATEGORY,
       COUNT(*) AS PRODUCTS
FROM PRODUCT
GROUP BY LEFT(PRODUCT_CODE, 2)
ORDER BY CATEGORY ASC;

```
- 추출한 문자열 범위: PRODUCT_CODE의 앞 2자리
- 그룹화 기준: 상품 카테고리 코드별로 그룹화
- 정렬 기준: CATEGORY 기준 오름차순(ASC)
```

<!-- 정답을 맞추게 되면, 정답입니다. 이 부분을 캡처해서 이 주석을 지우시고 첨부해주시면 됩니다. --><img width="838" height="423" alt="image" src="https://github.com/user-attachments/assets/3e366054-ac9d-4d87-aaa1-6556c87ce89b" />


---

# 4️⃣ 이번 주 회고

```
1. 쿼리 작성 흐름을 잡을 때 도움이 된 방법:
2. 타입 변환이나 문자열 처리에서 조심해야 할 점:
3. 앞으로 문제 풀이 때 먼저 확인할 것:
```

수고하셨습니다!
