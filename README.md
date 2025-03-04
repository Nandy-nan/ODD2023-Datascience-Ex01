# Ex-01_DS_Data_Cleansing

REG:NO:212223040124
NAME:Nandhana R


## AIM
To read the given data and perform data cleaning and save the cleaned data to a file. 

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. 
Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information. 

# ALGORITHM
### STEP 1
Read the given Data
### STEP 2
Get the information about the data
### STEP 3
Remove the null values from the data
### STEP 4
Save the Clean data to the file

# CODE and OUTPUT

```
import pandas as pd
df=pd.read_csv("/content/SAMPLEIDS (2).csv")
df
```
OP:
![image](https://github.com/user-attachments/assets/4166ad8e-7ee4-4a95-89ba-4ba3db9f3929)
```
df.isnull().sum()
```
op:
![image](https://github.com/user-attachments/assets/52290a7b-7fb6-4996-8bf9-bad39ea1216a)
```
df.isnull().any()
```
op:
![image](https://github.com/user-attachments/assets/5ab1db58-ffeb-4cb7-ad2a-0f05b74d9367)
```
df.dropna()
```
op:
![image](https://github.com/user-attachments/assets/6189e1da-d786-4bd5-985c-f5b32abfe0d3)
```
df.fillna(0)
```
op:
![image](https://github.com/user-attachments/assets/8e0dcde8-498d-4272-96cb-2e6c5f5e2ab9)
```
df.fillna(0)
```
op:
![image](https://github.com/user-attachments/assets/b5f35396-f769-4b07-ae84-007715bad4e8)
```
df.fillna('method=ffill')
```
op:
![image](https://github.com/user-attachments/assets/07a0561f-e792-43f4-b63d-ab94206b55b1)

```
df.fillna(method='bfill')
```
op:
![image](https://github.com/user-attachments/assets/9ced07da-b6fb-4589-8ede-b370e00833d1)
```
ir=pd.read_csv("/content/iris (1).csv")
ir
```
op:
![image](https://github.com/user-attachments/assets/2c8bf6ca-53de-4b99-9270-742d000eef24)
```
ir.describe()
```
op:
![image](https://github.com/user-attachments/assets/5d259fe0-5e49-43f7-992c-7d267c0e2086)
```
import seaborn as sns
sns.boxplot(x='sepal_width',data=ir)
```
op:
![image](https://github.com/user-attachments/assets/31c40f96-3de4-4c4f-96e8-47c54fe51ae3)
```
df.describe()
```
op:
![image](https://github.com/user-attachments/assets/a5876938-459c-481e-ab44-86b8d94ac3cf)
```
import matplotlib.pyplot as plt
import pandas as pd
import numpy as np
import scipy.stats as stats

dataset=pd.read_csv("/content/heights.csv")
dataset
```
op:
![image](https://github.com/user-attachments/assets/3ea76f7e-6846-401f-88ef-49225f4f33cb)
```
z = np.abs(stats.zscore(dataset['height']))
z
```
op:![image](https://github.com/user-attachments/assets/1b5f23f4-ffab-48d6-84f3-65c3446773c7)

```
dataset1 = dataset[z<3]
dataset1
```
op:
![image](https://github.com/user-attachments/assets/e6caaeb7-f61d-4ef7-b3ec-ddbfb0449f0f)
```

Result:
```
Thus we have cleaned the data and removed the outliers by detection using IQR and Z-score method.

















