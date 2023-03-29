# Implementation of Univariate Linear Regression
## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Get the independent variable X and dependent variable Y.
2. Calculate the mean of the X -values and the mean of the Y -values.
3. Find the slope m of the line of best fit using the formula. 
<img width="231" alt="image" src="https://user-images.githubusercontent.com/93026020/192078527-b3b5ee3e-992f-46c4-865b-3b7ce4ac54ad.png">
4. Compute the y -intercept of the line by using the formula:
<img width="148" alt="image" src="https://user-images.githubusercontent.com/93026020/192078545-79d70b90-7e9d-4b85-9f8b-9d7548a4c5a4.png">
5. Use the slope m and the y -intercept to form the equation of the line.
6. Obtain the straight line equation Y=mX+b and plot the scatterplot.

## Program:
```
/*
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: Revathi D
RegisterNumber:  212221240045
*/
```
#import package
import numpy as np
import matplotlib.pyplot as plt
#preprocessing input data
x=np.array(eval(input()))
y=np.array(eval(input()))
#mean
x_mean=np.mean(x)
y_mean=np.mean(y)
#get the numerator and denominator
num,denom=0,0
#To find sum of
for i in range(len(x)):
num+=(x[i]-x_mean)*(y[i]-y_mean)
denom+=(x[i]-x_mean)**2
#caluculate slope
m=num/denom
#caluculate intercept
b=y_mean-(m*x_mean)
print(m,b)
#line equation
y_predicted=m*x+b
print(y_predicted)
#To plot graph
plt.scatter(x,y)
plt.plot(x,y_predicted,color='blue')
plt.show()
y_predicted1=m*3+b
print(y_predicted1)

## Output:
![output](.//ML1.png)
![output](.//ML2.png)


## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
