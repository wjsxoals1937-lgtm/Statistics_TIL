# 데이터분석 6주차 정규과제

📌데이터분석 정규과제는 매주 정해진 분량의 『*혼자 공부하는 데이터 분석 with 파이썬*』 을 읽고 학습하는 것입니다. 이번 주는 아래의 **DataAnalysis_6th_TIL**에 나열된 분량을 읽고 공부하시면 됩니다.

아래의 문제를 풀어보며 학습 내용을 점검하세요. 문제를 해결하는 과정에서 개념을 스스로 정리하고, 필요한 경우 제시된 강의를 참고하여 보완하는 것이 좋습니다.

<!-- 강의 링크는 아래와 같습니다.
https://www.youtube.com/watch?v=XD65UhBMOiI&list=PLVsNizTWUw7FGzSRCkQrPEEe-ljVXgS7k&index=12
https://www.youtube.com/watch?v=NTQ5NXelOfw&list=PLVsNizTWUw7FGzSRCkQrPEEe-ljVXgS7k&index=13
-->


## DataAnalysis_6th_TIL

### 6장 복잡한 데이터 표현하기
#### 01. 객체지향 API로 그래프 꾸미기
#### 02. 맷플롯립의 고급 기능 배우기


## Study Schedule

| 주차  | 공부 범위     | 완료 여부 |
| ----- | ------------- | --------- |
| 1주차 | p.24~81    | ✅         |
| 2주차 | p.84~151   | ✅         |
| 3주차 | p.154~219  | ✅         |
| 4주차 | p.222~279 | ✅         |
| 5주차 | p.282~325 | ✅         |
| 6주차 | p.328~379 | ✅         |
| 7주차 | p.382~430 | 🍽️         |

<br>

<!-- 여기까진 그대로 둬 주세요-->


# 1️⃣ 개념 정리 

## 01. 객체지향 API로 그래프 꾸미기

<!-- 새롭게 배운 내용을 자유롭게 정리해주세요.-->
객체지향 API에서는 Figure 객체와 Axes 객체를 구분한다. Figure는 그래프 전체를 담는 영역이고, Axes는 실제 데이터가 표현되는 그래프 영역이다. ax.set_title()로 그래프 제목을 지정하거나 ax.scatter()로 산점도를 그리는 등 그래프의 세부 요소를 각각 조정할 수 있다.

## 02. 맷플롯립의 고급 기능 배우기

<!-- 새롭게 배운 내용을 자유롭게 정리해주세요.-->
맷플롯립은 하나의 그래프를 그리는 것뿐만 아니라 여러 데이터를 다양한 형태로 표현하고, 여러 그래프를 하나의 화면에 배치하는 기능도 제공한다.

먼저 판다스의 groupby()를 사용하면 특정 기준에 따라 데이터를 그룹으로 나누고, sum() 등을 이용해 각 그룹의 합계를 계산할 수 있다. 이렇게 정리한 데이터를 활용하면 출판사별 연도별 대출건수처럼 여러 기준에 따른 데이터의 변화를 분석할 수 있다.

그래프의 종류에 따라 표현 방법도 달라진다. plot()은 시간의 흐름에 따른 데이터의 변화를 선 그래프로 나타내며, stackplot()은 여러 데이터의 누적된 변화를 영역 그래프로 표현한다. bar()는 막대 그래프를 그릴 때 사용하고, bottom 매개변수를 이용하면 막대를 위로 쌓아 올리는 스택 막대 그래프를 만들 수 있다. 또한 cumsum()은 누적 합계를 계산할 때 사용한다. pie()는 전체에서 각 항목이 차지하는 비율을 원 그래프로 표현하며, autopct를 이용해 비율을 표시하고 explode를 이용해 특정 항목을 강조할 수 있다.

여러 그래프를 한 화면에 배치할 때는 plt.subplots()를 사용한다. 행과 열의 개수를 지정하면 하나의 Figure 안에 여러 Axes 객체를 만들 수 있으며, 각 Axes에 서로 다른 그래프를 그릴 수 있다. 이를 통해 산점도, 영역 그래프, 막대 그래프, 원 그래프 등을 한 화면에서 비교할 수 있다.

마지막으로 판다스에서도 plot.area()와 plot.bar()를 이용해 그래프를 그릴 수 있다는 점을 배웠다. 특히 stacked=True를 지정하면 누적 막대 그래프를 간편하게 표현할 수 있다.

이번 학습을 통해 데이터를 목적에 맞게 집계하고, 여러 종류의 그래프를 활용하여 데이터의 변화와 구성 비율을 시각적으로 비교하는 방법을 익혔다.


# 2️⃣ 수행 인증

<!-- 교재에서 안내된 과정을 직접 실행해본 뒤, 진행 결과가 보이도록 4~6장의 스크린샷을 캡처하여 아래에 첨부해주세요.-->
<img width="1010" height="767" alt="스크린샷 2026-10-31 194035" src="https://github.com/user-attachments/assets/674b2477-30af-4205-8c51-e76a9e3aa5ff" />
<img width="1001" height="792" alt="스크린샷 2026-10-31 194104" src="https://github.com/user-attachments/assets/2d209873-2a1e-4908-96f4-943fe8bcd937" />
<img width="992" height="770" alt="스크린샷 2026-10-31 194311" src="https://github.com/user-attachments/assets/973141a7-d000-43b3-a176-2949f2c1047c" />
<img width="1005" height="772" alt="스크린샷 2026-10-31 194333" src="https://github.com/user-attachments/assets/3aa894e2-e8be-4d3b-b7ba-6ddd514e6007" />
<img width="877" height="737" alt="스크린샷 2026-10-31 194400" src="https://github.com/user-attachments/assets/10acc496-9325-4cfd-a010-03f3458d7297" />
<img width="502" height="787" alt="스크린샷 2026-10-31 194425" src="https://github.com/user-attachments/assets/a7cfee4b-b6ad-4a4a-ba11-ccb223ea879f" />
<img width="640" height="772" alt="스크린샷 2026-10-31 194447" src="https://github.com/user-attachments/assets/11ad1ea0-a369-4a57-9115-0dfbc8032047" />
<img width="877" height="782" alt="스크린샷 2026-10-31 194510" src="https://github.com/user-attachments/assets/9c961ef4-36b6-4f7d-af9b-9ce29e317149" />
<img width="557" height="655" alt="스크린샷 2026-10-31 194528" src="https://github.com/user-attachments/assets/8c5760f4-8702-41a6-ac8f-0d6189fc708e" />
<img width="795" height="652" alt="스크린샷 2026-10-31 194553" src="https://github.com/user-attachments/assets/9cf08241-a4f1-404f-abdb-d6d7a6fc4b65" />

<br>
<br>

# 3️⃣ 확인 문제

## 문제 1.

> **🧚Q. 이번 주차에는 확인문제 대신 그래프 그리기 실습을 진행합니다.
4주차에서 사용했던 캐글 데이터셋을 활용하여, 다양한 요소를 포함한 복잡한 그래프를 직접 작성해주세요.**

```
https://colab.research.google.com/drive/1pWM9mfNypsXMgvkqOtTPriUBWXhIDa0g#scrollTo=zP_K8qcOnSeG
여기에 코랩 링크를 첨부해주세요!
(제출 전, 코랩의 공유 설정을 ‘링크가 있는 모든 사용자가 보기 가능’으로 변경했는지 반드시 확인해주세요.)
```



### 🎉 수고하셨습니다.
