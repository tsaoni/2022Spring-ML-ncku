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
在每層activation function後面，加上batch normalization  
#### class 截圖
![image](https://user-images.githubusercontent.com/61599898/162403801-ac34a515-ef0a-4e24-a103-6897ae85fe4d.png)
#### train/valid
(藍色代表train，橘色代表valid)
* loss
![image](https://user-images.githubusercontent.com/61599898/162450863-d16d48bc-83ad-47cc-817b-e938ecc3ea3e.png)
* accuracy
![image](https://user-images.githubusercontent.com/61599898/162450891-71d2eec1-2e94-45b2-9ae9-fac8aeab6186.png)
#### test
##### output
F74072277_test_model.csv  

### pretrained model finetuned
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
pretrained model一train就accuracy 8X起跳太厲害啦
model class手寫板本的，epoch = 10時都還停留在4X...
### 模型比較
有加batch normalization真的有比沒加accuracy高
### 實作中遇到的困難與克服
#### cuda out of memory
解決方法: 1. 把batch size設小 2. 把image resize小一點(實驗是1000x1000 -> 300x300)  
#### CUDA error: device-side assert triggered resnet
網路上查到都是classification label的問題，但我的情況感覺不是...  
(到現在還未找到bug，不知道是不是不同筆記本切換GPU時出的問題..)  
#### training time out of deadline(X)
嗚嗚修課太多沒幾天可以finetune model...
希望可以再多試試dropout(data argumentation)，調整optimizer
調高epoch數應該可以在讓accuracy升高
