---
layout: post
title: "멀티부팅 환경에서 Windows의 시간이 깨지는 이슈 해결"
date: 2020-03-15
categories: [Linux, Windows]
tags: [Development]
background: '/img/200315_rcS.png'
---

현재 내 데스크톱에는 우분투, 윈도우를 멀티부팅으로 세팅되어있다. 
근데 우분투를 설치하게 되면 윈도우의 시계가 맞지 않는 이슈가 발생한다.

[KRISS](https://www.kriss.re.kr/index.do) 에서 만든 프로그램인 [UTCk](https://www.kriss.re.kr/standard/view.do?pg=standard_set_01)를 이용하여 윈도우의 타임서버를 변경하여 동기화 하는 방법이 있다.
해당 방법은 효과적이지만, 시간이 안맞는다는 문제 해결을 위해 프로그램을 깔고 동작시켜야 한다는 단점이 있다.

그래서 근본적인 문제인 우분투에서 UTC 해석방법을 변경하여 윈도우 시간을 변경하는 방법을 소개하고자 한다.

리눅스에서 터미널을 열어 다음 명령 실행

```bash
timedatectl set-local-rtc 1
```

재부팅 후에도 변경사항이 적용되도록 `/etc/default/rcS`를 열어(터미널에서 아래 명령어 실행) `UTC=no`를 수정하거나 가장 아래에 추가

```bash
sudo gedit /etc/default/rcS
```

![/etc/default/rcS](/img/200315_rcS.png)

재부팅하면 설정 완료

## Reference
[1] [https://www.tuwlab.com/ece/28472](https://www.tuwlab.com/ece/28472)  
[2] [http://www.webupd8.org/2014/09/dual-boot-fix-time-differences-between.html](http://www.webupd8.org/2014/09/dual-boot-fix-time-differences-between.html)