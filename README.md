# Ex:05 Feature Generation


Reg No : 212221040013

Date : 

<br>

## AIM

To read the given data and perform  Feature Encoding & Scaling process and save the data to a file.

<br>

## Explanation

Feature Generation (also known as feature construction, feature extraction or feature engineering) is the process of transforming features into new features that better relate to the target.

<br>

## ALGORITHM

### STEP 1
Read the given Data

### STEP 2
Clean the Data Set using Data Cleaning Process

### STEP 3
Apply Feature Generation techniques to all the feature of the data set

### STEP 4
Save the data to the file

<br>

## CODE and OUTPUT

```py
import pandas as pd
from scipy import stats
import numpy as np
df = pd.read_csv("bmi.csv")
df.head()
df.dropna()
max_val = np.max(np.abs(df[['Height','Weight']]))
max_val
```
![image](https://github.com/Anbuselvan04/ODD2023-Datascience-Ex-05/assets/119410896/52a14a09-9a4d-4d59-96de-f06048217677)
![image](https://github.com/Anbuselvan04/ODD2023-Datascience-Ex-05/assets/119410896/79b08787-e1e2-4cef-8c5b-d90dcb596af8)

<br>

### Standard Scaler
```
from sklearn.preprocessing import StandardScaler
sc = StandardScaler()
df[['Height','Weight']] = sc.fit_transform(df[['Height','Weight']])
df.head(10)
```
![image](https://github.com/Anbuselvan04/ODD2023-Datascience-Ex-05/assets/119410896/2e52bd78-85e4-4c08-be5b-37f02963b63e)

<br>

### MinMax Scaler
```
from sklearn.preprocessing import MinMaxScaler
scaler = MinMaxScaler()
df[['Height','Weight']] = scaler.fit_transform(df[['Height','Weight']])
df.head(10)
```
![image](https://github.com/Anbuselvan04/ODD2023-Datascience-Ex-05/assets/119410896/02459078-5e96-42b1-90d1-4e76f169158e)

<br>

### Normalizer
```
from sklearn.preprocessing import Normalizer
scaler = Normalizer()
df[['Height','Weight']] = scaler.fit_transform(df[['Height','Weight']])
df
```
![image](https://github.com/Anbuselvan04/ODD2023-Datascience-Ex-05/assets/119410896/4139d4aa-4c33-4977-8e6d-be1f4f129672)

<br>

### MaxAbs Scaler
```
from sklearn.preprocessing import MaxAbsScaler
scaler = MaxAbsScaler()
df[['Height','Weight']] = scaler.fit_transform(df[['Height','Weight']])
df
```
![image](https://github.com/Anbuselvan04/ODD2023-Datascience-Ex-05/assets/119410896/91e4043d-8aca-40b5-8d96-f6b255bf9877)

<br>

### Robust Scaler 
```
from sklearn.preprocessing import RobustScaler
scaler = RobustScaler()
df[['Height','Weight']] = scaler.fit_transform(df[['Height','Weight']])
df.head()
```
![image](https://github.com/Anbuselvan04/ODD2023-Datascience-Ex-05/assets/119410896/de9d511b-53db-413a-8a6e-3af361bd13c4)

<br>

## Result :
The Programs has been executed successfully.
