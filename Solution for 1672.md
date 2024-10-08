# Solution for 1672

## Name: Richest Customer Wealth

### Category: Easy

1672 is a good beginner problem that you can look at when it comes to LeetCode. It is a good prerequisite that one can use to get a small introduction to python. 

#### Question

You are given an m x n integer grid accounts where accounts[i][j] is the amount of money the $$i^{th}$$ customer has in the $$j^{th}$$​​​​​​​ bank. Return the wealth that the richest customer has.

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
This was the first ever problem that I took on in LeetCode. My though process to approaching this problem was first understanding the question. The question wants us to be able to find the array that has the maximum sum.
from the define part of the function I can see that the value of accounts is a nested list and the output of the given function has to be an integer. The next step that I did was that I set a datapoint called richest and gave it a default value of 0 because the minimum value that can be kept inside a bank is a positive value.
The next line I iterated using a for loop throught the accounts. The next step that I do is that I compare whether the current value of richest is the most or whether the sum of the current list is the highest.
Finally I returned the maximum value that I obtained.

The time complexity of this code is $$\Omega(n^2)$$

#### Solution 2: A medium method (Commonly used method)
```{python}
class Solution:
    def maximumWealth(self, accounts: List[List[int]]) -> int:
        return sorted([sum(i) for i in accounts])[-1]
```
###### Runtime 🕙 and Memory Utilization 🔲

|Run Time (ms)|Memory Utilization (MB)|
|------------|------------|
|54|16.64|

###### Explanation of the Solution
This was the solution that I created when I tried solving it after having almost three years of experience in python. As it can be seen that this is just a single line solution. Let us look inside the brackets from the brackets it can be seen that I iterate through the accounts finding the sum of each account and put it into a list. After creating the list I use the sorted command that returns the list in a sorted manner. I then take out the last element this is because of the fact that the list that has been made is a sorted list in ascending order so the last element is the maximum value.

The time complexity of this given code is $$\Omega(m*n + m\log(m))$$.