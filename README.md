# Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored


# DATE : 21/04/26

# NAME : SHREEJA R S
# REF.NO : 25017561

## AIM:
To write a program to predict the marks scored by a student using the simple linear regression model.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Get the independent variabble X ( hours studied ) and  dependent variable Y ( marks scored ) .
2. Import Linear Regression from sklearn.linear_model 
3. Fit the model using model.fit(X,Y) .
4. Find slope and intercept using model.coef_ and model.intercept_
5. Give new input value for testing (prediction) and use model.predict() to calculate the predicted Y .
6. Plot the actual data using scatter plot and label axes of the data using plt.legend() .

## Program:
```
/*
Program to implement the simple linear regression model for predicting the marks scored.
Developed by: SHREEJA R S
RegisterNumber:  25017561
*/

# Import libraries

import numpy as np
import matplotlib.pyplot as plt 
from sklearn.linear_model import LinearRegression

# Sample Data ( Inputs )

X = np.array([4,5,6,7,8]).reshape(-1,1)
Y = np.array([40,50,65,75,90])

# Create object for the model

model = LinearRegression()

# Train the model ( use model.fit to train the model )

model.fit(X,Y)

# Get the slope (m) and y - intercept (b)

m = model.coef_[0]
b = model.intercept_

print("Slope (m): ",m)
print("Intercept (b): ",b)

# -- Prediction -- ( giving new inputs to test the model )

x_input = float(input("Enter no of hours studied :"))
predicted_marks = model.predict([[x_input]])
print("Predicted Marks : ",predicted_marks[0])

# -- Plot -- ( eq of st.line )

Y_pred = model.predict(X)

plt.scatter(X,Y,label = "Actual Data")
plt.plot(X,Y_pred,label = "Regression Line")
plt.xlabel("Hours Studied")
plt.ylabel("Marks Scored")
plt.title("Simple Linear Regression(Using sklearn)")
plt.legend()
plt.show()


```

## Output:
![simple linear regression model for predicting the marks scored](sam.png)

<img width="982" height="715" alt="Screenshot 2026-04-21 092816" src="https://github.com/user-attachments/assets/6d40c858-ffa1-4ca3-9789-05f1f1d75604" />


## Result:
Thus the program to implement the simple linear regression model for predicting the marks scored is written and verified using python programming.
