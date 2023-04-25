---
layout: single
title: "Error : 0x8007019e Linux? Windows? 에러 해결하기"
categories: [It, Server, Error]
tag: [it, linux]
toc: true
---

![error]({{site.url}}/images/2023-04-25-HOME-SERVER-error/error.PNG)

이 에러는 WSL(Windows Subsystem for Linux) 구성 요소가 아직 설치되지 않았을 때 발생하는 것으로 보입니다. WSL 구성 요소를 설치하려면 다음 단계를 따르세요:

1. 관리자 권한으로 PowerShell 또는 명령 프롬프트를 실행합니다. (시작 메뉴에서 검색하여 찾은 후 마우스 오른쪽 버튼 클릭 > '관리자 권한으로 실행')

2. PowerShell 또는 명령 프롬프트에서 다음 명령어를 입력하여 WSL 구성 요소를 설치합니다:

   ```
   wsl --install
   ```

   또는

   ```
   wsl --install -d Ubuntu-22.04
   ```

3. 설치가 완료되면 시스템을 다시 시작해야 합니다. 명령 프롬프트 또는 PowerShell에 다음 명령어를 입력하여 컴퓨터를 재부팅합니다:

   ```
   shutdown -r -t 0
   ```

4. 컴퓨터가 다시 시작된 후, 다시 PowerShell 또는 명령 프롬프트를 실행하여 `wsl` 명령어를 입력합니다. 이제 에러 없이 우분투가 실행되어야 합니다.

위 단계를 따라 WSL 구성 요소를 설치하고 시스템을 다시 시작한 후, 에러 없이 우분투를 실행할 수 있어야 합니다. 그러면 앞서 언급한 작업들을 진행할 수 있습니다.

