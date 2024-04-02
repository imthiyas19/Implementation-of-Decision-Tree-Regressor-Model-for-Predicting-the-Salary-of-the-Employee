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
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: MOHAMMED IMTHIYAS.M
RegisterNumber:212222230083  
```
```
import pandas as pd
data=pd.read_csv("/content/Salary(1).csv")
print('data.head():')
data.head()
print('data.info():')
data.info()
print('isnull() and sum():')
data.isnull()
print('data.head() for salary:')
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
data.head()
x = data[["Position","Level"]]
y = data["Salary"]
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test = train_test_split(x,y,test_size=0.2,random_state=2)
from sklearn.tree import DecisionTreeRegressor
dt = DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred = dt.predict(x_test)
print('MSE value:')
from sklearn import metrics
mse = metrics.mean_squared_error(y_test,y_pred)
mse
print('r2 value:')
r2 = metrics.r2_score(y_test,y_pred)
r2
print('data prediction:')
dt.predict([[5,6]])
```
## Output:
![Decision Tree Regressor Model for Predicting the Salary of the Employee](sam.png)
![240625208-852c50c9-64bb-4412-b661-8f6b55feb5a0](https://github.com/NathinR/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118679646/40b57ed6-916f-4c5f-ae06-d3927ecab9f0)

![240625274-9ddf7ade-efec-4780-ba6c-2fdad008f207](https://github.com/NathinR/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118679646/162cc530-285b-47cd-85c7-807f4ab6401b)

![240625422-6ab42b5a-c402-44b4-aac4-eccf4a329d6f](https://github.com/NathinR/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118679646/7d03f7f1-a482-4d22-a228-99576dbb236d)

![240625547-06a63650-48a7-4742-bc37-417a56767409](https://github.com/NathinR/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118679646/11db55e8-aebf-43ac-94ca-7a70689e06bb)

![240625613-f21aa42f-96be-4ed8-8432-8278c0e6429f](https://github.com/NathinR/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118679646/8dd0e191-2656-4b14-a51e-b5292309b04c)

![240625661-d2d35478-e397-49a0-8530-6db4aabd85f0](https://github.com/NathinR/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118679646/716be9ee-70bc-490f-bddf-bc138b8c6630)

![240625836-a11b4bf4-fc84-4214-8595-9865efa559bb](https://github.com/NathinR/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118679646/64d55f11-59e4-4413-bbf0-61b4c180a331)

## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.

