---
layout: single
title: "서버 설치, 집에서 서버열고 서비스 하기, 우분투 22.04 - 1"
categories: [It, Server]
tag: [it, linux]
toc: true
---

# 집에서 서버 마련하기 ch 1

집에서 서버를 한 번 만들어서 운영해볼려고 한다. 집 컴퓨터는 윈도우 10으로 64비트 환경이다.

## 설치 필수요소

1. 우분투 설치
2. 가상머신 설치

우선 윈도우에 우분투를 돌릴 가상머신과 우분투를 설치해준다. 

### 가상머신 설치 VirtualBox

사이트 주소 : https://www.virtualbox.org/wiki/Downloads 

VirtualBox 설치 사이트 이다. 들어가서 자신 운영체제에 맞는 버전을 설치한다. 

![1]({{site.url}}/images/2023-04-25-HOME-SERVER/1.png)

설치 시작하자 마자.. 오류 컴퓨터를 초기화 했더니 Microsoft Visual C++ 이 삭제되었나 보다 다시 설치해주도록 하자

![2]({{site.url}}/images/2023-04-25-HOME-SERVER/2.png)

이 에러는 설치하면 잠시 네트워크가 끊긴다는 경고이다..



가상머신이 완료되면 우분투를 설치하자 

### 우분투 22.04 설치 ubuntu 22.04 

사이트 주소 : https://releases.ubuntu.com/jammy/

들어가면 image 파일을 다운받으면 된다 (iso)

Desktop image : GUI가 설치되어 있는 버전

Server install image : CLI가 설치되어 있는 버전 (커맨드라인)



### 가상머신에 우분투 추가하기 

가상머신을 키고난후 새로 만들기 해서 우분투를 추가하면 된다. 

기본 메모리와 프로세서를 좀 높게 잡았는데 가상머신 실행하니 렉이..장난없다 

![3]({{site.url}}/images/2023-04-25-HOME-SERVER/3.PNG)



![4]({{site.url}}/images/2023-04-25-HOME-SERVER/4.PNG)

설치 작업만 1시간 정도 걸린거 같다. 다음 포스팅에 다음 단계로 넘어가보자 

### 가상머신 화면 크기 키우기

OS종료 후 설정 -> 디스플레이 -> 그래픽 컨트롤러를 변경해준다  

기본값 : VMSVGA -> 변경 후  VBoxVGA, VBoxSVGA 둘중 골라서 선택해주면 된다. (저는 전자 선택)
