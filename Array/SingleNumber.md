**Single Number**
====================

Given a non-empty array of integers nums, every element appears twice except for one. Find that single one.

You must implement a solution with a linear runtime complexity and use only constant extra space.

 
```
Example 1:

Input: nums = [2,2,1]
Output: 1
Example 2:

Input: nums = [4,1,2,1,2]
Output: 4
Example 3:

Input: nums = [1]
Output: 1

```

^ = XOR operation
a^a = 0
1^1 = 0 
0^0 = 0
0^1 = 1

4,1,2,1,2
100,001,010,001,010  Xor on binary digit will cancel each other if it is same digits and yield 0 as output 0^a = a thats how 0^4  = 4
4,1,2,1,2,2 =>4^2 will be the answer

Solution
==========

```
public class Solution {
    public int SingleNumber(int[] nums) {
       var result = 0;
        for(var i=0; i<nums.Length; i++)
        {           
            result = result ^ nums[i];
        }
        return result;
    }
}
```

111
