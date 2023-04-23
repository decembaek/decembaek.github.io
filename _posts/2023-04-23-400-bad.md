---
layout: single
title: "명령어 자동완성 및 추천기능, 개발자 필수툴"
categories: [It, Tool]
tag: [zsh, terminal, tool]
toc: true
---

# zsh Auto-suggestions

쉘 명령어를 자주 사용하는 개발자라면 정말 좋은 기능이다.

GitHub : https://github.com/zsh-users/zsh-autosuggestions



## zsh auto suggestions 이란

내가 자주 쓰는 명령어 기록을 기반으로 명령을 제안해주는 기능을 가지고 있다. 

![zsh]({{site.url}}/images/2023-04-23-Auto-suggestion/zsh.png)

py만 입력했는데 개발 서버를 킬때 쓰는 명령어를 자동으로 추천해준다. 방향키 오른쪽키를 누르면 자동으로 명령어를 작성해준다.



## zsh-autosuggestions 플러그인 사용법

### 제안 하이라이트 스타일 구성

제안이 표시되는 스타일을 구성하려면 `ZSH_AUTOSUGGEST_HIGHLIGHT_STYLE` 설정하세요. 256색 팔레트에서 전경색을 8색으로 설정하는 기본은 `fg=8`. 터미널이 8가지 색상만 지원하는 경우, 0에서 7 사이의 숫자를 사용해야 합니다.

```bash
ZSH_AUTOSUGGEST_HIGHLIGHT_STYLE="fg=#ff00ff,bg=cyan,bold,underline"
```

### 제안 전략

`ZSH_AUTOSUGGEST_STRATEGY`는 사용자가 원하는 자동완성을 요청할 수 있다. ㅎㅎ 다음과 같이 3가지가 있다.

- `history`: 가장 최근에 쓰는 명령어 추천 ex) python manage.py runserver, python manage.py migrate 과 같이 같은 명령어로 시작하는 경우 최근에 쓴 명령어를 추천해준다!
- `completion`: 완성된 명령어를 추천 받을 수 있습니다. (zpty 모듈 필요)
- `match_prev_cmd`: history 중 가장 최근 실행된 명령과 일치하는 항목 중 가장 최근 것을 선택합니다.  이 전략은 HIST_IGNORE_ALL_DUPS 또는 HIST_EXPIRE_DUPS_FIRST와 같은 ZSH 옵션과 함께 사용할 경우 예상대로 작동하지 않을 수 있습니다.

예를 들어, `ZSH_AUTOSUGGEST_STRATEGY=(history completion)`를 설정하면 먼저 기록에서 제안을 찾으려고 시도하지만, 일치하는 것을 찾을 수 없으면 완료 엔진에서 제안을 찾을 수 있다 



| 필자는 history를 추천한다 (기본값)



## autosuggestions 설치 방법 (Oh My Zsh)

Terminal 및 Item, cmd 명령 프롬포트에서 편집할때 파일 경로 앞에 vi 을 입력하면 편집기가 실행됩니다.

1. i 입력 -> insert 모드
2. 파일 수정 후 esc로 insert모드 나오기
3. :wq! 입력해서 저장하고 나오기 (!를 붙이면 강제 저장)



### $ZSH_CUSTOM/plugins 디렉토리에 저장소 복제

우선, 아래 명령어를 실행하여 zsh-autosuggestions 저장소를 클론합니다. 이때 저장소는 기본적으로 $ZSH_CUSTOM/plugins 디렉토리에 저장됩니다.

```bash
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```

### 플러그인 로드 리스트에 추가

그리고 나서, 플러그인을 Oh My Zsh에서 로드할 수 있도록 로드 리스트에 추가합니다. 이때 Oh My Zsh의 설정 파일인 ~/.zshrc 파일에서 플러그인 리스트를 찾아 plugins 항목 아래에 zsh-autosuggestions를 추가합니다.

```makefile
plugins=(
  # 다른 플러그인...
  zsh-autosuggestions
)
```

### 터미널 세션 재시작

마지막으로 플러그인을 추가하고 설정 파일을 저장한 후, 새 터미널 세션을 시작하거나 현재 터미널 세션에서 아래 명령어를 실행하여 플러그인을 로드합니다.

```bash
source ~/.zshrc
```

이제, zsh-autosuggestions 플러그인이 설치되어, 명령어를 입력할 때 적절한 자동 완성 제안이 표시됩니다.
