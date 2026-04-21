# Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored

## AIM:
To write a program to predict the marks scored by a student using the simple linear regression model.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Data Preparation -  Defining the datas that are used in the Linear Regression model.
2. Model Training - Training the Model with the defined data to make the correct predictions for future input using ```model.fit()``` method.
3. Prediction & Input - Taking input from the user and Predicting the possible output using ```model.predict()``` method
4. Visualization - Visualizing the data and also ploting the Line of Linear Regression using MatplotLib Libraray.

## Program:
```
Program to implement the simple linear regression model for predicting the marks scored.
Developed by: Athul Krishna A V
RegisterNumber:  212225240017


import numpy as np
import matplotlib.pyplot as plt
from sklearn.linear_model import LinearRegression

X = np.array([1, 2, 3, 4, 5]).reshape(-1, 1)
Y = np.array([35, 50, 65, 70, 85])

Model = LinearRegression()

Model.fit(X,Y)

m = Model.coef_[0]
b = Model.intercept_

print("Slope of the Model", m)
print("Intercept on the graph",b)


x = float(input("Enter X value / Enter Number of Hours: "))
y = Model.predict([[x]])
print("Predicted Value of Y / Predicted Mark is: ",y)

y_pred = Model.predict(X)

plt.figure(figsize=(5,4))
plt.scatter(X,Y,label="Given Points")
plt.plot(X,y_pred,label="Predicted Marks")
plt.xlabel("Hours of Study")
plt.ylabel("Marks scored")
plt.title("Simple Linear Regression (using Scikit-Learn library)")
```

## Output:
<img width="668" height="614" alt="image" src="https://github.com/user-attachments/assets/24556f7b-c061-4e2c-86ab-5cb95320ee29" />


## Result:
Thus the program to implement the simple linear regression model for predicting the marks scored is written and verified using python programming.
