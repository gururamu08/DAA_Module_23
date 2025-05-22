# EX 5B Coin Change Problem
## DATE:16/5/25
## AIM:
To compute the fewest number of coins that we need to make up the amount given.


## Algorithm
1.Goal: Find the minimum number of coins needed to make a given amount using provided coin denominations.

2.DP Array: A dp array is used where dp[i] stores the minimum coins needed to make amount i.

3.Initialization: All values in dp are set to infinity, except dp[0] = 0 (zero coins needed to make amount 0).

4.Update Logic: For each coin, the algorithm checks all amounts from coin to amount and updates the minimum count.

5.Final Answer: If dp[amount] is still infinity, return 0 (not possible), else return dp[amount].
## Program:
```
Create a python function to compute the fewest number of coins that we need to make up the amount given
Developed by: GURUMOORTHI R
Register Number:  212222230042
```
```python
class Solution(object):
   def coinChange(self, coins, amount):
      ####################      Add your Code Here ###########
      dp=[float('inf')]*(amount+1)
      dp[0]=0
      for coin in coins:
          for i in range(coin,amount+1):
              dp[i]=min(dp[i],dp[i-coin]+1)
      return dp[amount] if dp[amount] != float('inf') else 0

      
      
ob1 = Solution()
n=int(input())
s=[]
amt=int(input())
for i in range(n):
    s.append(int(input()))


print(ob1.coinChange(s,amt))
```

## Output:
![image](https://github.com/user-attachments/assets/46c725cb-292c-43e2-9f60-91124a8a493d)



## Result:
Thus the program was executed successfully for finding the minimum number of coins required to make amount.
