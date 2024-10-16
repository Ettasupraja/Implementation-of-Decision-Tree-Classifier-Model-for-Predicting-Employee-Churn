# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
```
1. mport pandas module and import the required data set.
2.Find the null values and count them.
3.Count number of left values.
4.From sklearn import LabelEncoder to convert string values to numerical values.
5.From sklearn.model_selection import train_test_split.
6.Assign the train dataset and test dataset.
7.From sklearn.tree import DecisionTreeClassifier.
8.Use criteria as entropy.
9.From sklearn import metrics.
10.Find the accuracy of our model and predict the require values.

```
## Program:
```
/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: ETTA SUPRAJA
RegisterNumber: 212223220022
import pandas as pd
data = pd.read_csv("Employee.csv")
data
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
*/
```

## Output:
![image](https://github.com/user-attachments/assets/1e25fe31-e5ca-4409-bd2d-ce6487f739d0)
![image](https://github.com/user-attachments/assets/8015083d-e505-48bd-b839-e67a7dac2495)
![image](https://github.com/user-attachments/assets/35204ece-a0a1-4069-8ee7-d701c46988cf)
![image](https://github.com/user-attachments/assets/cc002634-86c3-48af-a3d7-60c63565f763)
![image](https://github.com/user-attachments/assets/69ff6147-0acd-464f-bfa4-1a7c4a3ba85b)
![image](https://github.com/user-attachments/assets/68301ada-e5e3-4af7-8823-607a5f5ceff0)
![image](https://github.com/user-attachments/assets/c00122f2-be15-42f8-8aae-0aef12f9b1c1)
![image](https://github.com/user-attachments/assets/4c78adb4-59dd-4774-bad7-4f9ce76c5b3c)


## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
