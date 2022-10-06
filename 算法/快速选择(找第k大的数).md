# 快速选择
方便用于找中位数，找第k大的数，好处是比先排序再找时间复杂度来的要低

https://leetcode.cn/problems/xx4gT2/  
https://leetcode.cn/problems/kth-largest-element-in-an-array/  

### 对比快速排序

主要思想是快速排序的思想

```java
class Solution {
    public int findKthLargest(int[] nums, int k) {
        return QuickSelect(nums,0,nums.length-1,k);
    }

    public int QuickSelect(int[]nums,int start,int end,int k){
        if(start==end)return nums[start];

        int left = start,right=end;
        int pivot = nums[(left+right)/2];
        //降序排序
        while(left<=right){
            while(left<=right&&nums[left]>pivot)left++;
            while(left<=right&&nums[right]<pivot)right--;
            if(left<=right){
                int temp = nums[left];
                nums[left]=nums[right];
                nums[right]=temp;
                left++;
                right--;
            }
        }
        //循环结束后right<left
        //且right和left直接可能还有一个元素
        
        //看k落在哪个区间
        if(start+k-1<=right){
            return QuickSelect(nums,start,right,k);
        }
        if(start+k-1>=left){
            //注意重新计算k与left的距离
            return QuickSelect(nums,left,end,k-(left-start));
        }

        return nums[right+1];
    }
}
```
time O(n)
space O(logn),栈空间,n为数组元素
