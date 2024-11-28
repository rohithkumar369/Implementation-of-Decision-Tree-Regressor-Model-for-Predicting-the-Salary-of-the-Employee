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
Developed by: S.Rohith kumar
RegisterNumber:24004371  
*/
import pandas as pd

 data=pd.read_csv("/Salary.csv")

 data.head()

 data.info()

 data.isnull().sum()

 from sklearn.preprocessing import LabelEncoder

 le=LabelEncoder()

 data["Position"]=le.fit_transform(data["Position"])

 data.head()

 x=data[["Position","Level"]]

 x.head()

 y=data["Salary"]

 y.head()

 from sklearn.model_selection import train_test_split

 x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=2)

 from sklearn.tree import DecisionTreeRegressor

 dt=DecisionTreeRegressor()

 dt.fit(x_train,y_train)

 y_pred=dt.predict(x_test)

 y_pred

 r2=metrics.r2_score(y_test,y_pred)
 r2
 dt.predict([[5,6]])
```

## Output:
![Decision Tree Regressor Model for Predicting the Salary of the Employee](sam.png)
![WhatsApp Image 2024-11-28 at 20 57 06_5f3a99b7](https://github.com/user-attachments/assets/56bbdb5f-1a62-40aa-9f83-823283200e17)
![WhatsApp Image 2024-11-28 at 20 57 07_fa12b358](https://github.com/user-attachments/assets/4a9db747-80d8-4ad8-987b-02be3ad073e6)
![WhatsApp Image 2024-11-28 at 20 57 08_3900f338](https://github.com/user-attachments/assets/1027255d-8493-4db8-9ae3-0d1bc9bb54c8)


## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
