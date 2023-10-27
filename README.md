# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm

### Step 1.
Import pandas module and import the required data set.

### Step 2.
Find the null values and count them.

### Step 3.
Count number of left values.

### Step 4.
From sklearn import LabelEncoder to convert string values to numerical values.

### Step 5.
From sklearn.model_selection import train_test_split.

### Step 6.
Assign the train dataset and test dataset.

### Step 7.
From sklearn.tree import DecisionTreeClassifier.

### Step 8.
Use criteria as entropy.

### Step 9.
From sklearn import metrics. 

### Step 10.
Find the accuracy of our model and predict the require values.

## Program:
```
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: MARELLA DHARANESH
RegisterNumber:  212222240062
```
```python
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
accuracy= metrics.accuracy_score(y_test,y_pred)
accuracy

dt.predict([[0.5,0.8,9,260,6,0,1,2]])
```
## Output:

### data.head()
![Screenshot from 2023-10-16 11-19-08](https://github.com/Gchethankumar/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/118348224/48655bcb-9d9e-4b1e-b3fc-e010e41d871d)


### data.info()
![Screenshot from 2023-10-16 11-19-34](https://github.com/Gchethankumar/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/118348224/11f09b30-13ab-4ab1-80ef-aa64ecd564f3)


### isnull() and sum()
![Screenshot from 2023-10-16 11-19-44](https://github.com/Gchethankumar/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/118348224/2d6df42f-8ffb-4ff2-97cd-4c4f617bedee)


### data value counts()
![Screenshot from 2023-10-16 11-19-54](https://github.com/Gchethankumar/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/118348224/756bd98e-eb24-418e-852a-eaf9bd001349)


### data head() for salary
![Screenshot from 2023-10-16 11-20-09](https://github.com/Gchethankumar/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/118348224/301a39b0-d524-4fa0-8463-cfbe651367eb)


### x.head()
![Screenshot from 2023-10-16 11-20-20](https://github.com/Gchethankumar/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/118348224/9f5db096-b94e-4c13-aaac-6283409b5622)


### accuracy value
![Screenshot from 2023-10-16 11-20-34](https://github.com/Gchethankumar/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/118348224/0b2c0de5-81a6-4dd6-9ed4-ce52f1629d3d)


### data prediction
![Screenshot from 2023-10-16 11-20-44](https://github.com/Gchethankumar/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/118348224/577d873a-32dc-488a-b94a-bd0ca4513346)


## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
