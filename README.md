# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import pandas library to read csv or excel file.
2. Import LabelEncoder using sklearn.preprocessing library.
3. Transform the data's using LabelEncoder.
4. Import decision tree classifier from sklearn.tree library to predict the values.
5. Find accuracy.
6. Predict the values.
7. End of the program.

## Program:
```
/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: SANDHIYA R
RegisterNumber:  212222230129
*/
```
```
import pandas as pd
data=pd.read_csv("Employee[1].csv")
data.head()
data.info()
data.isnull().sum()
data["left"].value_counts()
 from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["salary"]=le.fit_transform(data["salary"])
data.head()data["Departments "]=le.fit_transform(data["Departments "])
data.head(100)
data.info()
x=data[["satisfaction_level","last_evaluation","number_project","average_montly_hours","time_spend_company","Work_accident","promotion_last_5years","Departments ","salary"]]
x.head()
x.info()
y=data["left"]
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test= train_test_split(x,y,test_size=0.2,random_state=100)
x_train.shape

from sklearn.tree import DecisionTreeClassifier
dt=DecisionTreeClassifier(criterion="entropy")
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
y_pred
from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
accuracy
dt.predict([[0.5,0.8,9,260,6,0,1,2,1]])
```
## Output:
### data.head():
![image](https://github.com/SandhiyaR1/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/113497571/c4bc31b2-79fc-41e4-ace3-09bb8948158f)

### data.info():
![image](https://github.com/SandhiyaR1/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/113497571/b4df07f4-37e5-4efc-b5ae-7230d06b1e6e)

### data.isnull().sum()
![image](https://github.com/SandhiyaR1/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/113497571/a03be87a-1e7a-4195-bc2f-42c76e900795)

###
![image](https://github.com/SandhiyaR1/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/113497571/e48d1053-d4f6-4407-a6a5-7956aa9176a1)

### After lable encoding:
![image](https://github.com/SandhiyaR1/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/113497571/9ee8f9ef-7280-493c-a071-dfa64396660a)

### x_train.shape
![image](https://github.com/SandhiyaR1/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/113497571/ae2ae673-738b-4939-917c-2a9709c38fae)

### y_pred
![image](https://github.com/SandhiyaR1/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/113497571/be8a89c7-302d-451e-ae5d-d6460b5bfd41)

### accuracy
![image](https://github.com/SandhiyaR1/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/113497571/682ba873-1dde-47c3-8686-af5e1b957269)

### predicted value
![image](https://github.com/SandhiyaR1/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/113497571/bbbfe749-ca6c-4c5a-a14e-b8d1551f209f)




## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
