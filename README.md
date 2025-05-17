# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.import pandas module and import the required data set.
2.Find the null values and count them. Count number of left values. 
4.From sklearn import LabelEncoder to convert string values to numerical values. 
5.From sklearn.model_selection import train_test_split. 6.Assign the train dataset and test dataset. 
7.From sklearn.tree import DecisionTreeClassifier . Use criteria as entropy. 
8.From sklearn import metrics. 
9.Find the accuracy of our model and predict the require values.

## Program:
```
/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: Vimala Rani A
RegisterNumber:  212223040240

import pandas as pd
data=pd.read_csv("/content/Employee.csv")
data.head()
data.info()
data.isnull().sum()
data["left"].value_counts()
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["salary"]=le.fit_transform(data["salary"])
data.head()
x=data[["satisfaction_level","last_evaluation","number_project","average_montly_hours","time_spend_company","Work_accident","promotion_last_5years","salary"]]
x.head()
y=data["left"]
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=100)
from sklearn.tree import DecisionTreeClassifier
dt=DecisionTreeClassifier(criterion="entropy")
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
accuracy
dt.predict([[0.5,0.8,9,260,6,0,1,2]])
*/
```

## Output:
Data.head()
![323627311-c4c54e86-9348-41be-9e16-c13bf0ce29dc](https://github.com/RamkumarGunasekaran/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/144870820/69024fb4-7594-498f-8a62-13bbd6c41317)
Data.head()for salary:
![323627788-50b3e487-9e5a-4197-8dae-b219c75f867d](https://github.com/RamkumarGunasekaran/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/144870820/7575d74b-b898-4177-8058-adc0071c992a)
x.head():
![323627950-0dd44e4f-3443-4107-8b4c-f18cc2f00ed3](https://github.com/RamkumarGunasekaran/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/144870820/4d1d8600-df07-4c59-ab54-68b15332005d)
Accuracy Value:

![323628110-0a43bb55-252e-4bbf-be71-810c6cd9f59e](https://github.com/RamkumarGunasekaran/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/144870820/df662c76-a5f9-49c5-a541-ce7d4a3125f1)

Data Prediction:
![323628218-5cd36afc-05c0-4144-bbd6-5434676f8b1a](https://github.com/RamkumarGunasekaran/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/144870820/801f66d9-1a91-436b-883c-4618b085f9f3)

## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
