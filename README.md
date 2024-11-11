# DATE:
# EX NO:09
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
# Program for Univariate linear regression using the least squares method.
# Developed by: Kamalesh y
# Register Number: 24004024


import numpy as np 
import matplotlib.pyplot as plt 
x = np.array([0,1,2,3,4,5,6,7,8,9]) 
y= np.array([1,3,2,5,7,8,8,9,10,12]) 
plt.scatter (x,y) 
plt.show() 
xmean = np.mean(x) 
ymean = np.mean(y) 
num=0 
den=0
for i in range(len(x)): 
  num+=(x[i]-xmean)*(y[i]-ymean) 
  den+=(x[i]-xmean) **2 
m = num/den 
b = ymean - m*xmean 
print(m,b) 
ypred = m*x+b 
print(ypred) 

plt.scatter(x, y, color='Blue') 
plt.plot(x, ypred, color='Green') 
plt.show()
```
## Output
![image](https://github.com/user-attachments/assets/a19bf46a-59af-4178-b138-63067261c39f)

![image](https://github.com/user-attachments/assets/5c6709d7-d9d6-449f-91ab-aee6af7875e8)

![image](https://github.com/user-attachments/assets/63d0ca9a-8b70-4187-8de7-1f1124e45a90)

## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
