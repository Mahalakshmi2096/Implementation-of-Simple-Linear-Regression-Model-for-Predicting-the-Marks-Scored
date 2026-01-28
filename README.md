# Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored

## AIM:
To write a program to predict the marks scored by a student using the simple linear regression model.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import the standard libraries

2.Set variables for assigning dataset values

3.Import linear regression from sklearnr

4.Assign the points for representing the graph

5.Predict the regressio for makes by using the representation of the graph

6.Compare the graphs and hence we obtained the linear regression for the given datas

## Program:
Program to implement the simple linear regression model for predicting the marks scored.

Developed by: Mahalakshmi B

RegisterNumber:  212224040182

```
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt

# Read data from CSV file
data = pd.read_csv("student_scores.csv")

X = data['Hours'].values
y = data['Scores'].values

# Mean values
mean_x = np.mean(X)
mean_y = np.mean(y)

# Slope and intercept
m = np.sum((X - mean_x) * (y - mean_y)) / np.sum((X - mean_x) ** 2)
c = mean_y - m * mean_x

# User input
hours = float(input("Enter number of study hours: "))

# Prediction
predicted_marks = m * hours + c

print("Study Hours:", hours)
print("Predicted Marks:", round(predicted_marks, 2))
print(f"Regression Equation: Y = {m:.2f}X + {c:.2f}")

# Plot
y_pred = m * X + c
plt.scatter(X, y)
plt.plot(X, y_pred)
plt.xlabel("Study Hours")
plt.ylabel("Marks Scored")
plt.title("Simple Linear Regression with Realistic Data")
plt.show()
```
## Output:

<img width="811" height="663" alt="image" src="https://github.com/user-attachments/assets/21c15aa3-b27e-40fc-be77-cf3d435be220" />

## Result:
Thus the program to implement the simple linear regression model for predicting the marks scored is written and verified using python programming.
