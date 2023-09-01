# Data Structures and Algorithm{

Data Structures:
================
<br/>&emsp; Defined as particular way of storing and organizing data in our deveices to use the data effectively and efficiently.
<br/>&emsp; Main object of using DS is to reduce the time and space complexity.

<br/>Linkedlist<br/>
<br/>Matrix/Grid
<br/>Stack
<br/>Queue
<br/>Graph
<br/>Array
<br/>Hash
<br/>Heap
<br/>Tree
<br/>String


<br/>Algorithm:<br/>
------------------
&emsp; Defined as a process or set of welldefined instructions that are used to solve the group of poblems or perform specific calculations.
<br/>


<br/>Time complexity:
====================

<br/>&emsp;The time complexity of an algorithm quantifies the amount of time taken by an algorithm to run as a function interms of the length of the input.

<br/>Space Complexity:
=================
<br/>&emsp;The space complexity of an algorithm quantifies the amount of space taken by an algorithm to run as a function interms of the length of the input.

<br/>(1) A fixed part: It is independent of the input size. It includes memory for instructions (code), constants, variables, etc.

<br/>(2) A variable part: It is dependent on the input size. It includes memory for recursion stack, referenced variables, etc.

<br/>Asymphotic Notations
==========================
<br/>Big O O(1) - Best, <br/>O(logn) - Good ,<br/>O(n) - Fair,<br/>O(nlogn)-Bad, <br/>O(n!)/O(C<sup>n</sup>)/O(n<sup>c</sup>) - worst
<br/>Big Omega(Ω) 
<br/>Big theta(θ)


```
public class Solution
{
    public IList<string> FizzBuzz(int n)
    {
        string[] answer = new string[n];

        for (int i = 1; i <= n; i++)
        {
            bool isDivisibleBy3 = i % 3 == 0;
            bool isDivisibleBy5 = i % 5 == 0;

            var index = i - 1;

            if (isDivisibleBy3 && isDivisibleBy5)
            {
                answer[index] = "FizzBuzz";
            }
            else if (isDivisibleBy3)
            {
                answer[index] = "Fizz";
            }
            else if (isDivisibleBy5)
            {
                answer[index] = "Buzz";
            }
            else
            {
                answer[index] = i.ToString();
            }
        }

        return answer;
    }
}
```

Time complexity: O(n)
The main computational part of the function is the for loop that iterates over all integers from 1 to n. Inside the loop, the operations (modulus checks, assignments) are all constant time. Hence, the time complexity is determined by the number of iterations, which is n.

Space complexity: O(n)
The function uses a single string array answer of size n to store the results. There are also a few constant-sized variables (isDivisibleBy3, isDivisibleBy5, index). The space used by the constant-sized variables does not grow with n, so they do not contribute to the overall space complexity. Hence, the space complexity is determined by the size of the answer array.
