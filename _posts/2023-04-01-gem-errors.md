---
layout: single
title: "ruby, gem (bundle install)설치 오류 해결"
categories: [Error]
tag: [it, coding, error, ruby, rbenv, bundle]
toc: true
---

An error occurred while installing eventmachine (1.2.7), and Bundler cannot continue. 

이 오류는 EventMachine gem 설치 중에 발생했습니다. EventMachine은 C 확장 라이브러리를 사용하므로 설치 중에 컴파일 오류가 발생할 수 있습니다.

다음 단계를 따라 문제를 해결하세요.
## An error occurred while installing eventmachine (1.2.7) 문제 해결 방법

### 1. 먼저, EventMachine이 필요로 하는 모든 종속성을 설치하세요.

   macOS에서는 다음과 같은 명령어를 사용하세요.

   ```
   brew install openssl libyaml
   ```

   Ubuntu에서는 다음과 같은 명령어를 사용하세요.

   ```
   sudo apt-get install build-essential openssl libssl-dev libyaml-dev
   ```

### 2. 이제 EventMachine gem을 다시 설치하세요.

   ```
   gem install eventmachine -v '1.2.7' -- --with-cppflags=-I/usr/local/opt/openssl/include --with-ldflags=-L/usr/local/opt/openssl/lib
   ```

   위 명령어에서 OpenSSL이 설치된 경로를 지정합니다. 만약 OpenSSL의 경로가 다른 경로라면, 위 명령어에서 `-I`와 `-L` 플래그의 경로를 수정하세요.

### 3. 위 명령어를 실행하면 EventMachine gem이 성공적으로 설치될 것입니다. 이제 Bundler를 다시 실행하여 문제를 해결하세요.

   ```
   bundle install
   ```

   이제 Bundler가 EventMachine을 제대로 설치할 수 있어서 더 이상 오류가 발생하지 않을 것입니다.