# 다음 분기에 어떤 게임을 설계해야 할 것인가?
* **개요** : 게임 판매량 데이터를 바탕으로 한 트렌드 파악 및 다음 분기 출시해야할 게임 설계
* **진행 기간** : 2022. 02. 11 ~ 2022. 02. 17
* **사용 스킬** : `pandas` `matplotlib` `seaborn` `scipy` `t-test`

### &nbsp;

## *I. 프로젝트 계획 수립*
### 프로젝트 진행 배경
* ㅇㅇㅇ

### 데이터 확인
* **데이터 출처** : [Kaggle - Video Game Sales Dataset](https://www.kaggle.com/datasets/gregorut/videogamesales)
* **데이터 설명** : 1980년부터 2020년까지 출시된 게임들의 판매량 데이터
* **데이터 수** : 16599

<img width="1015" alt="스크린샷 2022-09-01 오후 7 25 07" src="https://user-images.githubusercontent.com/97662174/187895979-6aa7ad2b-200e-4af6-966e-263f668871b2.png">

|Features|Description|Data Type|
|:---:|---|:---:|
|Name|게임의 이름|Categorical|
|Platform|게임이 지원되는 플랫폼|Categorical|
|Year|게임이 출시된 연도|Numerical|
|Genre|게임의 장르|Categorical|
|Publisher|게임을 제작한 출판사|Categorical|
|NA_Sales|북미지역에서의 출고량|Numerical|
|EU_Sales|유럽지역에서의 출고량|Numerical|
|JP_Sales|일본지역에서의 출고량|Numerical|
|Other_Sales|기타지역에서의 출고량|Numerical|

### 프로젝트 진행 방향
* 현재 존재하는 특성들을 바탕으로 다음 게임 설계에 사용할 수 있는 특성은 **플랫폼**과 **장르**
* 플랫폼과 장르와 출고량과의 관계를 확인하여 다음 분기에 출시할 게임의 플랫폼과 장르를 설계

### &nbsp;

## *II. 데이터 전처리 & Feature Engineering*
### 데이터 전처리
* 결측치(출시 연도, 장르) 처리
* 단위가 맞지 않는 값(출시 연도, 출고량)들을 일정한 단위로 변환

### Feature Engineering
* 범주가 너무 다양하여 특성으로 사용하기 부적절한 특성(출판사) 제거
* 기존 특성을 활용하여 새로운 특성(출시 연대, 총 출고량) 생성

### 데이터 전처리 및 Feature Engineering 결과

<img width="863" alt="스크린샷 2022-09-01 오후 7 45 29" src="https://user-images.githubusercontent.com/97662174/187896136-4bd9d29b-73d0-4576-aa3f-32b3097c8158.png">


|Features|Description|Data Type|
|:---:|---|:---:|
|Name|게임의 이름|Categorical|
|Platform|게임이 지원되는 플랫폼|Categorical|
|Era|게임이 출시된 연대|Categorical|
|Genre|게임의 장르|Categorical|
|NA_Sales|북미지역에서의 출고량|Numerical|
|EU_Sales|유럽지역에서의 출고량|Numerical|
|JP_Sales|일본지역에서의 출고량|Numerical|
|Other_Sales|기타지역에서의 출고량|Numerical|
|Total_Sales|모든지역에서의 출고량의 합|Numerical|


### &nbsp;

## *III. 데이터 시각화 & 분석*
### 출고량이 높은 게임들을 대상으로 분석
### 각 지역별 인기있는 게임에 대해 분석
### 연대별 인기있는 게임의 트렌드에 대해 분석
### 분석 결과

### &nbsp;

## *IV. 가설 생성 & 검정*
### 1. 북미 지역에서 다른 게임에 비해 더 잘 팔리는가?
### 전 세계에서 다른 게임에 비해 더 잘 팔리는가?

### &nbsp;

## *V. 결론*
* **다음 분기에 설계해야할 게임** : X360 기반 슈팅게임
* 가장 시장이 큰 북미지역 뿐 아니라 일본을 제외하면 다른 지역에서도 인기가 높고, 현재 제작되는 게임의 트렌드에도 부합하여 판매량이 높을 것으로 
