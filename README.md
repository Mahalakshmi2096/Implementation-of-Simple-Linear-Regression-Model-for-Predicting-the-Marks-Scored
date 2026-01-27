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
import matplotlib.pyplot as plt

X = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12]
Y = [20, 30, 34, 46, 50, 61, 67, 73, 80, 86, 91, 95]

n = len(X)

mean_x = sum(X) / n
mean_y = sum(Y) / n

num = 0
den = 0
for i in range(n):
    num += (X[i] - mean_x) * (Y[i] - mean_y)
    den += (X[i] - mean_x) ** 2

m = num / den
b = mean_y - m * mean_x

print(f"Y = {m:.2f}X + {b:.2f}")

y_pred = [m * x + b for x in X]

plt.scatter(X, Y)
plt.plot(X, y_pred)
plt.xlabel("Study Hours")
plt.ylabel("Marks Scored")
plt.title("Simple Linear Regression with Realistic Data")
plt.show()
```
## Output:

<img width="830" height="605" alt="image" src="https://github.com/user-attachments/assets/51d594fc-536b-4418-9acd-e759a7d2a96c" />

## Result:
Thus the program to implement the simple linear regression model for predicting the marks scored is written and verified using python programming.
