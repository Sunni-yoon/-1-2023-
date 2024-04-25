# 2023_Regional_Public_Safety_Data_Analysis_Competition

### Notice
- 제1회 2023년 지역 치안 안전 데이터 분석 공모전 코드입니다.
  
--------------------------------------------------------------------------------------
### 파일 설명

```치안데이터 코드1(전처리)_올리브통조림.ipynb``` : 전처리 <br/>
```치안데이터 코드2 (예측)_올리브통조림.ipynb``` : 예측 분석 모델 <br/>

--------------------------------------------------------------------------------------

### 분석 설명

성별, 지역, 신고 시간 등의 변수를 활용하여 보이스피싱 예측 모델을 구현함으로써 보이스피싱이 일어날 것을 미리 예측하여 피해를 방지하고자 한다.

1. 보이스피싱 사건을 알아보기 위해 사건종별코드 변수에 중심을 둠
2. 사건종별코드가 보이스피싱:215 == ‘1’ 나머지는 ‘0’으로 변경
3. 보이스피싱에 유의미한 영향을 줄 것이라고 생각되는 날짜와 지역 변수를 가진 새로운 dataframe 생성
4. 대전,세종,충남 지역의 다른 이름의 경찰서들을 ‘대전’,‘세종’,‘충남’ 으로 그룹화
5. 데이터를 train 과 test 로 나눔
6. Regression, Desicion Tree, RandomForest 작업을 수행

###  성능

| Command    | Description   | Precision| Recall  |
| ---------- | ------------- | -------  | ------- |
| 0.4117     |  0.03429      |  0.0175  |  0.7813 |


| Accuracy_score | F1_score | Precision | Recall |
| -------------- | -------- | --------- | -------|
| 0.4117         | 0.03429  | 0.0175    | 0.7813 |

- Decison Tree
- Random Foreset

In this assignment, you build a neural network classifier with MNIST dataset. For a detailed description about MNIST dataset, please refer to [this link](http://yann.lecun.com/exdb/mnist/).

- Requirements
    1. You should write your own pipeline to provide data to your model. Write your code in the template `dataset.py`. Please read the comments carefully and follow those instructions.
    2. (Report) Implement LeNet-5 and your custom MLP models in `model.py`. Some instructions are given in the file as comments. Note that your custom MLP model should have about the same number of model parameters with LeNet-5. Describe the number of model parameters of LeNet-5 and your custom MLP and how to compute them in your report.
    3. Write `main.py` to train your models, LeNet-5 and custom MLP. Here, you should monitor the training process. To do so, you need some statistics such as average loss values and accuracy at the end of each epoch.
    4. (Report) Plot above statistics, average loss value and accuracy, for training and testing. It is fine to use the test dataset as a validation dataset. Therefore, you will have four plots for each model: loss and accuracy curves for training and test datasets, respectively.
    5. (Report) Compare the predictive performances of LeNet-5 and your custom MLP. Also, make sure that the accuracy of LeNet-5 (your implementation) is similar to the known accuracy. 
    6. (Report) Employ at least more than two regularization techniques to improve LeNet-5 model. You can use whatever techniques if you think they may be helpful to improve the performance. Verify that they actually help improve the performance. Keep in mind that when you employ the data augmentation technique, it should be applied only to training data. So, the modification of provided `MNIST` class in `dataset.py` may be needed.
- **Note that the details of training configuration which are not mentioned in this document and the comments can be defined yourself.** For example, decide how many epochs you will train the model.

