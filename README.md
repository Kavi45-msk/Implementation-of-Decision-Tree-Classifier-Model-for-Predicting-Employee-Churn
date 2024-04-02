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
data=pd.read_csv("/content/Employee (1).csv")
data.head()

data.info()

data.isnull().sum()

data['left'].value_counts()

from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()

data['salary']=le.fit_transform(data['salary'])
data.head()

x=data[['satisfaction_level','last_evaluation','number_project','average_montly_hours','time_spend_company','Work_accident','promotion_last_5years','salary']]
x.head()

y=data['left']

from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=100)

from sklearn.tree import DecisionTreeClassifier
dt=DecisionTreeClassifier(criterion='entropy')
dt.fit(x_train,y_train)
y_predict=dt.predict(x_test)

from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_predict)
accuracy

dt.predict([[0.5,0.8,9,260,6,0,1,2]])

```

## Output:
![decision tree classifier model](sam.png)
![318408406-541c24b3-59d2-48d7-81f3-d120d285dd2f](https://github.com/Kavi45-msk/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/147457752/35293119-d5d4-4c3c-b5ad-b1b2bbdd8779)
![318408424-5dd19e9d-6f46-44b1-aad0-fb75131a25fa](https://github.com/Kavi45-msk/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/147457752/7c4e4c71-2cb1-46d4-ad36-bbde25c8f4c2)
![318408454-2272c806-838b-4d04-aeb1-82fc809045d4](https://github.com/Kavi45-msk/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/147457752/734587d5-b7fb-4aab-b88c-db70eaf94d7d)
![318408484-c0437120-e318-4285-b86d-7a561abdd8bf](https://github.com/Kavi45-msk/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/147457752/70dbe8d4-3dff-4df3-b724-16a16c5d1d80)
![318408505-e0105ab9-f922-4de5-97ae-c7f296cd8ec0](https://github.com/Kavi45-msk/Implementation-of-De
![318408525-5769c780-813f-4d20-8c9a-e646b4b6a90e](https://github.com/Kavi45-msk/Implementation-of-Decision-Tree-Classifier-Model-for-Predi
![318408318-df2b9024-c189-4566-8a9a-a953d5229f2b](https://github.com/Kavi45-msk/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/147457752/72a24351-38ec-4d96-a511-67a7b0ea0a7f)

cting-Employee-Churn/assets/147457752/bf3699b6-30b2-4d74-91d3-ef05cd279002)
cision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/147457752/774895c6-4ea3-44ed-8303-bdd864c42b87)


## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
