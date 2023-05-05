# 슈퍼히어로 데이터로 보는 군집화 알고리즘 비교
- Member: 머신러닝 위키 팀
- Status: Complete
- Tag: Project

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

## 4. 프로젝트 진행 과정
### 4.1. 데이터 전처리
- 결측치 확인 및 제거
- 데이터 타입 변환
- 이상치 확인
- 로그 변환
- 스케일링
- 차원축소(PCA)

### 4.2. 군집분석(Clustering Analysis)















