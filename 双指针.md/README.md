![WeChat Screenshot_20221013111716](https://user-images.githubusercontent.com/83968454/195556584-30252fe1-df87-47d8-b873-86afb0b3cee2.png)
### 题目
![image](https://user-images.githubusercontent.com/83968454/195603395-533d5c06-dc85-4fcc-bc9d-1ee69d7ab7b3.png)  
```java
public class Solution {
    /**
     * @param nums: an array of integers
     * @return: nothing
     */
    public void partitionArray(int[] nums) {
        if(nums.length == 0) return;
        // write your code here
        PartitionEvenOdd(nums);
    }
    public void PartitionEvenOdd(int[] nums){
        int left = 0;
        int right = nums.length - 1;
        while(left<=right){
            while(left <= right && nums[left] % 2 == 1) left++;
            while(left<=right && nums[right] % 2 ==0) right--;
            if(left<=right){
                int temp = nums[right];
                nums[right] = nums[left];
                nums[left] = temp;
                left++;
                right--;
            }
        }
    }
}
```
