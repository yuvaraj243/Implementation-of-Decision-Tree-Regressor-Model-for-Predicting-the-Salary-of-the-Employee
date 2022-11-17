# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the required libraries.
2. Upload the csv file and read the dataset.
3. Check for any null values using the isnull() function.
4. From sklearn.tree inport DecisionTreeRegressor.
5. Import metrics and calculate the Mean squared error.
6. Apply metrics to the dataset, and predict the output.

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: YUVARAJ V
RegisterNumber:  212220220056

import pandas as pd
data = pd.read_csv("Salary.csv")
data.head()
data.info()
data.isnull().sum()
from sklearn.preprocessing import LabelEncoder
le = LabelEncoder()
data["Position"] = le.fit_transform(data["Position"])
data.head()
x = data[["Position","Level"]]
y = data["Salary"]
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test = train_test_split(x,y,test_size=0.2,random_state=2)
from sklearn.tree import DecisionTreeRegressor
dt = DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred = dt.predict(x_test)
from sklearn import metrics
mse = metrics.mean_squared_error(y_test,y_pred)
mse
r2 = metrics.r2_score(y_test,y_pred)
r2
dt.predict([[5,6]])

*/
```

## Output:
## Data Head:
![SS1](https://user-images.githubusercontent.com/115924983/200125452-71aeb9f9-59c4-4cdc-bae3-a2744b703087.png)

## Data Information:
![SS2](https://user-images.githubusercontent.com/115924983/200125487-0a28e39a-8b8f-4483-bce1-d7842bbfb294.png)

## Data Head after applying LabelEncoder:
![SS3](https://user-images.githubusercontent.com/115924983/200125569-a8a4286c-7e0a-4805-9425-4672bf1bf11c.png)

## MSE:
![SS4](https://user-images.githubusercontent.com/115924983/200125592-1042fb62-13b8-440a-a49f-e5103e0f8751.png)

## R2:
![SS5](https://user-images.githubusercontent.com/115924983/200125620-0c4f8294-d509-4062-adfa-c88f3fe6e01c.png)

## Data Prediction:
![SS6](https://user-images.githubusercontent.com/115924983/200125648-bd3a7507-51ec-4b10-8a1f-d8e7770f2c12.png)


## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
