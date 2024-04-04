# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import the required libraries.
2.Upload and read the dataset.
3.Check for any null values using the isnull() function.
4.From sklearn.tree import DecisionTreeClassifier and use criterion as entropy.
5.Find the accuracy of the model and predict the required values by importing the required module from sklearn.

## Program:
```

Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: C.Shrenidhi
RegisterNumber:  212223040196


import pandas as pd
data=pd.read_csv("/content/Salary.csv")
data.head()
data.info()
data.isnull().sum()
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data['Position']=le.fit_transform(data['Position'])
data.head()
x=data[['Level','Position']]
y=data['Salary']
x.head()
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=2)
from sklearn.tree import DecisionTreeClassifier
dt=DecisionTreeClassifier()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
from sklearn import metrics
mse=metrics.mean_squared_error(y_test,y_pred)
mse
r2=metrics.r2_score(y_test,y_pred)
r2
dt.predict([[5,6]])

```

## Output:
![Decision Tree Regressor Model for Predicting the Salary of the Employee](sam.png)
<br>
<br>

data.head()
<br>
<br>
<img width="248" alt="image" src="https://github.com/shrenidhi28/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/155261096/f4019ab5-fb1a-4828-86cb-66574f37edfa">
<br>
<br>
data.info()
<br>
<br>
<img width="247" alt="image" src="https://github.com/shrenidhi28/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/155261096/89d5e508-9bf2-4adb-8938-7c24d39d83b4">
<br>
<br>
data.isnull().sum()
<br>
<br>
<img width="92" alt="image" src="https://github.com/shrenidhi28/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/155261096/141eb5dd-5309-43b9-a7b3-9c425f305b10">
<br>
<br>
data['Position']=le.fit_transform(data['Position'])
<br>
data.head()
<br>
<br>
<img width="175" alt="image" src="https://github.com/shrenidhi28/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/155261096/c600f823-4f0f-431d-9fc4-610b4831996e">
<br>
<br>
x=data[['Level','Position']]
<br>
y=data['Salary']
<br>
x.head()
<br>
<br>
<img width="175" alt="image" src="https://github.com/shrenidhi28/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/155261096/e5a42039-3c21-4897-892b-1ab7536967c4">
<br>
<br>
from sklearn import metrics
<br>
mse=metrics.mean_squared_error(y_test,y_pred)
<br>
mse
<br>
<br>
<img width="175" alt="image" src="https://github.com/shrenidhi28/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/155261096/a24c8f58-69b3-4b71-af54-ecb09594f212">
<br>
<br>
r2=metrics.r2_score(y_test,y_pred)
<br>
r2
<br>
<br>
<img width="153" alt="image" src="https://github.com/shrenidhi28/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/155261096/e23e19b5-de39-4c92-b20f-476e301595aa">
<br>
<br>
/usr/local/lib/python3.10/dist-packages/sklearn/base.py:439: UserWarning: X does not have valid feature names, but DecisionTreeClassifier was fitted with feature names
  warnings.warn(
array([80000])






## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
