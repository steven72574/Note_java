## K数和
https://lintcode.com/problem/90
```java
public class Solution {
    /**
     * @param a: an integer array
     * @param k: a postive integer <= length(A)
     * @param target: an integer
     * @return: A list of lists of integer
     *          we will sort your return value in output
     */
     
    public List<List<Integer>> kSumII(int[] nums, int k, int target) {
        // write your code here
        List paths = new ArrayList();
        if(nums.length==0||k==0||target==0)return paths;

        List<Integer> path = new ArrayList<Integer>();
        dfs(path,paths,0,k,target,nums,0);
        return paths;
    }
    //递归定义：path是数字组合
    //paths 是装path的列表
    //index 当前是第几个数
    public void dfs(List<Integer> path,
                    List paths,int index,
                    int k,int target,
                    int[] nums,int sum){
        //递归出口
        //如果k数之和等于target，结束
        if(k==0&&sum==target){
            paths.add(new ArrayList<Integer>(path));
            return;
        }
        //如果和大于target，或index
        if(sum>target||k<=0){
            return;
        }
        //递归拆解
        for(int i=index;i<nums.length;i++){
            path.add(nums[i]);
            dfs(path,paths,i+1,k-1,target,nums,sum+nums[i]);
            path.remove(path.size()-1);
        }


    }
}
```
