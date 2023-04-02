---
layout: single
title: "파이썬 장고로 폼 제출시 취약점 없애기 Python Django / csrf_token"
categories: [Python, Django]
tag: [python, django, Form, security]
toc: true
---

 "CSRF verification failed" error 해결 방법

# Django Form 제출시 생기는 보안 취약점

## Django Form 으로 제출할 때 생기는 보안 취약점

![csrf]({{ site.url }}/images/2023-04-02-Django-csrf/csrf.png)

Csrf_token은 폼 제출시 아래에 명시해야한다

웹 사이트가 사용자의 브라우저를 확인할 수 없다면, 악의적인 사용자가 웹 사이트에서 발생하는  **데이터 변조**를 막을 수 없습니다. 

CSRF 공격을 방어하기 위에 위 같은 코드를 사용합니다.

**Django에서는 csrf_token 이 없다면  "CSRF verification failed" 와 같은 에러를 발생시킵니다.** 

---

결론 :
{% csrf_token %}은 Django에서 Cross-Site Request Forgery(CSRF) 공격을 방어하기 위해 사용하는 기능 중 하나입니다. 이 기능은 사용자가 웹사이트에서 폼을 제출할 때 웹사이트가 사용자의 브라우저를 식별할 수 있도록 해줍니다.

따라서, 보안 상의 이유로 {% csrf_token %}은 반드시 사용해야 합니다. 만약 {% csrf_token %}이 없다면, 웹사이트는 보안 취약점을 가지게 됩니다.
