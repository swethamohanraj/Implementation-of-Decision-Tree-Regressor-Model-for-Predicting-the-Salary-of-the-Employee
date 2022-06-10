# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
```
1. Import the required libraries.
2. Upload the csv file and read the dataset.
3. Check for any null values using the isnull() function.
4. From sklearn.tree inport DecisionTreeRegressor.
5. Import metrics and calculate the Mean squared error.
6. Apply metrics to the dataset, and predict the output.
```
## Program:
```
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: K.M.SWETHAA 
RegisterNumber:212221240055
import pandas as pd
data=pd.read_csv("/content/Salary.csv")

data.head()

data.info()

data.isnull().sum()

from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()

data["Position"]=le.fit_transform(data["Position"])
data.head()

x=data[["Position","Level"]]
x.head()

y=data[["Salary"]]

from sklearn.model_selection import train_test_split
x_train, x_test, y_train, y_test=train_test_split(x,y,test_size=0.2,random_state=2)

from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)

from sklearn import metrics
mse=metrics.mean_squared_error(y_test, y_pred)
mse

r2=metrics.r2_score(y_test,y_pred)
r2

dt.predict([[5,6]])
```

## Output:
### Head Data
![image](https://user-images.githubusercontent.com/94228215/172994847-509fbfc1-e5f7-410e-b35b-33659f8ce2c4.png)

### Information of Data
![image](https://user-images.githubusercontent.com/94228215/172994860-84140b73-e49e-4323-bb9c-d7fa9d6e8381.png)

### Null Data
![image](https://user-images.githubusercontent.com/94228215/172994880-b8b1f88f-79f2-4ba7-a22d-fafca6b2e111.png)

### Transformed Head Data
![image](https://user-images.githubusercontent.com/94228215/172994901-14035105-077d-4eb5-91e8-187bee5eed5c.png)

### X.Head()
![image](https://user-images.githubusercontent.com/94228215/172994913-236a7a43-688d-456b-8479-f24a50a33bd6.png)

### Mean Square Error
![image](https://user-images.githubusercontent.com/94228215/172994928-e1d8362e-4662-4bec-8afa-4e1ba8e71010.png)

### R2
![image](https://user-images.githubusercontent.com/94228215/172994951-912ec241-31f2-46a8-bf12-abd42e45601c.png)

### Data Prediction
![image](https://user-images.githubusercontent.com/94228215/172994964-8639d547-494b-4d6e-8ec5-73f966154b06.png)



## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
