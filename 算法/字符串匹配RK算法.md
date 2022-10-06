rarbin karp
java字符串比较时注意不要用==，因为这个是比较两字符串的内存地址的会出错。用equals
把字符串进制转换
![image](https://user-images.githubusercontent.com/83968454/194349812-9b284ec3-59a1-4549-91e5-3bfc503e96e3.png)

## 题目
https://leetcode.cn/problems/find-the-index-of-the-first-occurrence-in-a-string/
![image](https://user-images.githubusercontent.com/83968454/194361434-70405eeb-811e-4e3d-a468-5623b80b05a7.png)

```java
class Solution {
    public int strStr(String haystack, String needle) {
        int needleLength = needle.length();
        if(needleLength==0)return 0;
        int BASE = 1000000;
        int haystackLength = haystack.length();
        //neeld hashCode
        int needleHashCode = 0;
        int power = 1;
        for(int i = 0;i < needleLength;i++){
            needleHashCode = (needleHashCode*31+needle.charAt(i))%BASE;
            power = (power*31)%BASE;
        }

        int HashCode = 0;
        for(int i =0;i<haystackLength;i++){
            HashCode = (HashCode*31+haystack.charAt(i))%BASE;
            //字符串不到needle长度时不用执行下面操作
            if(i<needleLength-1){
                continue;
            }
            
            if(i>=needleLength){
                HashCode = HashCode-(power*haystack.charAt(i-needleLength))%BASE;
                if(HashCode<0){
                    HashCode+=BASE;
                }
            }
            if(HashCode==needleHashCode){
                String subString = haystack.substring(i-needleLength+1,i+1);
                if(subString.equals(needle)){
                    return i-needleLength+1;
                }
            }
        }
        return -1;

        
    }
}
```

