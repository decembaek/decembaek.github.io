---
layout: single
title: "서버 설치, WSL설치하기 우분투 22.04 - 2"
categories: [It, Server]
tag: [it, linux]
toc: true
---

# 집에서 서버 마련하기 ch 2

가상환경 VirtualBox로 우분투를 돌렸는데 너무 무겁다는 단점이 있다.

윈도우10에서 지원하는 WSL을 사용해서 우분투를 돌리도록 하자

## WSL 설치하기 

관리자 권한으로 PowerShell 또는 cmd(명령 프롬프트) 를 실행하자

```css
wsl --install
또는 
wsl --install -d Ubuntu-22.04     # 마지막 숫자는 버전을 적어주면됌
```

명령어 실행 후 컴퓨터 다시시작을 하자 

```
shutdown -r -t 0
```



Microsoft Store 에서 리눅스 배포판 설치 

![error]({{site.url}}/images/2023-04-25-HOME-SERVER/wsl.PNG)

명령어 wsl을 쳐서 우분투를 켜보자 
