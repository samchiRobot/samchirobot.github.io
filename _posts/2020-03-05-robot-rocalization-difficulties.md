---
layout: post
title: "위치인식의 어려운점"
date: 2020-03-05
categories: [Robotics]
tags: [Robotics, Theory]
background: '/img/mogura.jpg'
---

로봇이 위치인식하는데 가장 어려운 점은 크게 세 가지로 나눌 수 있다.

## 1. Position tracking (local localization)
로봇이 자신의 초기 위치를 안다고 가정하면, 움직이면서 자신의 위치를 추정하게 된다.
하지만, 로봇은 움직일 때마다 항상 자신의 위치에 불확실성이 발생하여 위치추정에도 영향을 끼친다. 이러한 불확실성은 로봇의 주변 환경에만 국한되기에 local localization이라고도 불린다.

## 2. Global localization
로봇이 자신의 초기 위치를 모른다고 가정하면, 로봇은 자신의 환경 정보와 ground truth map을 대조하여 자신의 위치를 추정해야한다.
Global localization의 불확실성 정도는 position tracking 보다 훨씬 크기에 훨씬 어려운 문제라고 볼 수 있다.

## 3. Kidnapped problem
해당 문제는 global localization 문제와 비슷하다고 볼 수 있는데, 다른 점은 로봇이 갑자기 순간이동 한 것과 같이 갑자기 다른 위치로 이동해서 위치추정을 해야하는 문제이다. 이름처럼 로봇이 납치되었다고 볼 수 있다. 가장 최악인 문제로 볼 수 있으나 로봇에게 흔히 발생하는 문제이기에 이를 해결할 수 있어야 한다.
