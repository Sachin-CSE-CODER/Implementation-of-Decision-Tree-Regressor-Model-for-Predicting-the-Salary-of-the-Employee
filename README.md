# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import pandas as pd and import the required dataset.

2.Calculate the null values in the dataset.

3.Import the LabelEncoder from sklearn.preprocessing

4.Convert the string values to numeric values.

5.Import train_test_split from sklearn.model_selection.

6.Assign the train and test dataset.

7.Import DecisionTreeRegressor from sklearn.tree.

8.Import metrics from sklearn.metrics.

9.Calculate the MeanSquareError. 10.Apply the metrics to the dataset.

10.Predict the output for the required values.

## Program:

Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

Developed by: SACHIN S

RegisterNumber:  212224040283  

```python
import pandas as pd
data=pd.read_csv("/content/Salary.csv")
data.head()

data.info()

data.isnull().sum()

from sklearn.preprocessing import LabelEncoder
le = LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
data.head()

x= data[["Position","Level"]]
y=data["Salary"]

from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test = train_test_split(x,y,test_size = 0.2,random_state = 2)

from sklearn.tree import DecisionTreeRegressor
dt = DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred = dt.predict(x_test)

from sklearn import metrics
mse = metrics.mean_squared_error(y_test,y_pred)
mse

r2= metrics.r2_score(y_test,y_pred)
r2

dt.predict([[5,6]])

```

## Output:
![{85A07EF3-1B8D-4EFC-8E64-D02A3152A2E4}](https://github.com/user-attachments/assets/8367b62d-a97b-4af1-b994-ef8f18ed8f17)

![{ADB1AF80-087D-4A74-989A-5E2593654123}](https://github.com/user-attachments/assets/fdd2b0ed-6ea8-4d15-b4c9-2ee6d0ea22ce)

![{1895B351-59E8-473D-8EB5-871C3835CDA9}](https://github.com/user-attachments/assets/38fc8dd2-bbc5-4c6b-973a-ee2f053736b3)

![{BD6C0586-CC07-42B6-9D38-FA97A449605C}](https://github.com/user-attachments/assets/17770d3f-61d3-41f1-8b1b-4f7f15fe0a2b)

![{8FED069B-79DF-4E29-90CB-ABFDEE6DD52C}](https://github.com/user-attachments/assets/1213a3bf-e900-462d-956d-4fde69a7393c)

![{2DF81B40-44F1-47EB-91FB-94175D94D6B0}](https://github.com/user-attachments/assets/946f78b3-f91b-440f-9026-7c4f5aa9d785)


## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
