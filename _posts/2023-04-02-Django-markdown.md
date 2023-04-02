---
layout: single
title: "파이썬 장고로 마크다운 사용하기 Python Django /pip install markdown"
categories: [Python, Django]
tag: [python, django, pip, install]
toc: true
---

# Django에 Markdown 마크다운 설치

## markdown 설치하기 install markdown

terminal 에서 실행

```
pip install markdown
```

## markdown 마크 다운 필터 등록하기

> 마크다운으로 작성한 문서를 HTML문서로 변환할려면 다음과 같은 markDown 함수를 추가하자

```python
import markdown
from django.utils.safestring import mark_safe

# template
from django import template

@register.filter() #filter함수로 설명은 블로그에 올려두겠다
def markDown(value):
		extensions = ['nl2br', 'fenced_code']
		return mark_safe(markdown.markdown(value, extensions=extensions))
```

mark 함수는 markdown module 과 mark_safe 함수를 사용해서 HTML 코드로 변환하여 return 한다

### markdown module

1. Nl2br 은 줄바꿈 문자를 `<br>` 태그로 바꿔 주므로 Enter를 한 번만 눌러도 줄바꿈으로 인식한다.
2. fenced_code 는 마크다운의 소스 코드 표현을 위해 사용된다.

### markdown 모듈 템플릿에 적용하기

templates/template.html 자신 템플릿에 들어갑니다

![스크린샷 2023-04-02 오후 5.11.54]({{site.url}}/images/2023-04-02-Django-markdown/스크린샷 2023-04-02 오후 5.11.54.png)

이렇게 사용하면 마크다운을 가져올 수 있습니다.
