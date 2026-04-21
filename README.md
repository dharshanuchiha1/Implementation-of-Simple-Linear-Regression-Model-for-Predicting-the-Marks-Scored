# Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored

## AIM:
To write a program to predict the marks scored by a student using the simple linear regression model.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import required libraries and prepare the dataset (X and Y values).
2. Create and train the simple linear regression model using the dataset.
3. Accept input (hours studied) and predict the marks using the trained model. 
4. Display the predicted result and visualize the data using a graph.

## Program:
```
/*
Program to implement the simple linear regression model for predicting the marks scored.
Developed by: Dharshan G
RegisterNumber:  212225230054
*/
import numpy as np
import matplotlib.pyplot as plt
from sklearn.linear_model import LinearRegression

A = np.array([1, 2, 3, 4, 5]).reshape(-1, 1)
B = np.array([35, 50, 65, 70, 85])

m = LinearRegression()

m.fit(A, B)

n = m.coef_[0]
b = m.intercept_

print("Slope (n):", n)
print("Intercept (b):", b)

a_input = float(input("Enter hours studied: "))
predicted_marks = m.predict([[a_input]])
print("Predicted Marks:", predicted_marks[0])

B_pred = m.predict(A)

plt.scatter(A, B, label="Actual Data")
plt.plot(A, B_pred, label="Regression Line")
plt.xlabel("Hours Studied")
plt.ylabel("Marks Scored")
plt.title("Simple Linear Regression (Using sklearn)")
plt.legend()
plt.show()
```

## Output:
![simple linear regression model for predicting the marks scored](sam.png)
<img width="707" height="653" alt="Screenshot 2026-04-21 110507" src="https://github.com/user-attachments/assets/630fa5bc-43b4-4b17-b4b8-313550de1e0f" />
<img width="757" height="588" alt="Screenshot 2026-04-21 110523" src="https://github.com/user-attachments/assets/3248656c-6243-4a18-a15a-03f001555d17" />


## Result:
Thus the program to implement the simple linear regression model for predicting the marks scored is written and verified using python programming.
