# 2022.03.12 hw1

## Build Model 的截圖
![image](https://user-images.githubusercontent.com/61599898/157932156-b30e3212-d963-4a57-a7f3-160b33fc1c14.png)

## 完成實驗表格
### epoch = 2
Loss
![image](https://user-images.githubusercontent.com/61599898/157932457-aa027d6d-4a89-497a-8d50-a3046a3cceb6.png)
Accuracy
![image](https://user-images.githubusercontent.com/61599898/157932616-533ebf09-480b-4381-86db-730c4aca8d6e.png)
### epoch = 4
Loss
![image](https://user-images.githubusercontent.com/61599898/157932785-0d3625d2-1582-409e-90c6-3da379f8b450.png)
Accuracy
![image](https://user-images.githubusercontent.com/61599898/157932840-03265e2c-df0b-40d4-bd32-1b474c724b2e.png)
### epoch = 8
Loss
![image](https://user-images.githubusercontent.com/61599898/157932905-b86b3c88-ad5f-4606-a723-91fb5c185546.png)
Accuracy
![image](https://user-images.githubusercontent.com/61599898/157932996-c66248d3-56e7-4229-9efb-01c452546c28.png)
### epoch = 16
Loss
![image](https://user-images.githubusercontent.com/61599898/157934288-7e54a877-8347-4626-afa1-836fc0069b87.png)
Accuracy
![image](https://user-images.githubusercontent.com/61599898/157934374-ff6251da-9720-4388-bff7-61d4a6d6f82c.png)

## 心得及討論(ex: 探討實驗結果)

### 心得
1. 通常loss越低accuracy越高。
2. 每一個row，隨著neuron數(X)增加，loss先減後增，accuracy先增後減。
3. 每一個column，隨著hidden layer數(N)增加，loss上升，accuracy下降。
4. 在X = 1024，N = 8, 16的地方，loss會大爆炸。

### 討論

1. training set跟testing set上感覺都可以分別算loss跟accuracy，但是在本次作業上助教的範本是算training set上的loss跟testing set上的accuracy，不知道這是不是大家的習慣?
2. MLP的模型好像越deep越train不起來?
3. 不知道如果加上activation function後，可否解決loss大爆炸的問題?
