# Algorithm

Time complexity: O(n)
The main computational part of the function is the for loop that iterates over all integers from 1 to n. Inside the loop, the operations (modulus checks, assignments) are all constant time. Hence, the time complexity is determined by the number of iterations, which is n.

Space complexity: O(n)
The function uses a single string array answer of size n to store the results. There are also a few constant-sized variables (isDivisibleBy3, isDivisibleBy5, index). The space used by the constant-sized variables does not grow with n, so they do not contribute to the overall space complexity. Hence, the space complexity is determined by the size of the answer array.
