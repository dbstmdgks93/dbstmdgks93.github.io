---
layout: post
title:  "Orthogonalization"
date:   2022-01-05
excerpt: ""
tag:
- Coursera - Structuring Machine Learning Projects
comments: false
---





# 소개

머신러닝 업무를 효과적으로 수행하는 사람들은 하나의 효과를 얻기 위해 무엇을 튜닝할지에 대해서 정확한 안목을 갖고 있다.





# Orthogonalization

직교화는 TV 디자이너들이 하나의 손잡이가 하나의 기능만을 제어할 수 있도록 만드는 것을 의미했다.

자동차에서도 하나의 레버는 하나의 기능만을 제어하는 것을 볼 수 있다.





# Chain of assumptions in ML

training set -> dev set -> test set -> real world 로 데이터가 바뀔 때 잘 작동해야 한다.

본인이 설계한 알고리즘이 학습데이터와 잘 안맞는 경우 하나씩 조절해보는 것이 좋다.

1. 더 큰 네트워크
2. 다른 최적화 함수



## training set 에서는 잘되는데 dev set에서 잘 안되는 경우

1. Regularization 적용
2. 더 큰 training data set 사용



## test set에서 안되는 경우

1. 더 큰 dev set 사용



## real world에서 안되는 경우

1. 더 큰 dev set 사용
2. cost function의 변경



early stopping의 경우 training set에서 학습시킬 때, dev set에서 테스트할 때 둘 다 쓰이는 테크닉인데 정확히 어떤 부분을 효율적으로 하기 위해 적용하는 것인지 알기 어렵다.

