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
import matplotlib.pyplot as plt

x = np.array([0,1,2,3,4,5,6,7,8,9])
y = np.array([1,3,2,5,7,8,8,9,10,12])

plt.scatter(x,y)
plt.show()

xmean = np.mean(x)
ymean = np.mean(y)

num = 0
den = 0

for i in range(len(x)):
    num += (x[i]-xmean)*(y[i]-ymean)
    den += (x[i]-xmean)**2

m = num/den
b = ymean-m*xmean
print(m,b)

ypred = m*x + b
print(ypred)

plt.scatter(x,y,color='red')
plt.plot(x,ypred, color='blue')
plt.show()





```
## Output
</br>![Screenshot 2025-05-01 163320](https://github.com/user-attachments/assets/07244e05-6b5f-4ec2-8cb4-94620dccd3e7)

</br>![Screenshot 2025-05-01 163354](https://github.com/user-attachments/assets/0c0e4027-61e3-49a5-b6a6-850b24043575)

</br>![Screenshot 2025-05-01 163503](https://github.com/user-attachments/assets/9b3e5d7d-0c43-44cf-90fd-f7e3321cc5ec)

</br>

## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
