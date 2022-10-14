# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1.Import numpy as np.

2.Get the values from the user as input.

3.Use Gaussian elimination method without partial pivoting to solve a matrix.

4.Find the solution.

5.Display the result.

## Program:
```python
/*
#Program to find the solution of a matrix using Gaussian Elimination.
#Developed by: Saileshkumar A
#RegisterNumber: 22003843
import numpy as np
import sys
n=int(input())
a=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        a[i][j]=float(input())
for i in range(n):
    if a[i][j]==0.0:
        sys.exit('Divide by zero found!')
    for j in range(i+1,n):
        scalar=a[j][i]/a[i][i]
        for k in range(n+1):
            a[j][k]=a[j][k]-scalar*a[i][k]
x[n-1]=a[n-1][n]/a[n-1][n-1]
for i in range(n-2,-1,-1):
    x[i]=a[i][n]
    for j in range(i+1,n):
        x[i]=x[i]-a[i][j]*x[j]
    x[i]=x[i]/a[i][i]
for i in range(n):
    print('X%d = %0.2f'%(i,x[i]),end= ' ')


```

## Output:
![gaussian elimination](g2.png)
![output](g1.png)


## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

