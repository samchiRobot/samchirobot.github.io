---
layout: post
title: "Chromium 설치 (Linux)"
date: 2020-03-05
categories: [Linux,Windows]
tags: [Development]
background: '/img/mogura.jpg'
---

## Chromium ?
Chromium은 오픈소스 웹브라우저 프로젝트 이며, Google Chrome은 해당 프로젝트를 기반으로 개발되었다.

### 설치방법 (Linux)

 Google Chrome에 비하여 설치가 간편함. (아래 명령어 하나로 OK)

```bash
sudo apt install chromium-browser
```

### 설치방법 (Windows)

아래 링크에 들어가 exe파일 다운받아 설치

https://chromium.woolyss.com/download/ko/


## 정보 [1]

### 라이선스
- 구글이 관여한 부분 : BSD
- 다른 부분 : MIT, LGPL, GPL 등 여러 오픈소스 라이선스가 적용됨 

### Google Chrome과 차이점
Chrome에는 있지만 Chromium에 없는 것은 다음과 같다.
- 구글 이름과 로고
- 사용자 식별 인증키 설정 요구사항
- 자동 업데이트
- 사용 정보 및 오류 보고서를 구글로 보내기 선택하기
- 사용 정보 추적(구글 웹사이트에서 구글 크롬을 다운로드하지 않을 경우에 이 코드가 포함되어 언제 어디서 구글 크롬을 다운로드했는지 등의 정보를 전송)
- 구글 크롬과는 다른 별도의 오픈소스 내장 PDF 뷰어
- 구글 크롬과는 다른 별도의 
- 내장 인쇄 미리보기와 인쇄 시스템
- 내장 어도비 플래시 플레이어

종합적으로 보면 Chromium이 Chrome보다 사용자 정보 수집이 적다는 점을 알 수 있다.

## Reference
[1] https://ko.wikipedia.org/wiki/%ED%81%AC%EB%A1%9C%EB%AF%B8%EC%97%84_(%EC%9B%B9_%EB%B8%8C%EB%9D%BC%EC%9A%B0%EC%A0%80)