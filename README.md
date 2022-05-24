# DACON_Movement
![20220524_131124](https://user-images.githubusercontent.com/84311270/169981580-8a50bd36-6304-4fb1-9ded-36286400af8d.png)
3축 가속도계(accelerometer)와 3축 자이로스코프(gyroscope)를 활용해 측정된 센서 데이터에 머신러닝 알고리즘을 적용해 운동 동작 인식 알고리즘 개발

## Dataset
3축 가속도계(accelerometer)와 3축 자이로스코프(gyroscope)를 활용해 측정된 센서 데이터  
-train_features.csv (1875000, 8)  
id 별 600 time 간 동작 데이터  
id 3125개  x 600 time =1875000 데이터  
-train_labels.csv (3125, 3)  
id 별 동작과 동작 label(61개)  

-test_features.csv (469200, 8)  
id 별 600 time간 동작 데이터  
id 782개  x 600 time =469200 데이터  

-sample_submission.csv (782, 62)  
id별 동작을 예측해 작성하는 csv   

## Model
3축 가속도께와 3축 자이로스코프를 이용한 파생변수 생성과 Catboost 모델을 활용하여 학습.

## Results
Public Score : 0.64599, Private Score : 0.64801로 최종 24등으로 마무리.
![20220524_131139](https://user-images.githubusercontent.com/84311270/169981983-fe747a12-f93e-4c50-ae75-5c48c767631f.png)
