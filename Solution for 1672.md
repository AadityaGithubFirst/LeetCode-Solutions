# Solution for 1672

## Name: Richest Customer Wealth

### Category: Easy

1672 is a good beginner problem that you can look at when it comes to LeetCode. It is a good prerequisite that one can use to get a small introduction to python. 

#### Question

You are given an m x n integer grid accounts where accounts[i][j] is the amount of money the \[i​​​​​​​​​​​^th\]​​​​ customer has in the j^​​​​​​​​​​​th​​​​ bank. Return the wealth that the richest customer has.

A customer's wealth is the amount of money they have in all their bank accounts. The richest customer is the customer that has the maximum wealth.

#### Solution 1: Simplest Method

```{python} 
class Solution:
    def maximumWealth(self, accounts: List[List[int]]) -> int:
        richest = 0
        for account in accounts:
            richest = max(richest, sum(account))
        return richest
```
###### Runtime 🕙 and Memory Utilization 🔲

|Run Time (ms)|Memory Utilization (MB)|
|------------|------------|
|54|16.54|
###### Explanation of Solution
This was the first ever problem that I took on in LeetCode. My though process to approaching this problem was first understanding the Question
