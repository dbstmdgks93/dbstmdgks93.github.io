---
layout: post
title:  "03 : Satisficing and Optimizing Metric"
date:   2022-01-07
excerpt: ""
tag:
- Coursera - Structuring Machine Learning Projects
comments: false
---





# 소개

중요시 여기는 모든 부분을 single row number로 평가하는 것은 어렵다.





# 예시 1

Accuracy와 Running Time이라는 척도에 따라 classifier를 평가한다고 가정해보자.

두 가지를 고려할 수 있는 한 가지 예시는 accuracy - 0.5 * running time  이 있을 것이다.

그 외에는 정확도를 maximize 하고, satisificing metric으로 100ms 보다만 작게하는 방법도 있다.

신중히 생각하는 N개의 행렬이 있으면 한 가지를 최적화된 것으로 고르는 것이 합리적이다. 나머지 N-1개는 satisficing metric으로 두자.



# 예시 2

wake words를 감지하는 시스템을 만든다고 해보자.  (= trigger words)

보통 음성인식 기기를 깨우는 말을 말한다. 예를들면 "헤이 구글" 이 있겠다.



trigger word detection 의 정확도를 신경쓸 수 있을 것이다. 

이럴 때는 false positive, false negative에 관심을 가질 수 있다.



이 경우 정확도를 먼저 최대화 한 다음

24시간에 1번 이하의 false negative만 허용한다 정도로 합의를 볼 수 있다.

false negative 가 satisficing metric 이 된다.

