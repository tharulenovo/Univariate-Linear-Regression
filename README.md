# Implementation of Univariate Linear Regression
## Aim:
To implement univariate Linear Regression to fit a straight line using least squares.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
1.	Get the independent variable X and dependent variable Y.
2.	Calculate the mean of the X -values and the mean of the Y -values.
3.	Find the slope m of the line of best fit using the formula.
 ![eqn1](./eq1.jpg)
4.	Compute the y -intercept of the line by using the formula:
![eqn2](./eq2.jpg)  
5.	Use the slope m and the y -intercept to form the equation of the line.
6.	Obtain the straight line equation Y=mX+b and plot the scatterplot.
## Program
```
import numpy as np

X = np.array(eval(input("Enter X values as a list: ")))
Y = np.array(eval(input("Enter Y values as a list: ")))  

X_mean = np.mean(X)
Y_mean = np.mean(Y)

num = 0
don = 0
for i in range(len(X)):
    num += (X[i] - X_mean) * (Y[i] - Y_mean)
    don += (X[i] - X_mean) ** 2

m = num / don
c = Y_mean - m * X_mean

print("Slope (m):", m)
print("Intercept (c):", c)

Y_pred = m * X + c
print("Predicted Y values:", Y_pred)

```
## Output
<img width="367" height="116" alt="Screenshot 2025-10-19 214726" src="https://github.com/user-attachments/assets/9b693bb6-6815-481c-8b63-04cfcd2300b4" />


## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
