# 2019 Deep Leaning for Spatio-Temporal Data Mining: A Survey

이 논문에서는 Spatio-Temporal dataset을 이용한 딥러닝 논문들을 소개하고 있다. ST data에는 어떤 종류가 있는지, 그 종류에 따라서 데이터가 어떻게 표현될 수 있는지, 표현된 데이터에 따라 어떤 딥러닝 모델을 선택할 수 있는지, 어떤 주제를 가진 프로젝트들이 어떤 딥러닝 모델을 썼는지에 대해 얘기한다.



### Predictive Learning

point

- [145] [2017 Deep Learning for Real Time Crime Forecasting](2017%20Deep%20Learning%20for%20Real%20Time%20Crime%20Forecasting.md)
  - 동시간대에 발생한 raw crime data를 한데 모아 이미지처럼 데이터를 만들고 예측한다는 점과 cnn을 사용해 예측한다는 점이 신기했음
  - 여기에 쓰인 DNN은 [2017 Deep Spatio-Temporal Residual Networks for Citywide Crowd Flows Prediction](2017%20Deep%20Spatio-Temporal%20Residual%20Networks%20for%20Citywide%20Crowd%20Flows%20Prediction.md)에 기초한다.
- [57] [DeepCrime: Attentive Hierarchical Recurrent Networks for Crime Prediction](2018%20DeepCrime%20Attentive%20Hierarchical%20Recurrent%20Networks%20for%20Crime%20Prediction.md)
  - 범죄 예측을 위해 GRU 사용
  - dataset으로는 범죄 현황 데이터와 POI 데이터 이용, [datapreprocessing.py]([https://github.com/Prabhat1808/CrimePrediction/blob/master/Python%20code/datapreprocessing.py](https://github.com/Prabhat1808/CrimePrediction/blob/master/Python code/datapreprocessing.py))로 데이터 전처리 코드 있음
- [201] [Hetero-ConvLSTM: A Deep Learning Approach to Traffic Accident Prediction on Heterogeneous Spatio-Temporal Data](2018%20Hetero-ConvLSTM%20A%20Deep%20Learning%20Approach%20to%20Traffic%20Accident%20Prediction%20on%20Heterogeneous%20Spatio-Temporal%20Data.md)
  - ConvLSTM 사용해 교통 사고 예측
  - first merged the point data of traffic accidents and modeled the traffic accident count ini a spatio-temporal field as a 3-D tensor



time series

- [126] Combining time-series and textual data for taxi demand prediction in event areas: a deep learning approach
  - historical time series에서 feature를 뽑아 다른 문맥적 feature와 합한다는 점에서 재미있게 보였는데, 그 문맥적 feature가 말 그대로 'texture'에서 오는 거여서 이번 연구와 맞지 않다고 생각함



spatial maps

- [184] [Dnn-based prediction model for spatio-temporal data](2016%20DNN-Based%20Prediction%20Model%20for%20Spatial-Temporal%20Data.md)
  - 까마귀의 이동이 spatial maps로 표현돼 input으로 들어가고, 이동을 예측한다는 점에서 이번 연구와 관련이 있을 것 같다는 생각이 들었음
- [69] Hexagon-Based Convolutional Neural Network for Supply-Demand Forecasting of Ride-Sourcing Services
  - 도시를 육각형 단위로 쪼개 인접한 노드의 수가 사각형일 때보다 훨신 많아지도록 함
  - 공유 자전거에 대한 수요와 공급을 예측하는 것이 이 프로젝트의 목적
  - 주제는 covid19과 관련이 없지만 육각형으로 지형을 나눈 점이 재미있어 보였음



graph

- [8] bike flow prediction with multi-graph convolutional networks
- [85] DIFFUSION CONVOLUTIONAL RECURRENT NEURAL NETWORK: DATA-DRIVEN TRAFFIC FORECASTING
  - traffic flow를 diffusion의 형태로 보고, 이를 그래프로 표현했다는 점에서 covid19와 결이 같다고 느꼈음
  - spatial dependency와 temporal dependency를 각각 다른 방법으로 빼내는데, automl에서 이 작업을 할 수 있을지 잘 모르겠음
- [155] Efficient metropolitan traffic prediction based on graph recurrent neural network
  - road network를 model하고 교통 흐름에서 전파 패턴을 표현하는 프로젝트 (model the road networks and presented the propagation patterns of traffic flow)
  - 그래프에서 전파 패턴 학습



trajectories

- [67 61-72] A convolutional neural network approach for modeling semantic trajectories and predicting future locations
  - 각각의 장소가 home, work, shopping 등으로 나뉨
  - 의미있는 trajectories를 뽑아내고, 미래에 사람이 어느 곳에 있을지 예측
  - cnn에는 matrix가 input으로 입력된다.
- [103] T-CONV: A Convolutional Neural Network For Multi-scale Taxi Trajectory Prediction
  - trajactories를 이차원 이미지로 만든 다음 multi-layer cnn이 multi-scale trajectory patterns를 합해 택시 경로에서부터 목적지 예측



ST raster

matrix이거나 tensor 형태로 데이터가 표현될 수 있음

- ST raster data가 spatial map과 다른 점
  - ST ratster는 여러개의 시간대에서 측정된 ST 정보의 합이라면,
  - spatial map은 한 시점에서만 측정된 ST 정보

- [12] Exploiting spatio-temporal correlations with multiple 3d convolutional neural networks for citywide vehicle flow prediction
  - 길에서의 교통 속도를 측정한 프로젝트가 아니라 도시에서 한 구역씩 자동차 이동 예측
- [131] Stepdeep: A novel spatio-temporal mobility event prediction framework based on deep neural network
  - 3d tensor 형태로 다른 시간대의 도시 보행자의 움직임 모델링함



### APPLICATIONS

종류가 너무 많고, 이미 위에 제시된 논문이 많아서 저 논문들부터 봐도 괜찮을거라 생각해 넘김



### OPEN PROBLEMS

deep learning model selection 부분 정리해놓을 것