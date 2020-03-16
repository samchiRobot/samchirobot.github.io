---
layout: post
title: "Nvidia Graphic Driver 설치 (18.04)"
date: 2020-03-16
categories: [Linux]
tags: [Development]
background: '/img/200315_rcS.png'
---

16.04 버전 우분투에서 그래픽 카드를 설치하려면 GUI 내리고 CLI로 전환해서 작업해야했다.   하지만 해당 방식은 잘못했다간 무한 로그인 문제가 발생해 우분투를 처음부터 재설치해야 되는 문제가 발생한다.

다행히 18.04에서는 해당 방식을 사용하지 않고 설치할 수 있다.

Nvidia 사이트로 들어가 [드라이버 다운로드 페이지](https://www.nvidia.co.kr/Download/index.aspx?lang=kr)로 이동

![200316-nvidia_driver_download.png](/img/200316_nvidia_driver.png)

자신이 소유한 드라이버(예시 : RTX 2060)를 선택, `검색`버튼을 누르면 드라이버 파일이 나옴

![200316_nvidia_RTX.png](/img/200316_nvidia_RTX.png)

![](/img/200316_Driver_download.png)

`다운로드` 버튼을 누르면 `.run`파일이 다운로드 됨

![200316_run_file_download.png](/img/200316_run_file_download.png)

해당 파일을 실행하기 위해서 실행 권한을 부여 (받은 파일의 버전에 맞추어 입력)

```bash
sudo chmod +x NVIDIA-Linux-x86_64-430.34.run
```

그리고 실행
```bash
./NVIDIA-Linux-x86_64-430.34.run
```

무언가 뜰 때마다 OK해주면 된다. (전부 설치해주면 된다.)  
설치가 완료되면 다음 명령어를 통해 설치확인
```bash
nvidia-smi
```

아래와 같이 뜨면 완료
![200316_nvidia_smi.png](/img/200316_nvidia_smi.png)

## 참고
설치파일 실행 중 오류가 발생하는 경우가 있다.  
해당 현상은 보통 g++과 같은 의존성 패키지가 설치되지 않아서 발생한다. 로그를 보고 해당 패키지를 설치하면 어느정도 해결될 것이다. (경우의 수가 많아 정리는 못함)