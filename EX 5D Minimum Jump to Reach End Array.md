# EX 5D Minimum Jump to Reach End Array
## DATE:16/5/25
## AIM:
To write a python program for finding the minimum number of jumps needed to reach end of the array using Dynamic Programming.


## Algorithm
1.Goal: Find the minimum number of jumps needed to reach the end of the array from the start.

2.Base Cases:

If start equals end (l == h), no jumps are needed.

If the current value is 0, you cannot move further (return ∞).

3.Recursive Check: Try all reachable positions from the current index and calculate the minimum jumps.

4.Important Condition: Only consider jumps within the allowed range: i < l + 1 + arr[l].

5.Result: Returns the minimum jumps to reach the end, or inf if it's not possible.


## Program:
```
To implement the program to finding the minimum number of jumps needed to reach end of the array.
Developed by: GURUMOORTHI R
Register Number:  212222230042
```
```python
def minJumps(arr, l, h):
    ###########   Add your code here ###########
    if l==h:
        return 0
    if arr[l]==0:
        return float('inf')
    m = float('inf')    
    for i in range(l+1,h+1):
        if i < l+1+arr[l]:
            j = minJumps(arr,i,h)
        if j != float('inf') and j+1<m:
            m =j +1
    return m        
    
arr = []
n = int(input()) 
for i in range(n):
    arr.append(int(input()))
print('Minimum number of jumps to reach','end is', minJumps(arr, 0, n-1))

```

## Output:

![image](https://github.com/user-attachments/assets/680da83a-0978-44b6-aa96-a5f91bf9f8e7)


## Result:
Thus the program was executed successfully for finding the minimum number of jumps to reach end.
