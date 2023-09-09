
Given an integer array nums, return true if any value appears at least twice in the array, and return false if every element is distinct.

 
Problem:
========
Example 1:

Input: nums = [1,2,3,1]
Output: true
Example 2:

Input: nums = [1,2,3,4]
Output: false
Example 3:

Input: nums = [1,1,1,3,3,4,3,2,4,2]
Output: true

 Solution:
 ==========
 
```
public class Solution {
    public bool ContainsDuplicate(int[] nums) {
        HashSet<int> set = new HashSet<int>(nums); //set is collection of elements with no duplicate element it ignore the duplicates during casting.
        foreach(var num in set)
        Console.WriteLine(num.ToString());
        return nums.Length != set.Count;
    }
}
```
