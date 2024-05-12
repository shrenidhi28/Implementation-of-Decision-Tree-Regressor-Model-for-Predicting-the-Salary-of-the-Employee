# EXP-7 Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

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
```

```


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

<br>
<br>

# data.head()
<br>
<br>

![image](https://github.com/shrenidhi28/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/155261096/090dc6a4-4081-4cad-9efa-8240869e0d8a)

<br>
<br>

# data.info()

<br>
<br>

![image](https://github.com/shrenidhi28/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/155261096/d785a975-69b2-4d35-9c42-eb446920f67f)

<br>
<br>

# data.isnull().sum()

<br>
<br>

![image](https://github.com/shrenidhi28/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/155261096/4e59774b-f7c3-4ec9-b93c-c0bce6e82656)

<br>
<br>

# x data

<br>
<br>

![image](https://github.com/shrenidhi28/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/155261096/3250258a-74c8-4689-b3d1-38dfed7f5615)

<br>
<br>

# y data

<br>
<br>

![image](https://github.com/shrenidhi28/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/155261096/9ca4a2d2-fe82-48f0-b461-709544347140)

<br>
<br>

# y_pred
<br>
<br>

![image](https://github.com/shrenidhi28/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/155261096/b2b3bb90-b3a5-46c8-a79e-9f1046818fe6)

<br>
<br>

# mse

<br>
<br>

![image](https://github.com/shrenidhi28/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/155261096/28a6ef84-877c-4d97-a6e6-e371e91323be)

<br>
<br>

# r2=metrics.r2_score(y_test,y_pred)

<br>
<br>

![image](https://github.com/shrenidhi28/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/155261096/c8b9e1e0-df68-45b1-98cd-29ee5f373409)

<br>
<br>







## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
