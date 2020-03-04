---
layout: post
title: "fcitx를 이용한 한글 입력"
date: 2020-03-04
categories: [Linux]
tags: [Development]
background: '/img/mogura.jpg'
---

## fcitx 설치 및 세팅

```bash
sudo apt update
sudo apt install fcitx-hangul
```
`Windows키`를 눌러 시작화면이 뜨면 `language support`를 입력한다. 그러면 다음과 같은 창이 뜨면서 업데이트 표시가 뜬다. 업데이트를 진행한다.

![업데이트 중인 모습](/img/200304_applying_changes.png)

업데이트가 완료되면 `Install / Remove Languages`에 들어가 `Korean`이 체크된 것을 확인  
(안되어있으면 체크하고 Apply)

![Installed Languages 항목](/img/200304_installed_languages.png)

`Language for menus and windows` 항목에 한국어가 추가되었는지 확인한 다음, `Keyboard input method system`을 아까 설치한 fcitx`로 선택하고 close

![Language_support 항목](/img/200304_Language_support.png)

이후 재부팅 진행
```bash
sudo reboot
```

재부팅 완료하면 오른쪽 위에 키보드 아이콘이 생성되는 것을 볼 수 있음  
`Windows키`를 누르고 fcitx configuration 입력하고 들어가 `+버튼` 선택  
`Only show Current Language`의 체크를 해제한 뒤, 검색창에 `hangul` 입력하면 아래 예시과 같이 한글이 뜸

![Add input method 항목](/img/200304_Add_input_method.png)

## 한영키를 이용한 언어전환
windows 키를 누르고 fcitx configuration 입력하고 들어가 'Global Config' 탭 선택  
Trigger Input Method를 클릭한 뒤 한영키 누르면 세팅 완료

### 참고. Ubuntu 16.04 이하 버전의 경우
`Ubuntu 16.04` 이하 버전은 `한영키` 누르면 HUD 빠른 실행과 겹치는 문제가 있음  
`Windows키`를 누르고 `keyboard` 입력하고 들어가 `Launcher` 선택하여 `HUD`를 `disabled` 시키면 됨  
(더블클릭한 다음, `backspace`를 누르면 disable 됨)