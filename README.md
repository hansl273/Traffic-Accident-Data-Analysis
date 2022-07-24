# Traffic-Accident-Data-Analysis
Traffic Accident Data Analysis(EDA, Apriori, Hybrid Model)
![image](https://user-images.githubusercontent.com/106146283/177912974-7d4fadb4-8781-455c-b5f1-7d09d28879de.png)

1. 의사결정나무는 분류나무, 회귀나무로 구분

분류나무
목표변수가 이산형인 분류나무는 상위 노드에서 가지분할을 할 때 분류 변수와 분류 기준값의 선택 방법으로 카이제곱통계량의 p값, 지니 지수, 엔트로피 지수 등이 사용된다.
 카이제곱 통계량의 p값은 작을수록, 지니 지수와 엔트로피 지수는 클수록 자식노드 내 이질성이 큼을 의미한다. 따라서 이질성이 작아지는 방향으로 가지분할을 수행해야 한다.
- 지니 지수 : 지니 지수는 불순도를 측정하는 방법으로 작을수록 분류가 잘 됨을 의미한다. 

회귀나무
목표변수가 연속형인 회귀나무의 경우 분류변수와 분류 기준 값의 선택 방법으로는 F 통계량의 p값, 분산의 감소량 등을 사용한다. F 통계량은 일원배치법에서의 검정 통계량으로서 값이 클수록 오차의 변동에 비해 처리 변동이 큼을 의미하므로 값이 커지는 방향으로 가지분할을 수행하게 된다. 분산의 감소량도 값이 최대화되는 방향으로 가지분할을 수행한다.
- 정지규칙 : 더 이상 분리가 일어나지 않고 현재 마디가 최종마디가 되도록 하는 여러 규칙으로 최대 나무의 깊이, 최소 관측치 수, 카이제곱통계량, 지니 지수, 엔트로피 지수 등이 있다.

![image](https://user-images.githubusercontent.com/106146283/180670140-52e493f6-974b-4969-9f44-964da79d1a5d.png)

2. Random Forest - 랜덤포레스트

정의

앙상블 기법이며 의사나무결정(Decision Tree)을 여러개로 훈련시킨 후 그 정확도의 평균을 구하는 기법

​

장점

일반화 및 성능 우수

파라미터 조정 용이

데이터 scale, 즉 단위의 영향을 받지 않음

Overfitting, 과적합이 잘 되지 않음 - 여러 모델의 평균을 구하기 때문

​

단점

개별 트리 분석이 어렵고 트리 분리가 복잡해 지는 경향 존재

차원이 크고 희소한 데이터는 성능 미흡(e.g., text data)

모델 성능 개선이 어려움

훈련 시 메모리 소모가 큼


3. KNN - K Nearest Neighbor

정의

데이터를 비슷한 부류끼리 모아 분류하여 라벨링 하는 분류 지도학습의 일부이며 데이터들끼리의 2차원 평면안에서 거리를 계산하여 라벨링을 한다

*데이터들 간의 거리: 유클리디안 거리(피타고라스)를 기준으로 계산

​

장점

구현하기 쉬운 알고리즘

단순 효율

훈련 단계 빠름

수치 기반 데이터 분류 작업에서의 성능 우수

​

단점

모델 생성이 없어 특징과 클래스 관계 이해가 제한적

적절한 k선택이 필요. 분류 단계가 많으면 성능에 문제가 생긴다

데이터가 많으면 분류 단계가 느려짐


