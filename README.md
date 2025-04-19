# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the standard libraries.

2.Upload the dataset and check for any null values using .isnull() function.

3.Import LabelEncoder and encode the dataset.

4.Import DecisionTreeRegressor from sklearn and apply the model on the dataset.


5.Predict the values of arrays.

6.Import metrics from sklearn and calculate the MSE and R2 of the model on the dataset.

7.Predict the values of array.

8.Apply to new unknown values.
  
## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: Vaishak.M
RegisterNumber:212224040355
*/
```
```
import pandas as pd
data=pd.read_csv("Salary.csv")
data.head()
```
![image](https://github.com/user-attachments/assets/d5696b1e-79a4-4471-bbd7-538954736a2a)
```
data.info()
```
![image](https://github.com/user-attachments/assets/93fe6f10-587b-446b-8dbe-42a11640a86d)
```
data.isnull().sum()
```
![image](https://github.com/user-attachments/assets/22115ea3-83fb-455d-ae2a-f02f1030eb58)
```
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
```
```
data["Position"]=le.fit_transform(data["Position"])
data.head()
```
![image](https://github.com/user-attachments/assets/ee98306e-4e7e-43b0-8ee8-1dc0c9f8a636)
```
y=data["Salary"]
y.head()
```
![image](https://github.com/user-attachments/assets/9a69c2b0-c09e-4f10-b8ce-11de0709a5cd)
```
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=2)
```
![image](https://github.com/user-attachments/assets/bc5c1c14-e2d4-4b50-95a1-1aa8ef14c484)

```
from sklearn import metrics
mse=metrics.mean_squared_error(y_test,y_pred)
mse
```
![image](https://github.com/user-attachments/assets/d380b34a-cf12-4cdd-8c3c-a09f7e844a8b)
```
r2=metrics.r2_score(y_test,y_pred)
r2
```
![image](https://github.com/user-attachments/assets/df4d7d0c-dc65-48e0-a304-eeab242e9b4d)
```
dt.predict([[5,6]])
```
![image](https://github.com/user-attachments/assets/b5c5a457-9ece-491b-ac75-513b55897819)


## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
