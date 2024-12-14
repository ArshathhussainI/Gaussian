# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
### Step 1:
First,we want to import numpy,then import sys,assume a variable.

### Step 2:
For gaussian elimination method, we want to make 2nd and 3rd column zero.

### Step 3:
For that we want to make a range accorting to our program output.

### Step 4:
Then print the program with correct form then the output will display.
## Program:
```
/*
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: ARSHATH HUSSAIN I
RegisterNumber: 24008800
*/
'''Program to solve a matrix using Gaussian elimination without partial pivoting.
Developed by: 
RegisterNumber: 
'''
import numpy as np
n=int(input())
matrix=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        matrix[i][j]=int(input())
for i in range(n):
    for j in range(i+1,n):
        ratio=matrix[j][i]/matrix[i][i]
        for k in range(n+1):
            matrix[j][k]=matrix[j][k]-ratio*matrix[i][k]
#back substitution
x[n-1]=matrix[n-1][n]/matrix[n-1][n-1]
for i in range(n-2,-1,-1):
    x[i]=matrix[i][n]
    for j in range(i+1,n):
        x[i]=x[i]-matrix[i][j]*x[j]
    x[i]=x[i]/matrix[i][i]
for i in range(n):
    print("X%d = %0.2f" %(i,x[i]),end=" ")
```

## Output

![Screenshot 2024-12-07 124802](https://github.com/user-attachments/assets/39f3447f-6992-4723-a7f4-a2c7d1464a27)





## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

