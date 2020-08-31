# 53.-Maximum-Subarray

```C#
   public class Solution {
    public int MaxSubArray(int[] nums) {
         
            int globalSum = int.MinValue;
            int sum = 0; 
            foreach(var num in nums)
            {
                sum = num > (num + sum) ? num : (num + sum);
                globalSum = sum > globalSum ? sum : globalSum;
            }

            return globalSum;
    }
}
```
