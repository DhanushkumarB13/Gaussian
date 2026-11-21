# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. First,we want to import numpy,then import sys,assume a variable.
2. For gaussian elimination method, we want to make 2nd and 3rd column zero.
3. For that we want to make a range accorting to our program output.
4. Then print the program with correct form then the output will display.

## Program:
```
n = int(input())

A = []
for i in range(n):
    row = []
    for j in range(n + 1):
        row.append(float(input()))
    A.append(row)

for i in range(n):
    for j in range(i + 1, n):
        factor = A[j][i] / A[i][i]

        for k in range(i, n + 1):
            A[j][k] -= factor * A[i][k]

x = [0.0] * n

for i in range(n - 1, -1, -1):
    x[i] = (A[i][n] - sum(A[i][j] * x[j] for j in range(i + 1, n))) / A[i][i]

for i in range(n):
    print(f"X{i} = {x[i]:.2f}", end=" ")
```

## Output:

<img width="1243" height="682" alt="{2891AB89-F354-4D50-9560-21F5566E92EA}" src="https://github.com/user-attachments/assets/2d742f01-8fb7-4d8c-9e16-ea2613e84e3e" />


## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

