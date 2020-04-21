# 2017 Deep Spatio-Temporal Residual Networks for Citywide Crowd Flows Prediction

- [github](https://github.com/snehasinghania/STResNet)
  - github에서 코드가 완전히 구현되어있지 않았다. 논문을 읽어보니 grid mapping으로 데이터를 전처리한 것 같았다.
- 참조 논문
  - [2016 DNN-Based Prediction Model for Spatial-Temporal Data](2016%20DNN-Based%20Prediction%20Model%20for%20Spatial-Temporal%20Data.md)



- ST-ResNet 목적
  - collectively forecast the inflow and outflow of crowds in each and every region of a city
- residual neural network framework 사용
- it learns to dynamically aggregate the output of the three residual neural networks
  - Spatial dependencies
  - Temporal dependencies
  - External influence
    - The aggregation if further combined with external factors



