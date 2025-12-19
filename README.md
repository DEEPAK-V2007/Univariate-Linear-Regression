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
'''
Python program to implement univariate Linear Regression to fit a straight line using least squares.
#Developed by: DEEPAK.V
#Register No: 25017595
'''

import numpy as np
import matplotlib.pyplot as plt
x = np.array([0,1,2,3,4,5,6,7,8,9])
y = np.array([1,3,2,5,7,8,8,9,10,12])
plt.scatter(x,y)
plt.show()
xmean = np.mean(x)
ymean = np.mean(y)
num=0
den=0
for i in range(len(x)):
    num+=(x[i]-xmean)*(y[i]-ymean)
    den+=(x[i]-xmean)**2
m = num/den
b = ymean - m*xmean
print(m,b)
ypred = m*x+b
print(ypred)


plt.scatter(x,y,color='Red')
plt.plot(x,ypred,color='Blue')
plt.show()
```
## Output
</br>
<img width="1369" height="693" alt="{FC2E15A0-65C9-4D9C-8667-D6F6736F417B}" src="https://github.com/user-attachments/assets/674ed314-0d56-4f73-a40d-45f96dd2a714" />
</br>
<img width="683" height="588" alt="{A26413A6-D8DF-45F7-872D-C4F68DB5E0FC}" src="https://github.com/user-attachments/assets/9d565919-d05d-4d22-a6c0-d72a685eca93" />
</br>
<img width="695" height="512" alt="{E67F5350-1282-453B-BC5D-ECA167F8F31A}" src="https://github.com/user-attachments/assets/f8bce7a8-ea1d-444e-98b8-675defe96c83" />
</br>

## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
