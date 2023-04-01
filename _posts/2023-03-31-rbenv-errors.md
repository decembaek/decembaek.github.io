---
layout: single
title: "rbenv 오류 해결: rbenv: version `3.0.6' is not installed"
categories: [Error]
tag: [it, coding, error, ruby, rbenv]
toc: true
---


rbenv: version `3.0.6' is not installed (set by /Users/UserName/.ruby-version)
이 오류는 현재 사용 중인 rbenv 버전이 3.0.6이 아니기 때문에 발생합니다.
이 문제를 해결하려면 rbenv 설치를 해야합니다.

## rbenv: version `3.0.6' is not installed 해결 방법
### 1. rbenv 설치 버전 확인

터미널에서 다음 명령어를 입력하여 현재 설치된 rbenv 버전을 확인하세요.

```
rbenv version
```

설치된 rbenv 버전이 3.0.6 이 아닌 경우 다음 명령어를 사용하여 3.0.6 버전을 설치하세요.

```
rbenv install 3.0.6
```

### 2. ruby-version 파일 확인

이 오류는 .ruby-version 파일에서 지정된 rbenv 버전과 일치하지 않는 rbenv 버전을 사용하려고 시도할 때 발생합니다. 따라서 프로젝트 루트 디렉토리에서 .ruby-version 파일을 열어 현재 지정된 rbenv 버전을 확인하세요.

```
cat .ruby-version
```

이 명령은 현재 프로젝트에서 사용되는 Ruby 버전을 출력합니다. rbenv가 3.0.6으로 설정되어 있는지 확인하세요. 그렇지 않은 경우 다음 명령어를 사용하여 버전을 업데이트하세요.

```
echo "3.0.6" > .ruby-version
```

### 3. rbenv global 버전 업데이트

터미널에서 다음 명령어를 입력하여 rbenv 전역 버전을 3.0.6으로 업데이트하세요.

```
rbenv global 3.0.6
```

이 명령은 rbenv 버전을 3.0.6으로 설정합니다. 이제 프로젝트에서 rbenv 3.0.6 버전을 사용해야 합니다.

이렇게 하면 rbenv: version `3.0.6' is not installed (set by /Users/localname/.ruby-version) 오류가 해결됩니다.


