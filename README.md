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
Devoloped by JEEVAN VISHAL G.D
Reg No:212224240062

import numpy as np
import matplotlib.pyplot as plt

x = np.array([1, 2, 3, 4, 5])
y = np.array([2, 3, 5, 7, 11])

x_mean = np.mean(x)
y_mean = np.mean(y)

m = sum((x - x_mean) * (y - y_mean)) / sum((x - x_mean)**2)

c = y_mean - m * x_mean

y_pred = m * x + c

plt.scatter(x, y, color='blue', label='Data Points')
plt.plot(x, y_pred, color='red', label='Regression Line')
plt.xlabel("X")
plt.ylabel("Y")
plt.legend()
plt.show()

print(f"Slope (m): {m:.2f}")
print(f"Intercept (c): {c:.2f}")

```
## Output

![Screenshot 2025-05-05 144458](https://github.com/user-attachments/assets/e4c0d5e4-5d1b-4d1f-a0fd-2a1e07dda0c5)


## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
