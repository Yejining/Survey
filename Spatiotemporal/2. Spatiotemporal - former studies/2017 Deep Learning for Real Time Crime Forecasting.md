# 2017 Deep Learning for Real Time Crime Forecasting

로스 앤젤레스 부근의 범죄 분포 예측

1. raw crime point data를 같은 시간대에 일어난 범죄들을 한 번에 합해 image-like crime heat map으로 변환

   <img src="images/crime distributions.png" alt="crime distribution" width="500">

2. hierarchical structures of residual convolutional units에 적용

   <img src="images/structure of the deep neural network models.png" alt="structure of the deep neural network models" width="500">

여기에 쓰인 DNN은 [2017 Deep Spatio-Temporal Residual Networks for Citywide Crowd Flows Prediction](2017%20Deep%20Spatio-Temporal%20Residual%20Networks%20for%20Citywide%20Crowd%20Flows%20Prediction.md)에서 가져온 것이다. [github](https://github.com/snehasinghania/STResNet)



### COVID19 dataset에 적용

대한민국 위/경도 범위 [33.065052, 38.755133] X [125.701933, 129.876737]

##### Data preprocessing

temporal dimension: 논문에서는 24시간 주기로 범죄율 그래프를 뽑을 때 특징이 있었지만, 코로나 데이터에서는 매일 같은 시간대에 하루동안 발생한 확진자 수를 발표했기 때문에 시간별 그래프를 그리기 어려움.





