---
layout: single
title: "파이썬 장고로 모델 데이터베이스의 구조 만들기  Python Django / model"
categories: [Python, Django]
tag: [python, django]
toc: true
---

code 출처 : docs.djangoprogect.com

## Django model 모델 만들기

> Model 모델이란 부가적인 메타데이터를 가진 데이터베이스의 구조(layout)을 말합니다.

 여론조사 서비스를 만든다고 가정했을때 Question 과 Choice 라는 두 가지 모델을 만들 것 입니다.

```python
from django.db import models

class Question(models.Model):
  question_text = modles.CharField(max_length=200)
  pub_date = models.DateTimeField('date published')
  
class Choice(models.Model):
  question = models.ForeignKey(Question, on_delete=models.CASCADE)
  choice_test = models.CharField(max_length=200)
  votes = models.IntegerField(default=0)
```

각 모델은 여러 클래스 변수가 있으며, 각 클래스 변수는 모델에서 데이터베이스 필드를 나타냅니다.



### CharField 

CharField는 문자 필드를 표현합니다.

### DateTimeField

날짜와 시간(datetime)을 표현합니다

### ForeignKey

Choice가 하나의 Question에 관계된다는것을 알려줍니다. 

- On_delete=models.CASCADE 는 삭제시 깔끔하게 지워집니다. 

---

## 모델 활성화

앞 db 생성할때 myproject/settings.py 파일에 있는

INSTALLED_APPS 설정에 추가해야합니다.

```python
INSTALLED_APSS = [
  'appName.apps.AppnameConfig',
  #django.contrib .....생략,
]
```

