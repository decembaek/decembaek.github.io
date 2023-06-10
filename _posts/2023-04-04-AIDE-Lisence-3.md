---
layout: single
title: "인공지능 방법론 : AIDE 데이터 전문가 2급 자격증"
categories: [Data, Ai, AIDE 데이터 전문가 2급 자격증]
tag: [python, ai, data, labeling]
toc: true
---



# 인공지능 알고리즘

---

## 딥러닝의 표현방식

> 딥러닝 Deep Learning
>
> **여러 층을 가진 인공신경망(ANN)**을 사용하여 머신러닝 학습을 수행

딥러닝 영어로는 Deep Learning (DL)이라고 한다.

기계가 **자동**으로 대규모 데이터에서 **패턴**과 **규칙**을 학습한다.

학습을 기반으로 의사결정이나 **예측**등을 수행하는 기술이다.



## 딥러닝의 동작원리

딥러닝을 위해선 많은 양의 학습데이터와 학습이 필요하다.

> 딥러닝의 성능은 학습데이터의 **품질**과 영향이 크다.

<h3>학습 데이터 </h3>

인공지능이 학습을 위해서는 많은 양의 데이터가 필요하며 데이터를 **전처리**(가공, 라벨링)하여 제공해 주어야 한다. 

딥러닝의 학습을 위한 데이터는 훈련데이터 train 그리고 평가데이터 test로 나누어 진다.

- 훈련데이터 train : 학습용 데이터
- 평가데이터 test : 학습평가용 데이터, 학습 후 정확도를 알아내기 위해 사용

보통 훈련 : 평가 를 7::3, 8:2로 나눈다.

10만개면 80,000 : 20,000



### epochs 에포크

학습 반복수를 뜻한다. 데이터가 10개 있다면 이 10개를 몇번 반복해서 학습하는지 정할 수 있다. 

훈련(fit) - 에포크(epochs)를 통해 손실 loss을 줄이고 정확도 (accuracy)를 올린다.

---

## 인공지능 프로그램 개발 단계별 

1. 라이브러리 가져오기(읽기)
2. 데이터 전처리(가공)하기
3. 신경망 만들기
4. 모델 만들기(학습)
5. 모델 적용하기(예측)

사실상 본격적인 개발은 3번 부터 5번까지이다.

개발을 위해 데이터 전처리 과정이 매우 중요하다

---

## 인공지능 객체검출 방법 (single object)

싱글 오브젝트 single object - 분류 Classification + 영역표시(Localization)

검출하고자 하는 객체가 하나인 경우는 싱글오브젝트로 처리한다.

> Localizaition 영역 표시
>
> 분류를 통해 검출한 객체의 정보가 있는 위치를 Box형태로 지정하는 것을 영역 표시라고 한다.

> Bounding Box 바운딩박스
>
> 학습을 통해 검출한 객체의 영역을 사각형으로 표시한다. 



---

## 인공지능 객체검출 방법 (multi object)

검출하고자 하는 객체가 여러 개인 경우 사용하는 방법 중 객체검출(Object Detection)이있다.

> 객체검출 **Object Detection**
>
> 학습을 통해 여러 개의 객체를 인식하고 인식된 객체를 각각 바운딩박스와 색을 이용하여 영역을 표시한다.

> 의미적 분할 **Instance Segmentation** 
>
> 객체인식에서 이미지 내의 의미 있는 단위로 분할 하는 작업을 말한다.
>
> 정교하고 복잡한 인공지능 구현을 위하여 이미지의 영역별 의미를 부여하는 경우 사용한다.

---

## 핵심 딥러닝 알고리즘 신경망 이해

<h2>CNN(합성곱신경망) Convolutional Neural Network</h2>

- 영상처리에 많이 활용되는 합성곱
- 인공신경망 합성공을 이용해 가중치 수를 줄여 이미지 처리에 효과적이다.
- 이미지의 특장점을 효과적으로 찾을 수 있는 신경망
- 데이터의 특징을 **분석**하여 **패턴**을 파악하는 구조

<h2>RNN(순환신경망) Recurrent Neural Network</h2>

- 음성처리에 많이 사용한다.
- 계층 출력이 순환구조로 되어있다.(은닉계층의 결과가 다음 계층으로 넘어가며, 자기 계층으로 다시 돌아온다.)
- 시계열 정보처리
- 음성, 웨이브폼, 텍스트의 앞뒤를 분석하는 등 언어처리에 사용

<h2>GAN(생성적 적대 신경망)</h2>

- 이미지 생성
- 이미지 복원
- 신경망끼리 경쟁을 시켜 학습한다.(신경망끼리 경쟁하여 최적화를 수행)
- 하나는 생성망, 하나는 판별망
- 이미지 생성, 복원, 흉내, 신약개발, 음성생성, 편집 변환, 복원 등 활용







---

-AIDE 2급 자격증 과정-


