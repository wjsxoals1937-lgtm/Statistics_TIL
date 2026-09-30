# 데이터분석 5주차 정규과제

📌데이터분석 정규과제는 매주 정해진 분량의 『*혼자 공부하는 데이터 분석 with 파이썬*』 을 읽고 학습하는 것입니다. 이번 주는 아래의 **DataAnalysis_5th_TIL**에 나열된 분량을 읽고 공부하시면 됩니다.

아래의 문제를 풀어보며 학습 내용을 점검하세요. 문제를 해결하는 과정에서 개념을 스스로 정리하고, 필요한 경우 제시된 강의를 참고하여 보완하는 것이 좋습니다.

<!-- 강의 링크는 아래와 같습니다.
https://www.youtube.com/watch?v=ho0LZ6GWhtc&list=PLVsNizTWUw7FGzSRCkQrPEEe-ljVXgS7k&index=10
https://www.youtube.com/watch?v=deYY4xHsI0o&list=PLVsNizTWUw7FGzSRCkQrPEEe-ljVXgS7k&index=11
-->


## DataAnalysis_5th_TIL

### 5장 데이터 시각화하기
#### 01. 맷플롯립 기본 요소 알아보기
#### 02. 선 그래프와 막대 그래프 그리기


## Study Schedule

| 주차  | 공부 범위     | 완료 여부 |
| ----- | ------------- | --------- |
| 1주차 | p.24~81    | ✅         |
| 2주차 | p.84~151   | ✅         |
| 3주차 | p.154~219  | ✅         |
| 4주차 | p.222~279 | ✅         |
| 5주차 | p.282~325 | ✅         |
| 6주차 | p.328~379 | 🍽️         |
| 7주차 | p.382~430 | 🍽️         |

<br>

<!-- 여기까진 그대로 둬 주세요-->


# 1️⃣ 개념 정리 

## 01. 맷플롯립 기본 요소 알아보기

<!-- 새롭게 배운 내용을 자유롭게 정리해주세요.-->
맷플롯립은 데이터를 그래프로 표현할 수 있게 해주는 파이썬 라이브러리이다. 그래프 전체를 담는 Figure
객체가 있고, 그 안에 실제 그래프가 그려지는 Subplot(서브플롯)이 들어간다.
Figure: 그래프 전체를 담는 가장 큰 영역이다.
rcParams: 맷플롯립 그래프의 기본 설정을 관리한다. 예를 들어 그래프의 기본 DPI나 마커 모양 등을 변경할 수 있다.
Marker: 그래프에서 각각의 데이터 값을 표시하는 모양이다. 기본 마커는 동그라미이며, marker 매개변수로 모양을 바꿀 수 있다.
Subplot: 하나의 Figure 안에 여러 개의 그래프를 배치할 때 사용한다.
set_title(): 서브플롯의 제목을 지정한다.
set_xlabel() / set_ylabel(): 각각 X축과 Y축의 이름을 지정한다.

## 02. 선 그래프와 막대 그래프 그리기

<!-- 새롭게 배운 내용을 자유롭게 정리해주세요.-->
선 그래프는 데이터 포인트를 선으로 연결하여 데이터의 변화나 추세를 확인하기 좋은 그래프이다. plot() 함수를 사용하며, 첫 번째 값은 X축, 두 번째 값은 Y축에 해당한다. 

plt.plot(x, y)

선 그래프에는 marker, linestyle, color 등의 매개변수를 사용하여 선의 모양이나 색상, 데이터 포인트의 모양을 변경할 수 있다.

plt.plot(x, y, marker='.', linestyle=':', color='red')

plt.plot(x, y, '*-g')

plt.bar(x, y)

plt.bar(x, y, width=0.7)

막대 그래프는 데이터의 크기를 막대의 높이로 나타내는 그래프이다. bar() 함수를 사용한다.

plt.bar(x, y)

plt.bar(x, y, width=0.7)

# 2️⃣ 수행 인증

<!-- 교재에서 안내된 과정을 직접 실행해본 뒤, 진행 결과가 보이도록 4~6장의 스크린샷을 캡처하여 아래에 첨부해주세요.-->
<img width="980" height="722" alt="image" src="https://github.com/user-attachments/assets/281580ad-b1cf-4a57-940b-61664c4091c4" />
<img width="791" height="773" alt="image" src="https://github.com/user-attachments/assets/d720ec63-251c-4ef1-bd71-78fbfaaf4695" />
<img width="735" height="460" alt="image" src="https://github.com/user-attachments/assets/360e3c40-0bef-4d25-bb25-81576823c1b1" />
<img width="672" height="617" alt="image" src="https://github.com/user-attachments/assets/474b1713-c8cf-4bfa-8708-8051bed6ce72" />
<img width="782" height="777" alt="image" src="https://github.com/user-attachments/assets/9ea4a140-0b51-493a-9d3b-fac006c06f2a" />



<br>
<br>

# 3️⃣ 확인 문제

## 문제 1.

> **🧚Q. 다음 데이터를 이용하여 matplotlib으로 선그래프를 그리는 코드를 작성해주세요.**
- x = [1, 2, 3, 4, 5]
- y = [2, 4, 6, 8, 10]
> 조건은 아래와 같습니다.

1️⃣ 제목은 "Linear Trend"로 설정해주세요.
2️⃣ x축 이름은 "X values"로 설정해주세요.
3️⃣ y축 이름은 "Y values"로 설정해주세요.
4️⃣ 마커(marker)를 포함하여 선그래프를 그려주세요.


import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]
y = [2, 4, 6, 8, 10]

plt.plot(x, y, marker='o')
plt.title('Linear Trend')
plt.xlabel('X values')
plt.ylabel('Y values')
plt.show()




### 🎉 수고하셨습니다.




