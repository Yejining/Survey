# AUTOML: METHODS, SYSTEMS, CHALLENGES (NEW BOOK)

이 글은 위의 책을 읽으면서 중요하다고 생각한 점을 번역해놓은 것이다.



### Contents

1. [Part I AutoML Methods](#Part-I-AutoML-Methods)
   1. [Hyperparameter Optimization](#1.-Hyperparameter-Optimization)
   2. Meta-Learning
   3. Neural Architecture Search
      1. Model-Free Blackbox Optimization Methods
      2. [Bayesian Optimization](#1.3.2-Bayesian-Optimization)
         1. [Bayesian Optimization in a Nutshell](#Bayesian-Optimization-in-a-Nutshell)
         2. [Surrogate Models](#Surrogate-Models)
         3. [Configuration Space Description](#Configuration-Space-Description)
         4. [Constrained Bayesian Optimization](#Constrained-Bayesian-Optimization)
2. Part II AutoML Systems
   1. Auto-WEKA: Automatic Model Selection and Hyperparameter
   2. Hyperopt-Sklearn
   3. Auto-sklearn: Efficient and Robust Automated Machine Learning
   4. Towards Automatically-Tuned Deep Neural Networks
   5. TPOT: A Tree-Based Pipeline Optimization Tool for AutomatingMachine Learning
   6. The Automatic Statistician
3. Part III AutoML Challenges
   1. Analysis of the AutoML Challenge Series 2015–2018



## Part I AutoML Methods

### 1.  Hyperparameter Optimization

#### 1.1 Introduction

Hyperparameter Optimization의 장점으로는 머신 러닝 알고리즘의 성능을 향상시킨다는 점과, 과학적 연구의 재사용성, fairness를 높인다는 점이 있다.

HPO는 특정 애플리케이션 도메인에 일반적인 기능을 하는 파이프라인을 적용시키는 데 사용될 수 있다. 요즘, 조정된 하이퍼파라미터가 일반적인 기계학습 라이브러리에서 기본적으로 세팅된 값보다 훨씬 더 좋은 성능을 내고 있는 것은 이미 자명한 사실이다.

HPO에는 다음과 같은 문제가 있다.

- Function evaluation이 비쌀 수 있다.
- Configuration space가 복잡하거나 고차원인 경우. 게다가 이런 경우에는 이 알고리즘의 어떤 하이퍼파라미터가 최적화 되어야하는지, 어느 범위에서 최적화 되어야하는지 정확하게 알 수 없다.
- 대부분이 gradient of the loss function에 대한 접근 권한이 없다.
- Training dataset이 limited size이기 때문에 일반적인 성능을 내도록 바로 최적화할 수 없다.



#### 1.2 Problem Statement

$$
\lambda^* = \underset{\lambda \in \Lambda}{\operatorname{argmin}}\mathbb{E}(D~train,D~valid)~ 수식 미완성. 찾기 귀찮아서 못 쓰겠다.
$$

#### 1.3 Blackbox Hyperparameter Optimization



#### 1.3.2 Bayesian Optimization

이번 장에서는 Bayesian optimization에 대한 간단히 소개하고, alternative surrogate models를 선보일 것이다. conditional and constrained configuration spaces에 대해 알아봄과 함께, hyperparameter optimization에서 중요한 몇가지 application에 대해서도 의논할 것이다.

최근 Bayesian optimization에 대한 연구들은 HPO를 blackbox로 보지 않는다. 게다가, 많은 Bayesian optimization연구들이 HPO를 직접적으로 타겟팅하지 않고, HPO에 적용하는 식으로 연구한다.

##### Bayesian Optimization in a Nutshell

Bayesin Optimization은 두 개의 키로 이루어진 반복 알고리즘이다. 하나는 probabilistic surrogate model이고, 다른 하나는 acquisition function으로, 이 둘은 다음에 평가할 지점(point)를 결정하는 역할을 가지고 있다.

각각의 반복마다, surrogate model은 target function이 파악된만큼 맞춰진다. 그러면 확률적 모델의 예측 분포를 사용하는 acquisition function이 다른 후보 포인트들을 결정한다.

blackbox function을 평가하는 것과는 달리, acquisition function은 계산량이 작고, 완전히 최적화할 수 있다.

<img src="images/acquisition function.png" alt="acquisition function" widht="500">

<img src="images/illustration of bayesian optimization.png" alt="illustration of bayesian optimization" width="700">

 ##### Surrogate Models

한 번 읽어봤는데, 도저히 무슨말인지 모르겠어서 좀 더 찾아봐야 할 것 같다.

##### Configuration Space Description

##### Constrained Bayesian Optimization



