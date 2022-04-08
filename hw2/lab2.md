# 人工智慧導論 hw2報告
```
學號: F74072277
姓名: 許郁翎
系所: 資訊工程學系
```

## Dataset Class截圖
### train/valid dataset
![image](https://user-images.githubusercontent.com/61599898/162396818-210f899d-b268-4af3-8030-b7cf1fa0a237.png)
### test dataset
![image](https://user-images.githubusercontent.com/61599898/162397152-3ca4333d-cdc9-416f-a055-f91b23afe218.png)


## 實驗結果
![image](https://user-images.githubusercontent.com/61599898/162203631-37db0b12-8e92-416f-a3e0-010fc4776457.png)

### Model Class
用5層convolution layer(未加batch normalization)  
#### class 截圖:  
 --  
#### train/valid
(藍色代表train，橘色代表valid)
* loss
![loss2](https://user-images.githubusercontent.com/61599898/162409215-bd159b2e-b4cc-401b-94f9-4d5da4ab6e95.png)
* accuracy
![acc2](https://user-images.githubusercontent.com/61599898/162409165-5a340a94-2fc6-43de-8c7f-e36741ea10fa.png)
#### testing
##### output
 --
### pretrained model finetuned
在每層activation function後面，加上batch normalization  
#### class 截圖
![image](https://user-images.githubusercontent.com/61599898/162403801-ac34a515-ef0a-4e24-a103-6897ae85fe4d.png)
#### train/valid
(藍色代表train，橘色代表valid)
* loss
![image](https://user-images.githubusercontent.com/61599898/162402746-0d99abfc-8de7-4170-9dde-b61ea2b1fba1.png)
* accuracy
![image](https://user-images.githubusercontent.com/61599898/162402961-2fddfacb-6c8a-49c6-84f9-df049c1816e2.png)
#### test
##### output
F74072277_test_model.csv  

#### 使用的模型
Resnet18
#### train/valid
(藍色代表train，橘色代表valid)
* loss
![image](https://user-images.githubusercontent.com/61599898/162406938-941c3779-9aae-4607-8fec-a550b31014b4.png)
* accuracy
![image](https://user-images.githubusercontent.com/61599898/162406988-14e5a756-bbff-495c-9afd-4046976359c5.png)
#### testing
##### output
F74072277_test_pretrain.csv  

## 結果與討論

### 模型比較

### 實作中遇到的困難與克服
#### cuda out of memory
解決方法: 1. 把batch size設小 2. 把image resize小一點(實驗是1000x1000 -> 300x300)  
#### CUDA error: device-side assert triggered resnet
網路上查到都是classification label的問題，但我的情況感覺不是...  
(到現在還未找到bug，不知道是不是不同筆記本切換GPU時出的問題..)  


