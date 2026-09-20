
# 데이터분석 3주차 정규과제

📌데이터분석 정규과제는 매주 정해진 분량의 『*혼자 공부하는 데이터 분석 with 파이썬*』 을 읽고 학습하는 것입니다. 이번 주는 아래의 **DataAnalysis_3rd_TIL**에 나열된 분량을 읽고 공부하시면 됩니다.

아래의 문제를 풀어보며 학습 내용을 점검하세요. 문제를 해결하는 과정에서 개념을 스스로 정리하고, 필요한 경우 제시된 강의를 참고하여 보완하는 것이 좋습니다.

<!-- 강의 링크는 아래와 같습니다.
https://www.youtube.com/watch?v=CE3_InvbmLY&list=PLVsNizTWUw7FGzSRCkQrPEEe-ljVXgS7k&index=6
https://www.youtube.com/watch?v=hhbzUEQWdTg&list=PLVsNizTWUw7FGzSRCkQrPEEe-ljVXgS7k&index=7
-->


## DataAnalysis_3rd_TIL

### 3장 데이터 정제하기
#### 01. 불필요한 데이터 삭제하기
#### 02. 잘못된 데이터 수정하기


## Study Schedule

| 주차  | 공부 범위     | 완료 여부 |
| ----- | ------------- | --------- |
| 1주차 | p.24~81    | ✅         |
| 2주차 | p.84~151   | ✅         |
| 3주차 | p.154~219  | ✅         |
| 4주차 | p.222~279 | 🍽️         |
| 5주차 | p.282~325 | 🍽️         |
| 6주차 | p.328~379 | 🍽️         |
| 7주차 | p.382~430 | 🍽️         |

<br>

<!-- 여기까진 그대로 둬 주세요-->


# 1️⃣ 개념 정리 

## 01. 불필요한 데이터 삭제하기

<!-- 새롭게 배운 내용을 자유롭게 정리해주세요.--> 데이터 정제는 수집한 데이터에서 분석에 필요하지 않은 데이터를 제거하거나 잘못된 데이터를 수정하여 분석에 적합한 형태로 만드는 과정이다.
데이터 정제와 데이터를 분석이나 머신러닝에 사용할 수 있도록 변환하는 과정을 통틀어 데이터 랭글링(data wrangling) 또는 데이터 멍잉(data munging)이라고 한다.


## 02. 잘못된 데이터 수정하기

<!-- 새롭게 배운 내용을 자유롭게 정리해주세요.--> `drop()` 메서드는 데이터프레임에서 특정 행이나 열을 삭제할 때 사용한다.


# 2️⃣ 수행 인증

<!-- 교재에서 안내된 과정을 직접 실행해본 뒤, 진행 결과가 보이도록 4~6장의 스크린샷을 캡처하여 아래에 첨부해주세요.-->
<!-- 이번 주차에는 API를 발급받는 과정도 포함하여 첨부해주세요.-->
<br>
<br>
<img width="887" height="677" alt="스크린샷 2026-09-20 141112" src="https://github.com/user-attachments/assets/d5a90053-222c-4361-8018-0748072bb05a" />
<img width="720" height="717" alt="1" src="https://github.com/user-attachments/assets/02cce965-df31-4717-9889-0cf1bb262477" />
<img width="535" height="806" alt="2" src="https://github.com/user-attachments/assets/cfa88c08-28be-4400-bd74-16c5f1fb3e32" />
<img width="590" height="712" alt="3" src="https://github.com/user-attachments/assets/18c8ffb4-fbab-4e5f-b031-33b3073cc025" />
<img width="675" height="782" alt="4" src="https://github.com/user-attachments/assets/09168a1a-9cd2-4b97-b858-f76c71ab5c92" />
<img width="632" height="725" alt="5" src="https://github.com/user-attachments/assets/8572a790-11ea-4634-a0d3-a39ecdbd95ff" />
<img width="611" height="781" alt="6" src="https://github.com/user-attachments/assets/d482c6fd-5821-44de-ba8c-63457c710653" />
<img width="586" height="760" alt="7" src="https://github.com/user-attachments/assets/2c6b423e-1ff3-48a1-b2f3-647fb1ba7f0a" />
<img width="677" height="772" alt="8" src="https://github.com/user-attachments/assets/94333b64-faa3-40ab-8ee3-ff5cab85bc85" />
<img width="475" height="752" alt="9" src="https://github.com/user-attachments/assets/1e133c1a-419c-4669-9be9-853131b8fa52" />
<img width="532" height="722" alt="10" src="https://github.com/user-attachments/assets/ba245ec0-168c-4c0c-8578-90591b57d4f2" />
<img width="322" height="780" alt="11" src="https://github.com/user-attachments/assets/b90108b7-94d6-44ae-8e88-2873bd24c1c9" />
<img width="296" height="147" alt="12" src="https://github.com/user-attachments/assets/ba54999f-753c-4346-8e36-6c4bc4164d7a" />






# 3️⃣ 확인 문제

## 문제 1.

> **🧚Q. 다음 두 데이터프레임 df1, df2를 합쳐서 데이터프레임 df3를 만들려고 합니다.**  
> 적절한 판다스 명령을 선택해주세요.
> 3️⃣

df1의 `col1`과 df2의 `col3`을 기준으로 합쳐야 합니다.

그리고 결과를 보면 `z`와 `w`처럼 한쪽에만 있는 데이터도 모두 들어가 있습니다.

따라서 두 데이터프레임의 데이터를 모두 가져오는 `outer`를 사용해야 합니다.

그래서 정답은 **3번**입니다.

<table>
<tr>

<td>

### df1

| index | col1 | col2 |
|-------|------|------|
| 0     | x    | 5    |
| 1     | y    | 6    |
| 2     | z    | 7    |

</td>

<td>

### df2

| index | col3 | col4 |
|-------|------|------|
| 0     | x    | 50   |
| 1     | y    | 60   |
| 2     | w    | 70   |

</td>

<td align="center" valign="middle">

<h2> ➜ </h2>

</td>

<td>

### df3 (결과)

| index | col1 | col2 | col3 | col4 |
|-------|------|------|------|------|
| 0     | x    | 5.0  | x    | 50.0 |
| 1     | y    | 6.0  | y    | 60.0 |
| 2     | z    | 7.0  | NaN  | NaN  |
| 3     | NaN  | NaN  | w    | 70.0 |

</td>

</tr>
</table>

```
1️⃣ pd.merge(df1, df2)
2️⃣ pd.merge(df1, df2, how='left')
3️⃣ pd.merge(df1, df2, left_on='col1', right_on='col3', how='outer')
4️⃣ pd.merge(df1, df2, left_on='col1', right_on='col3', how='inner')
```

```
여기에 선택한 답과 그 이유를 간단히 서술해주세요!
3️⃣

df1의 `col1`과 df2의 `col3`을 기준으로 합쳐야 합니다.

그리고 결과를 보면 `z`와 `w`처럼 한쪽에만 있는 데이터도 모두 들어가 있습니다.

따라서 두 데이터프레임의 데이터를 모두 가져오는 `outer`를 사용해야 합니다.

그래서 정답은 **3번**입니다.
```



### 🎉 수고하셨습니다.
