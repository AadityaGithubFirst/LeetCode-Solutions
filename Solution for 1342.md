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
###### Runtime 🕙 and Memory Utilization 🔲

|Run Time (ms)|Memory Utilization (MB)|
|------------|------------|
|39|16.58|

###### Explanation of the solution

In this method the first thing I did was that I initialized a counter variable. 
The second thing that I did was that I added a while loop which would break once the number is less than or equal to zero (or run only while the number is greater than zero). The first step that I did was that I added 1 to the counter variable because that means one step by default is going to happen. I then checked whether the number is odd. If the number is odd then I subtract one. If the number is even I divide it by two. After the while loop is finished I return the value of the counter variable as that is where my number of steps has been stored. 

#### Solution 2: 

```{python}
class Solution:
    def numberOfSteps(self, num: int) -> int:
        return bin(num).count('1') + len(bin(num)) - 3
```
###### Runtime 🕙 and Memory Utilization 🔲

|Run Time (ms)|Memory Utilization (MB)|
|------------|------------|
|33|16.46|

###### Explanation of the solution

I did this as a single line solution. The first thing that I do is that I convert the numbers into their binary format. and I counted all the times a one came up this is because in binary the way that it is represented is showing the number of times 2 has to be multipled by the zeros and the number of times one is added by the ones. I then added the length of the binary version of the number and subtracted three. The reason why I subtracted three is because of the fact that most binary numbers start with 0b and on top of that we don not account for the last digit. 