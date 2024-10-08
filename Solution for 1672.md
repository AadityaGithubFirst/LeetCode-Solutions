# Solution for 1672

## Name: Richest Customer Wealth

### Category: Easy

1672 is a good beginner problem that you can look at when it comes to LeetCode. It is a good prerequisite that one can use to get a small introduction to python. 
```{python} 
class Solution:
    def maximumWealth(self, accounts: List[List[int]]) -> int:
        richest = 0
        for account in accounts:
            richest = max(richest, sum(account))
        return richest
```
