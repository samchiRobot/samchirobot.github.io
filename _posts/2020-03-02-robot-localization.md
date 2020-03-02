---
layout: post
title: "위치인식 (Localization)"
date: 2020-03-02
categories: [Robotics]
tags: [Robotics, Theory]
background: '/img/mogura.jpg'
---

## 로봇의 위치인식

위치인식은 지도가 작성된 환경에서 로봇의 위치와 자세를 결정하는 방법이다.

이는 확률적 알고리즘(probabilistic algorithm)을 기반으로 둔다. 해당 알고리즘은 측정된 센서 노이즈를 필터링하면서 로봇의 위치와 자세를 추적하는데 사용된다.

지도가 있는 환경의 임의의 위치에서 로봇이 움직인다고 가정하면, 로봇은 이동하며 주변 환경을 측정하면서, 자신의 위치를 확률론적 모델을 이용하여 추정하게 된다.

해당 방식은 처음에는 정보가 적어 부정확한 위치도 추정하기에 정확도가 낮다. 하지만, 시간이 지날수록 누적된 정보에 의해 부정확한 위치에 대한 추정은 사라지게 되어 정확한 위치를 추정할 수 있게 된다. (아래 예제(AMCL) 참조, 파란점이 로봇이 있을 것으로 판단되는 지점이다[1].)

![AMCL update before](/img/200302_MCL_global_localization_before.png)

![AMCL update after](/img/200302_MCL_global_localization_after.png)

위치 인식에 사용되는 대표적인 알고리즘은 다음과 같다.

- [Extended Kalman Filter (EKF)](https://en.wikipedia.org/wiki/Extended_Kalman_filter) : 비선형 모델에 대하여 상태를 추정하는 알고리즘
- [Markov Localization](https://www.cs.cmu.edu/afs/cs/project/jair/pub/volume11/fox99a-html/node2.html) : Bayesian filter 개념을 기반, 확률 분포를 이용하여 모든 로봇의 가능한 위치를 추정하는 방법
- [Grid Localization](http://www.cs.columbia.edu/~allen/F15/NOTES/localization_1_to_4.pdf) : 로봇의 위치를 grid를 이용하여 추정하는 방법
- [Monte Carlo Localization (particle filter)](https://en.wikipedia.org/wiki/Monte_Carlo_localization) : particle을 이용하여 로봇의 위치를 추정

해당 알고리즘 부분에 대해서는 차근차근 정리할 예정이다.

## Reference
[1] https://www.mathworks.com/help/nav/ug/monte-carlo-localization-algorithm.html