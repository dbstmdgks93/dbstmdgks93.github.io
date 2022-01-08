---
layout: post
title:  "04 : Train,Dev,Test Distributions"
date:   2022-01-08
excerpt: ""
tag:
- Coursera - Structuring Machine Learning Projects
comments: false
---



# 소개

어떻게 하면 데이터셋을 잘 구성할 수 있을까?





# Cat classification dev/test sets

일반적인 머신러닝의 업무 플로우는 다양한 아이디어를 시도해보고, 다양한 모델을 훈련시켜보고, dev set으로 평가하면서 성능을 향상시키고, 마음에 드는 것으로 test set에서 실험하는 것이다.

예를 들어서 고양이 분류 데이터셋이 있다고 해보자.

고양이 분류기를 만들고 있다고 생각해보자.



지역은

* US
* UK
* Other Europe
* South America
* India
* China
* Other Asia
* Australia

이렇게 있다고 치자

Dev Set과 Test Set을 정하는 한 가지 방법은 무작위로 지역을 4개씩 나누는 것이다. 좋지 않은 방법이다. 왜냐하면 분포가 달라지기 때문이다.

Dev Set과 Metric을 같이 정하길 바란다. 그래야 분류기를 좋은 것으로 잘 고를 수 있게 된다. 과녁을 잘 가르쳐줘야 하기 때문이다.

그렇다면 모든 데이터를 shuffling해서 나누는게 가장 좋은 것 같다.





# 실제 이야기

어떤 지역에서 대출을 받는 사람들이 실제 상환능력이 되는지 예측하는 프로그램을 만들기 위해 3개월간 노력했는데 사실 예측하고 싶은 지역이 다른 지역이어서 헛고생이 된 적이 있다고 한다.





# 결론

Dev set과 Test Set은 같은 분포도에서 만들어져야 한다.

기억해야 하는 것은

dev set과 metric을 결정하는 것이다. 그래야 팀이 목표하는 타깃을 맞출 수 있게 된다. 



