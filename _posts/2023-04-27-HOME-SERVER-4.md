---
layout: single
title: "ssh로 원격으로 접속하기, 서버 설치 우분투 22.04 - 4"
categories: [It, Server]
tag: [it, linux]
toc: true
---

# 집에서 서버 마련하기 ch 4

우분투 설치를 완료하였다 그러면 서버 작업의 로망인 원격 접속을 하는법을 알아보도록 하자 

우선 필요한 패키지를 설치한다 

1. net-tools : 네트워크 관련도구
2. openssh-server : 원격 접속을 위한 SSH 서버

```sql
sudo apt update
sudo apt install openssh-server
sudo apt install net-tools
```

이것들을 설치한 후 

```sql
sudo systemctl status ssh
```

를 실행해 작동 중인지 확인한다. # 실행 중이 아닐시 sudo systemctl start ssh 명령어로 서비스를 시작한다.

원격에서 접속할 계정을 만들어야 합니다. 

```
sudo adduser <user>
```

마지막에 원하는 계정 이름을 만듭니다. 비밀번호 설정 해 주면 됩니다.



방화벽 설정을 본 후 ssh가 막혀있으면 열어주어야 합니다 

```sql
sudo ufw status
sudo ufw allow ssh
```



이제 접속 가능합니다. 

```sql
ifconfig
```

다음과 같은 명령어를 쳐서 lo를 제외한 e로 시작하는곳에서 inet 192.~~~~을 가져와 줍니다.



```sql
ssh <user>@ip_address
```

그런다음 다음과 같이 만든 계정과 @뒤에 ip주소를 적어서 접속해주면 끝.. 





