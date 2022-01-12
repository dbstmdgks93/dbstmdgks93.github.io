---
layout: post
title:  "05 : When to Change Dev/Test Sets and Metrics?"
date:   2022-01-12
excerpt: ""
tag:
- Coursera - Structuring Machine Learning Projects
comments: false
---



# 소개

Dev Set과 평가 지표를 설정하는 것은 팀이 특정 목표를 지향할 수 있도록 방향성을 제시하는 것이다.

하지만 프로젝트 진행 도중에 잘못된 방향이었다는 것을 깨달을 수도 있다.

그럴 때는 목표를 이동시켜야 한다.





# Cat dataset examples

만약 분류 작업에서 에러를 체크했을 때

* Algorithm A : 3% error

* Algorithm B : 5% error

겉으로 보기에는 A알고리즘이 더 낫다고 평가할 수 있다.



하지만 직접 시현했을 때 A알고리즘이 포르노 이미지를 많이 허용한다면 분류정확도가 아니라 다른 관점에서 문제가 클 수 있다.

만약 Algorithm B가 포르노를 잘걸러낸다면 B가 더 좋을 수도 있을 것이다.



이런 상황에서 Dev set은 A알고리즘을 선호하고, 유저는 B알고리즘을 선호하게 된다.

이럴 경우 Dev set이나 Test Set을 바꿔야 할 수 있다. 혹은 평가 metric을 바꿔야 할 것이다.



## metric을 바꾸는 방법

그냥 정확도는 이러한 문제를 해결할 수 없기 때문에 정확도에 포르노 이미지일 경우 loss를 굉장히 크게 높이는 가중치를 추가하는 방법이 있다. 100을 곱한다거나 하는 것이다.

여러가지 방법이 있을 수 있다.



이전 오류 메트릭이 만족스럽지 않다면 메트릭을 새롭게 정의해보라



## Cat dataset example 에서의 결론

첫 번째 단계는 수행하고 싶은 것을 잡아내도록 metric을 먼저 설정한 다음, 그 외의 목표를 다시 생각해보는 것이 순서이다.

Orthogonality의 철학을 지켜라.





# 다른 예시

* Algorithm A : 3% error

* Algorithm B : 5% error

일 때, 실제로 출시하면 B가 더 잘 작동한다고 생각해보자.

그 이유를 추적하다가 Dev / Test set 은 고해상도였고, 사용자가 사용하는 것은 저해상도였다는 것을 알아냈다고 가정해보자.



## 가이드라인

먼저 metric을 잘해라.

그런데 실제환경에서 잘 작동하지 않았다면, 그 때 dev set과 test set을 바꿔라



# 결론

평가 metric 과 dev set을 구축함으로써 우리는 알고리즘을 평가할 수 있게 된다.

평가 metric과 dev set을 완벽하게 평가할 수는 없지만 권장사항은 팀의 반복수행을 돕기 위해 한 가지를 빨리 세팅하는 것이다.

나중에 안좋은 것이라고 판명이 나거나 더 좋은 아이디어가 떠오르면 그 때 바꾸는 것이다.

오랫동안 이 평가작업을 붙잡고 있는 것은 권장하지 않는다.





