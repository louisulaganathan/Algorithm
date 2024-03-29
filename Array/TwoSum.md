Problem:
========
Given an array of integers nums and an integer target, return indices of the two numbers such that they add up to target.
You may assume that each input would have exactly one solution, and you may not use the same element twice.
You can return the answer in any order.

Example 1:
```
Input: nums = [2,7,11,15], target = 9
Output: [0,1]
Explanation: Because nums[0] + nums[1] == 9, we return [0, 1].
```
Solution:
=========
```
public class Solution {
    public int[] TwoSum(int[] nums, int target) {
        int[] result= new int[2];
        for(var i=0;i<nums.Length;i++)
        {
            for(var j=i+1; j<nums.Length;j++)
            {
                if(nums[i] + nums[j] == target)
                {
                    result[0]=i;
                    result[1]=j;
                }
            }            
        }
        return result;
    }
}
```
Foreach, indexof () provided by framework and has O(n) complexity
we have to use only the language provided properties.

```
public class Solution {
    public int[] TwoSum(int[] nums, int target) {
        Dictionary<int, int>  m= new ();
        m.Add(nums[0],0);
        for(var i=1;i<nums.Length;i++)
        {
            var pairNum = target-nums[i];
            if(!m.ContainsKey(pairNum))
                m.TryAdd(nums[i], i);
            else
                return new []{m[pairNum],i};

        }
        return new[]{-1,-1};
    }
}
```

