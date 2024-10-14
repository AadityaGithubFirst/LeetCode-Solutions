# Solution for 1342
## Name: Number of Steps to reduce a number to zero
### Categroy: Easy

This is another question that is pretty easy to do and is a good beginner question for people to solve. 

#### Quesion
Given an integer num, return the number of steps to reduce it to zero.

In one step, if the current number is even, you have to divide it by 2, otherwise, you have to subtract 1 from it.

#### Solution 1:

```{python}
class Solution:
    def numberOfSteps(self, num: int) -> int:
        counter = 0
        while(num>0):
            counter +=1
            if(num%2):
                num-=1
            else:
                num/=2
        return counter
            
```