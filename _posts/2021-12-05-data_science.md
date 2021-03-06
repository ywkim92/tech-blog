---
layout: single
title:  "데이터 사이언스 하면서 느낀 점(1)"
excerpt: "주니어 데이터 사이언티스트의 넋두리"

categories:
  - machine_learning
tags:
  - [machine_learning, AI,  data_science, data_scientist]
header:
  teaser: https://user-images.githubusercontent.com/66911578/144751709-07aec712-63ad-44d5-a617-75318bc3246c.jpg
toc: true
toc_sticky: true
use_math: true
date: 2021-12-05
last_modified_at: 2021-12-06
---
# 들어가며
파이썬을 배우고 scikit-learn, tensorflow를 써보며 인공지능, 데이터 사이언스에 입문한 지 어언 2년이 되었습니다. 독학, 교육, 스타트업 근무 등 다양한 환경에서 여러 프로젝트를 진행하며 느낀 게 제법 있습니다. 비록 길지 않은 경력이지만 중요한 고비마다 부족했던 부분을 되돌아보며 
전문가로 성장하기 위해 유념해야 할 점을 적어두었습니다. 포스트에 공유하며 생각을 정리하고 날카롭게 다듬고자 합니다.
<br>

<br />
# 전가의 보도는 없다
'전가의 보도(傳家의 寶刀)'란 말이 있습니다. '집안 대대로 전해 내려오는 명검'을 뜻하는데 의미가 변형되어 (상황이 궁할 때) 상투적으로 꺼내 쓰는 논리 등의 의미로 쓰입니다. 처음 인공지능을 접했을 때는 scikit-learn으로 대변되는 전통적인 머신러닝, 통계 기반 모델을 구시대의 유물로 
여겼습니다. 발전된, 최신 기술을 쓰면 대부분의 문제를 수월하게 해결할 수 있다고 믿었습니다. 비단 모델뿐만 아니라 scaling, encoding, oversampling, imputing 등 전처리 기법도 특정 방식이 최선이고 그 방식만 기계적으로 적용하면 될 줄 알았습니다.

그러나 이내 모든 상황에서 최적해를 도출하는 단 하나의 알고리즘은 없다는 것을 깨달았습니다. 상황에 맞게 데이터에 적합한 모델과 기법을 사용하는 안목이 필수적임을 체감하고 있습니다. 예를 들어 SMOTE 기법이 소수 클래스 더미 데이터를 생성하는 알고리즘을 알고 있다면, 데이터가 불균형하다 할 때 오버샘플링을 
쓰면 무조건 metric이 향상될 거라는 기대는 어불성설입니다. 적절한 전처리, 파생변수 생성, 변수 선택 등이 가미되면 logistic regression으로도 괜찮은 지표를 얻기도 합니다. 

대표적인 예시로 비틀즈 곡의 원작자를 예측하는 
[하버드 대학 연구](https://hdsr.mitpress.mit.edu/pub/xcq8a1v1/release/6)가 있습니다. 저자들은 여러 음악적 특성을 [features](https://hdsr.mitpress.mit.edu/pub/xcq8a1v1/release/6#ywxppmj6zp)로 
활용하여 곡을 인코딩한 후에 logistic regression으로 원작자를 판단하는 이진 분류 모델을 만들었으며 AUC 0.837이라는 결과를 얻었습니다.
<br>

<br />
# 수학이 생각보다 많이 필요하진 않다
처음 인공지능을 접했을 때 AI의 기반은 수학이며 수리적인 이해가 필수적이란 얘기를 많이 들었습니다. 일반적인 이공계 대학생 기준으로도 학부 때 수학을 많이 공부한 편이라고 자부했기에 이를 일종의 '보험'이라 여기며 데이터 사이언스에 도전했습니다. 하지만 막상 공부하면서 수학 때문에 덕을 봤다거나 발목 잡혔던 
경험은 없습니다.

학부에서 배웠던 수학의 키워드는 시공간, 행렬과 벡터, 복소수, 미분방정식 등이었습니다. 제가 AI에 과문한 탓이겠으나 행렬, 확률과 통계에 대한 기초 지식이 있다면 입문 시 수학으로 인한 진입 장벽은 없는 듯합니다. 아시다시피 이 내용들은 고등학교 수학 Ⅰ(7차 교육과정 기준)에서 다룹니다. 보이저엑스의 남세동 
대표님께서도 비슷한 논조로 말씀하고 계십니다. [페이스북 포스트](https://www.facebook.com/dgtgrade/posts/4630769066981923)에서 확인하실 수 있습니다.
<br>

<br />
# 분석만으로는 커리어를 인정받기 어렵다
이런 저런 프로젝트를 수행해보고 평가지표를 뽑는 것까지만 해봤다면, 아무리 직장 경험이 있을지라도 채용 시장에서 큰 주목을 끌기는 어렵습니다. 1. 특정 도메인 지식이 상당하거나 그 분야에 특화된 프로젝트를 여럿 성공시켰든지 2. NLP, 이미지, 추천 시스템 등 한 가지를 잡고 커리어 패스를 밟아왔다든지 
하는 스페셜리스트가 각광 받습니다. 소위 generalist는 개인의 역량이 아주 출중하지 않은 이상 각 분야의 specialist에게 밀리는 형국입니다.

![image](https://user-images.githubusercontent.com/66911578/144797109-abe430fd-70eb-40de-8d52-47ddc05c6cf9.png)

더불어 MLOps가 대두되는 현 시점에서 데이터를 '관리'하거나 모델을 '서빙'하는 역할이 중요해졌습니다. 위 그림과 같이 [Sculley(2015)](https://proceedings.neurips.cc/paper/2015/file/86df7dcfd896fcaf2674f757a2463eba-Paper.pdf)는 머신러닝 코드를 
제외한, 주변 인프라가 매우 크고 복잡하다고 지적합니다. <sup>[1](#footnote_1)</sup> ML workflow에 대한 전반적인 이해는 물론이고 실제 프로젝트를 통해 구현해 본 경험이 높게 평가됩니다.
<br>

<br />
# 마치며
다음 시간에는 비즈니스 관점에서 느낀 점을 소개해보겠습니다.

[source of teaser](https://unsplash.com/photos/JiSkHnWLo2o?utm_source=unsplash&utm_medium=referral&utm_content=creditShareLink)

<a name="footnote_1">1</a> Sculley, D & Holt, Gary & Golovin, Daniel & Davydov, Eugene & Phillips, Todd & Ebner, Dietmar & Chaudhary, Vinay & Young, Michael & Dennison, Dan. (2015). 
Hidden Technical Debt in Machine Learning Systems. NIPS. 2494-2502. 
<br>

<br />
[Scroll to Top](#){: .btn .btn--primary .btn-small .align-center}