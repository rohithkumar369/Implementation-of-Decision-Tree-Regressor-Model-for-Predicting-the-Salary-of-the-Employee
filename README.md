# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
 1.Import pandas
 
 2.Import Decision tree classifier
 
 3.Fit the data in the model
 
 4.Find the accuracy score

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: S.rohith kumar
RegisterNumber: 24004371 
*/
```
import pandas as pd

data=pd.read_csv("Salary.csv")

data.head()

data.info()

data.isnull().sum()

from sklearn.preprocessing import LabelEncoder

le=LabelEncoder()

data["Position"]=le.fit_transform(data["Position"])

data.head()

print(data.head())

x=data[["Position","Level"]]

print(x.head())

y=data["Salary"]

y.head()

from sklearn.model_selection import train_test_split

x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=2)

from sklearn.tree import DecisionTreeRegressor

dt=DecisionTreeRegressor()

dt.fit(x_train,y_train)

y_pred=dt.predict(x_test)

print(y_pred)

r2=(y_test,y_pred)

print(r2)


dt.predict([[5,6]])


## Output:
![Decision Tree Regressor Model for Predicting the Salary of the Employee](sam.png)
![Screenshot (71)](https://github.com/user-attachments/assets/3ae2d991-2fca-406d-986e-f995b21984e1)
![Screenshot (73)](https://github.com/user-attachments/assets/db9eb6cf-632a-4d98-92f5-dd74c07b57e7)
![Screenshot (74)](https://github.com/user-attachments/assets/32ee6a5e-13df-441a-8fb7-e7ee0a4c2f38)



## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
