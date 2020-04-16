# 2018 Diffusion Convolutional Recurrent Neural Network: Data-Driven Traffic Forecasting

spatiotemporal 데이터를 이용해서 traffic speeds를 예측한다는 점에서 dataset을 어떻게 구성했는지 보기에 좋겠다는 생각이 들어 이 논문을 읽었다.



### 특징

`Predict the future traffic speeds of a sensor network given historic traffic speeds and the underlying road networks`

이 프로젝트에서는 교통량 예측 데이터를 썼지만, 다른 spatiotemporal dataset을 input해도 된다.



[Github](https://github.com/liyaguang/DCRNN)



### DCRNN

<img src="images/system%20architecture%20of%20dcrnn.PNG" alt = "ssstem architecture of DCRNN" width="700">

- spacial dependency: bidirectional graph random walk 이용
- temporal dependency: RNN을 이용
- long-term forecasting을 위해 encoder-decoder architecture로 둘을 합함



### 데이터셋

<img src="images/sensor%20distribution%20of%20the%20datasets.PNG" alt="sensor distribution of the datasets" width="600">

- METR-LA
  - 로스앤젤레스 고속도로 교통정보
- PEMS-BAY
  - 캘리포니아 Bay area 교통정보

