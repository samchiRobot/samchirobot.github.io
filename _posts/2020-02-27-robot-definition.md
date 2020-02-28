---
layout: post
title: "[Robotics] 로봇의 정의"
date: 2020-02-27
tags: [Robotics, Theory]
background: '/img/200227_Robot_chaos_map.png'
---

## 로봇은 무엇인가?

영문위키에서는 로봇은 다음과 같이 정의한다. (나도 이 정의가 로봇의 목적과 가장 맞다고 생각한다.)

 *로봇은 컴퓨터를 이용하여 프로그래밍 할 수 있는 기계이며, 복잡한 일련의 동작을 자동으로 수행할 수 있음* [[1]](https://en.wikipedia.org/w/index.php?search=Robot&title=Special%3ASearch) 

 로봇은 목적에 따라 설계되어 크기와 형태가 다양하다. 그렇기에 사람형태가 아닌 것이 많다.

![2019 Robot chaos map[2]](/img/200227_Robot_chaos_map.png)

## 로봇의 3요소

크기와 모양에 관계없이 로봇은 3가지 요소를 가진다.

- Perception (인식)
- Decision Making (의사결정)
- Action (행동)

해당요소는 독립적이지 않고 서로 의존적이다. 
예를 들어, 로봇이 어느 공간에서 임의의 목적지로 이동한다고 가정하면 다음과 같은 시나리오로 반복하여 움직일 것이다. 

- 센서를 통해 로봇은 자신이 처한 상황을 인식 (perception) 
- 센서 데이터를 기반으로 목적지로 이동하기 위한 갈 수 있는지 여부 결정과와 경로계획 설정 (decision making)
- 모터에 명령을 내려 이동 (action)

 각 항목은 매우 중요한 요소이므로 차근차근 정리할 것이다.  

## 참고문헌

[1] Definition of 'robot'. Oxford English Dictionary. Retrieved November 27, 2016.

[2] https://robo-lib.com/repositories/summary/134 
