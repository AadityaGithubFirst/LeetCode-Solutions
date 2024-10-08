# Solution for 1672

## Name: Richest Customer Wealth

### Category: Easy

1672 is a good beginner problem that you can look at when it comes to LeetCode. It is a good prerequisite that one can use to get a small introduction to python. 

#### Solution 1: Simplest Method

```{python} 
class Solution:
    def maximumWealth(self, accounts: List[List[int]]) -> int:
        richest = 0
        for account in accounts:
            richest = max(richest, sum(account))
        return richest
```
###### Runtime and Memory Utilization

|Memory Utilization (MB)|Run Time (ms)|
|------------|------------|
|16.54|54|
###### Explanation of Solution
