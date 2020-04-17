# AUTOML: METHODS, SYSTEMS, CHALLENGES (NEW BOOK)

이 글은 위의 책을 읽으면서 중요하다고 생각한 점을 번역해놓은 것이다.



### Contents

1. [Part I AutoML Methods](#Part I AutoML Methods)
   1. [Hyperparameter Optimization](#1. Hyperparameter Optimization)
   2. Meta-Learning
   3. Neural Architecture Search
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

### 1. Hyperparameter Optimization

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



