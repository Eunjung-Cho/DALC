# kaggle_study
## EDA
### Titanic
#### 2021-01-23 : ddwu-bigdata-1week

**<새로 알게 된 것>** 
**EDA 전체적인 과정**
1) 분석 목적 설정: 얼마나 많이 생존 했는가? <-target값
- 이 타겟값의 distribution에 따라 문제를 풀어가는 방법이 달라진다. 
- 타겟을 먼저보는 이유: 어떤 matrix를 쓸 것인가 loss function 잴 때 matrix잰다. (auc) accuracy잰다

2) 시각화 하기 :  import matplotlib.pyplot as plt
%matplotlib inline

-> 여러가지 그래프 (어떤피처에 어떤 그래프가 어울릴지 고민!)
- 그래프 팁 -> 단지 개수(count), 평균값으로
- Tip : 특정 카테고리와 특정 카테고리가 가지고 있는 타겟의 평균값 <- 이걸 그리면 된다. 


3) feature에 대해서
category feature: 순서를 따질 수 x
ordinal feature: 순서를 따질 수 있다. (Pclass 등-> 수치적으로 비교가 가능하다.)
Countinous feature : 이어지는거 (age 등)
왜 데이터 타입을 알아야하는가? -> 처리하는 방법이 다르기 때문
numerical value:easy
string data가 까다롭다. ->category feature

* 보통 정형화 되어 있다. 
categoty encoder : 카테고리 처리방법
(https://contrib.scikit-learn.org/category_encoders/)-> 모르지만 그냥 쓴다 ㅎㅎ 코딩은 이미 되어있으니까 

이 카테고리를 어떻게 했을 때에 모델에 가장 좋게 넣을 수 있을까?? 등을 고민해야한다.

4) incoding에 대해서
Pclass : 순서가 있는 카테고리인 경우 -> 라벨 인코딩
What is Label incoding? : 카테고리 -> 숫자로 (순서가 생긴다!) 
ex) 학점 같은 경우도 ordinal (즉 라벨 인코딩 가능)

5) kaggle kernel 에서 시각화 자료 한글 깨짐 방지

**<공부해야 할 것>**
- encoding 종류 공부
: https://contrib.scikit-learn.org/category_encoders/
- factorplot -> catplot 으로 라이브러리 이름 renamed 
- 이상치,결측지 효과적인 제거 방법
