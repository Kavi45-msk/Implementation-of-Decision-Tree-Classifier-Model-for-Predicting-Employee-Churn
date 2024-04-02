# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import the required libraries.
2.Upload and read the dataset.
3.Check for any null values using the isnull() function.
4.From sklearn.tree import DecisionTreeClassifier and use criterion as entropy.
5.Find the accuracy of the model and predict the required values by importing the required module from sklearn.

## Program:
```
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: Kavi M S
RegisterNumber: 212223220044
```
```
import pandas as pd
data = pd.read_csv("Employee.csv")
data.head()
data.info()

data.isnull().sum()

data["left"].value_counts

from sklearn.preprocessing import LabelEncoder
le= LabelEncoder()
data["salary"]=le.fit_transform(data["salary"])
data.head()

x= data[["satisfaction_level","last_evaluation","number_project","average_montly_hours","time_spend_company","Work_accident","promotion_last_5years","salary"]]

x.head()
y=data["left"]

from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test = train_test_split(x,y,test_size=0.2,random_state = 100)

from sklearn.tree import DecisionTreeClassifier
dt = DecisionTreeClassifier(criterion="entropy")
dt.fit(x_train,y_train)

y_pred = dt.predict(x_test)
from sklearn import metrics

accuracy = metrics.accuracy_score(y_test,y_pred)
accuracy

dt.predict([[0.5,0.8,9,260,6,0,1,2]])
```

## Output:
Data.head():
![318627515-158d719b-d564-4a9b-9a82-1c747780c681](https://github.com/Kavi45-msk/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/147457752/311a67fb-1265-447c-938d-0c0272211d09)
Data.info():
![318627574-80d606d1-89a0-44ca-adab-7193369958a0](https://github.com/Kavi45-msk/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/147457752/0d68fe8f-ca3a-497c-b849-cc795adc9da7)
isnull() and sum():
![318627771-1545aa55-7b74-4f88-a551-bda52c90c149](https://github.com/Kavi45-msk/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/147457752/a6d85076-d39f-4a37-9cc7-4faa482709b6)
Data Value Counts():
![318627804-d003e638-3c04-4e84-bec6-704fddd71563](https://github.com/Kavi45-msk/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/147457752/4434df1a-11f9-4442-ade6-b6b8c287d53c)
Data.head() for salary:
![318627853-8a52bc22-65ef-42ef-a679-30347c84d0a8](https://github.com/Kavi45-msk/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/147457752/f6ec96b4-455c-4421-b7df-2b763100718e)
x.head():
![318627905-10d0ce78-537e-4ef4-8018-6d56072c8239](https://github.com/Kavi45-msk/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/147457752/af19bc4f-4230-42f7-9607-63bb491ecb2f)
Accuracy Value:
![318627952-cf94e7fa-20e3-488f-9c0c-ecf336e1dbaa](https://github.com/Kavi45-msk/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/147457752/27177cea-238a-425c-9bf4-2a71622ebe82)
Data prediction:
![318628010-41eba170-e1bd-4819-b4b4-7ef47859b338](https://github.com/Kavi45-msk/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/147457752/8d2cd76b-d23e-4894-b001-1061c09409fc)

## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
