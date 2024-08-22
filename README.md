# Implementation of Univariate Linear Regression
## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
step 1: start

step 2: Get the independent variable X and dependent variable Y.

step 3: Calculate the mean of the X -values and the mean of the Y -values.

step 4: Find the slope m of the line of best fit using the formula. 

<img width="231" alt="image" src="https://user-images.githubusercontent.com/93026020/192078527-b3b5ee3e-992f-46c4-865b-3b7ce4ac54ad.png">

step 5: Compute the y -intercept of the line by using the formula:

<img width="148" alt="image" src="https://user-images.githubusercontent.com/93026020/192078545-79d70b90-7e9d-4b85-9f8b-9d7548a4c5a4.png">

step 6: Use the slope m and the y -intercept to form the equation of the line.

step 7: Obtain the straight line equation Y=mX+b and plot the scatterplot.

step 8: End


## Program:
```
/*
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: MAHASRI P
RegisterNumber:  212223100029
*/
```
```
import numpy as np
import matplotlib.pyplot as plt

#Preprocessing input data
X= np.array(eval(input()))
Y= np.array(eval(input()))

#Mean
X_mean= np.mean(X)
Y_mean= np.mean(Y)
num=0
denom=0

#to find the sum of (xi-x') & (yi-y') & (xi-x')^2
for i in range(len(X)):
  num+=(X[i]-X_mean)*(Y[i]-Y_mean)
  denom+=(X[i]-X_mean)**2

#calculate slope
m=num/denom
#calculate intercept

b=Y_mean - m*X_mean
print(m,b)

#Line equation
Y_predicted=m*X + b
print(Y_predicted)

#To plot graph
plt.scatter(X,Y)
```

## Output:
### slope and y-intercept
![Screenshot 2024-08-22 032859](https://github.com/user-attachments/assets/72487fa0-0622-42c5-b388-0f82e59ce8fd)

### Y predicted
![Screenshot 2024-08-22 033015](https://github.com/user-attachments/assets/ab378e2a-fd4b-4327-8620-7c6276e6bc61)

### Graph
![Screenshot 2024-08-22 033025](https://github.com/user-attachments/assets/8e67d910-3d27-48eb-89b4-db8303533378)



## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
