---
layout: post
title: "인식 (Perception)"
date: 2020-02-29
categories: [Robotics]
tags: [Robotics, Theory]
background: '/img/mogura.jpg'
---

## 센서를 이용한 인식

로봇은 다양한 센서를 이용하여 주변 환경을 인식하고 신호처리를 통하여 유용한 정보로 만든다. (예시 : [ROS에서 지원하는 센서](http://wiki.ros.org/Sensors))

로봇은 사람과 같이 오감(시각, 청각, 촉각, 후각, 미각)을 갖고 느낄 수 있으며,

- 시각 : 카메라, LIDAR, RADAR, Depth camera, 초음파
- 청각 : 마이크로폰
- 후각, 미각 : 화학센서
- 촉각 : 압력센서, 온도센서, 근접센서

로봇은 오감 이외의 것도 감지할 수 있다.

- GPS<sup>\*</sup> : 실외에서의 로봇의 위치
- IMU<sup>\*\*</sup>, AHRS<sup>\*\*\*</sup> : 로봇의 기울기, 방향
- 기압계 : 고도

각 부분에 대한 자세한 내용은 다른 챕터에서 다룰 것이며, 이 페이지에 링크로 달아 계속 업데이트 할 예정이다.

---
<sup>\*</sup> Global Positioning System  
<sup>\*\*</sup> Inertial Measurement Unit  
<sup>\*\*\*</sup> Attitude and Heading Reference System 