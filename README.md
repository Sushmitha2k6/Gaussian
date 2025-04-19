# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. import the numpy module to use the built-in function for calculation
2. import sys and assign in np.zeros()
3. using the for loop,we can find the gaussian of the given matrix.
4. end the program 

## Program:
'''Program to solve a matrix using Gaussian elimination without partial pivoting.
Developed by: SUSHMITHA S
RegisterNumber: 212224230282
```
import numpy as np
import sys
n = int(input())
a = np.zeros((n,n+1))
x = np.zeros(n)
for i in range(n):
    for j in range(n+1):
        a[i][j]=float(input())
for i in range(n):
    if a[i][i]==0.0:
        sys.exit('Divide by zero detected!')
    for j in range(i+1,n):
        ratio=a[j][i]/a[i][i]
        for k in range(n+1):
            a[j][k]=a[j][k]-ratio*a[i][k]
x[n-1] = a[n-1][n]/a[n-1][n-1]
for i in range(n-2,-1,-1):
    x[i]=a[i][n]
    for j in range(i+1,n):
        x[i]=x[i]-a[i][j]*x[j]
    x[i]=x[i]/a[i][i]
for i in range(n):
    print('X%d = %0.2f'%(i,x[i]),end= ' ')
```

## Output:

![Screenshot 2025-04-15 111825](https://github.com/user-attachments/assets/2e9c70be-9d48-4292-a61a-99d925b1244a)


## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

