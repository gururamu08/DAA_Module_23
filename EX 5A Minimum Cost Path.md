# EX 5A Minimum Cost Path
## DATE:16/5/25
## AIM:
To write a Python program using A Naive recursive implementation of Minimum Cost Path Problem.




## Algorithm
1.Goal: The program calculates the minimum cost to reach cell (R-1, C-1) from (0, 0) in a grid.

2.Allowed Moves: You can move right, down, or diagonally down-right from each cell.

3.Recursive Function: The minCost function uses recursion to explore all valid paths and picks the one with the lowest cost.

4.Base Case: If you reach (0, 0), it returns the cost at that cell; if you go out of bounds, it returns a very large number.

5.Custom Min Function: A helper min(x, y, z) function returns the smallest of three values to assist in choosing the optimal path.
## Program:
```
/*
A program to implement to find the Minimum Cost Path Problem using a  Naive recursive Approach.
Developed by: GURUMOORTHI R
Register Number:  212222230042
```
```python
R = int(input())
C = int(input())
import sys
def minCost(cost, m, n):
    if (m<0 or n<0):
        return sys.maxsize
    elif(m==0 and n==0):
        return cost[m][n]
    else:
        return cost[m][n] + min(minCost(cost,m-1,n-1),minCost(cost,m-1,n),minCost(cost,m,n-1))
        
def min(x, y, z):
    if (x < y):
        return x if (x < z) else z
    else:
        return y if (y < z) else z
cost= [ [1, 2, 3],
        [4, 8, 2],
        [1, 5, 3] ]
print(minCost(cost, R-1, C-1))
```

## Output:


![image](https://github.com/user-attachments/assets/3e5da99e-4fc9-4c8f-baf0-5d4613f72948)

## Result:
Thus the above program was executed successfully for finding the minimum cost.
