---
layout: post
title: "의사결정 (Decision making)"
date: 2020-03-01
categories: [Robotics]
tags: [Robotics, Theory]
background: '/img/mogura.jpg'
---

## 로봇의 의사결정

로봇은 다양한 센서로부터 받은 데이터와 로봇의 초기상태를 기반으로 의사결정을 하게 된다.

의사결정은 결국 컴퓨터가 하는 일이기에 자료구조와 알고리즘을 이해하는 것이 중요하다.
그리고 이러한 의사결정을 위한 질문은 아래 예시와 같이 예/아니오로 대답할 수 있을 정도로 간단해야한다.

- 목표로 하는 위치까지 갈 수 있는가?
- 목표 물체가 책상 위에 있는가?

하지만, 실제로 로봇은 한가지 행동에 진행하기전에 무수히 많은 질문에 대하여 의사결정을 하게 된다. 이는 자료구조의 [이진탐색트리(binary search tree)](https://en.wikipedia.org/wiki/Binary_search_tree)와 비슷하다고 볼 수 있다.

![Binary search tree[1]](https://upload.wikimedia.org/wikipedia/commons/thumb/d/da/Binary_search_tree.svg/320px-Binary_search_tree.svg.png?1583051812250 "Binary search tree[1]"){: .center}

## 로봇의 경로계획

로봇의 의사결정에서 가장 중요한 것은 [경로계획(path planning)](https://en.wikipedia.org/wiki/Motion_planning)이라 할 수 있다.
로봇팔이 움직이는 경우도 경로계획이라 할 수 있지만, 여기에서는 이동하는 경우만 생각하기로 한다.

로봇의 이동은 다음 순서로 의사결정을 하게 된다. 
- 해당 목적지까지 이동할 수 있는가?
- 어느 경로로 가야 가장 효율적인가?

![](https://en.wikipedia.org/wiki/Dijkstra%27s_algorithm#/media/File:Dijkstras_progress_animation.gif)

경로계획에 많이 쓰이는 알고리즘에는 [Dijkstra](https://en.wikipedia.org/wiki/Dijkstra%27s_algorithm), [A\*](https://en.wikipedia.org/wiki/A*_search_algorithm), [RRT](https://en.wikipedia.org/wiki/Rapidly-exploring_random_tree)가 있다.

각 부분에 대한 자세한 내용은 다른 챕터에서 다룰 것이며, 이 페이지에 링크로 달아 계속 업데이트 할 예정이다.

## Reference
[1] https://en.wikipedia.org/wiki/Binary_search_tree