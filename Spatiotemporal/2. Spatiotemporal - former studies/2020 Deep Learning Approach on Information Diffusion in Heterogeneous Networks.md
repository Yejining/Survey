# 2020 Deep Learning Approach on Information Diffusion in Heterogeneous Networks

```
CNN-LSTM을 이용해 heterogeneous network에서 diffusion precess 예측
spatial dependency가 없기 때문에 spatiotemporal dataset은 아님
```

지금 보고 있는 covid19 dataset에서 확진자 수가 시공간의 영향을 받고 그 수가 확산되기 때문에 diffusion을 다룬 논문을 보면 도움이 될 것이라 생각했다. 이 논문에서는 논문이 발표된 후 다른 저자가 해당 논문을 인용하는 것을 확산의 형태라 보고 t 시간대에 논문이 어떻게 인용될 지 예측하는 방법론을 소개했다.

저자들끼리 어떻게 영향을 받았는지 각각의 meta-paths로 나눠 분석하고 그 결과값을 다시 합한 다음 딥러닝에 넣어서 예측하는 방법론에서는 spatial dependency가 없는 데이터를 사용했지만, 이 방법론을 spatiotemporal dataset을 딥러닝이나 AutoML에 적용할 수도 있을 것 같다는 생각이 들었다.

DBLP와 Citeseer dataset을 다운받아 어떻게 코드에 적용했는지 보려고 했는데, 다운받는 시간이 걸려서 나중에 봐야겠다.



```
딥러닝을 이용해 dataset에서 featrues를 뽑아내고, 뽑아낸 features로 네트워크 내에서 확산 과정을 예측
The well-known deep learning architectures are employed on our generated features to predict diffusion processes in the network
```

![CNN-LSTM Architecture](images/cnn-lstm%20architecture.PNG)



```
Our motivation is to employ a deep learning approach on information diffusion tasks such as topic diffusion and cascade prediction to alleviate the problems of the earlier ones.
```

![the overall flowchart of the proposed method](images/the%20overall%20flowchart%20of%20the%20proposed%20method.PNG)



```
A novel latent representational learning approach on heterogeneous networks based on different types of meta-paths
```

```
We have applied CNN-LSTM to generate meta-paths representation for information diffusion tasks. The CNN-LSTM architecture contains a CNN layer for feature extraction along with an LSTM to support sequential prediction. This model draws on the intuition that the sequence of features extracted from CNN can be encoded into a vector representation using LSTM architecture.
```

![the procedure of a tensor input creation in a time-stamp](images/the%20procedure%20of%20a%20tensor%20input%20creation%20in%20a%20time-stamp%20t.PNG)



#### 데이터셋

- DBLP
  - computer science bibliography among authors in main conferences and publications
- Citeseer
  - CiteSeer digital library에서 발췌한 데이터셋



#### Training and Testing

- training set
  - t-4부터 t-1 시간대까지 topic diffusion과 cascade prediction을 각각 학습
- test set
  - t-1 시간부터 t시간까지 topic diffusion을 테스트하는 데 사용. t-1 시간대의 데이터는 seed nodes로 사용되었다.