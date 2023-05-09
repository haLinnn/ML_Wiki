# 슈퍼히어로 데이터로 보는 군집화 알고리즘 비교
- Member: deep daiv. 머신러닝 위키 팀
- Status: Complete
- Period: 22.12.22 ~ 23.01.07

## 1. 주제 선정 이유

저희는 슈퍼히어로 영화 특히 ‘마블’의 오랜 팬입니다. 그런데 마블의 행보가 심상치 않습니다. ‘마블 페이즈4’의 시작을 알리는 영화 ‘블랙 위도우’와 ‘상치와 텐 링즈 전설’부터 내리막길을 걸으며 팬들의 아쉬움 자아내고 있습니다. 이렇게 인기가 줄어들고 있는 이유가 무엇일까요?

많은 사람들은 입을 모아 **아이언맨, 캡틴아메리카와 같은 매력적인 캐릭터의 부재**를 외치고 있습니다. 군집화를 통해 **이들의 역할을 대신할 슈퍼히어로**를 찾아보고자 합니다.

<p align="center"><img src="https://user-images.githubusercontent.com/108817458/236495279-f05b5499-0a15-4e18-9253-825c85cd0b2f.jpeg" weight=600 height=300/></p>

## 2. 문제 해결 아이디어
1. **Kaggle의 Kaggle의 Superheroes NLP Dataset 이용**

2. **군집화 이론 정리 및 최적의 군집 형성**
    
    ✔️ K-Means, DBSCAN 알고리즘 비교 및 적용할 알고리즘 선정
    
    ✔️ 최적의 하이퍼파라미터 선정 및 최적의 군집 형성
    
3. **‘아이언맨’, ‘캡틴 아메리카’가 속한 군집 내 대체 가능한 슈퍼히어로 선정**

## 3. 데이터 소개
- Kaggle의 Kaggle의 Superheroes NLP Dataset
- 81개의 컬럼 중 분석에 필요한 8개의 컬럼만 사용

|Feature|Type|Description|
|------|---|---|
|name|object|히어로 이름|
|overall_score|object|종합 점수|
|intelligence_score|int64|지능 점수|
|strength_score|int64|체력 점수|
|speed_score|int64|스피드 점수|
|durability_score|int64|내구성 점수|
|power_score|int64|파워 점수|
|combat_score|int64|전투 점수|

## 4. PCA(주성분 분석, Principle Component Analysis)

데이터 결측치 및 이상치 제거, MinMax 스케일링 등의 전처리를 한 후 데이터의 분포를 시각화하기 위해 PCA를 사용하여 2차원으로 차원 축소

<p align="center"><img src="https://github.com/haLinnn/ML_Wiki/assets/108817458/d134d61c-6633-4c49-b720-aa7a6320a4ff" weight=800 height=600/></p>


## 5. K-Means 군집 분석

### 5.1. 최적의 k값 선정

- 최적의 k값을 찾기 위해 Elbow method를 적용

    ![Untitled](https://github.com/haLinnn/ML_Wiki/assets/108817458/243a5a25-dc6b-4438-a836-b0ffa6820285)
    
- 실루엣 계수 비교
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/3b9de5ed-ac1e-42d1-aba2-1c5d05e1f1d6/Untitled.png)
    
- KElbowVisualizer를 사용하여 최적의 k값 선정
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/cbf511f5-4d35-40e2-8521-b57156ca63fc/Untitled.png)
    

### 5.2. 군집별 시각화

- SilhouetteVisualizer를 통한 시각화
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/a07fce9f-30cc-4c49-8b01-38e75f3cee4c/Untitled.png)
    
- scatter plot을 통한 군집별 시각화

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/ccbc5540-3ff3-4ce6-a7c2-c59752df281c/Untitled.png)

## 6. 결과

### 6.1. 히어로 군집 확인

아이언맨과 캡틴 아메리카가 속한 군집을 확인해본 결과 아이언맨은 1번 군집에, 캡틴 아메리카는 0번 군집에 속하였습니다.

다음은 아이언맨 군집과 캡틴아메리카 군집의 평균 능력치를 시각화한 결과입니다.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/ca5a68a0-5fc2-439a-89c0-7deb3c1e89ac/Untitled.png)

위 결과를 통해 아이언맨 군집이 캡틴 아메리카 군집보다 대체적으로 높은 능력치를 가지고 있음을 알 수 있습니다.

### 6.2. 대체 히어로 후보

아이언맨의 대체 히어로 후보는 아이언맨과 같은 1번 군집에 속한 히어로들입니다. 예로는 A-Bomb, Abomination, Wonder Woman 등이 있습니다.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/f716f856-4429-4123-a85e-ee26673a3f7a/Untitled.png)

캡틴 아메리카의 대체 히어로 후보는 캡틴 아메리카과 같은 0번 군집에 속한 히어로들입니다. 예로는 Aayla Secura, Yondu 등이 있습니다.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/ff50cfeb-1982-4d49-b420-fbf45a5a4765/Untitled.png)














