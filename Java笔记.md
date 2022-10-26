String.join(",", ArrayList);和"1,2,3".split(",");是一对  
### 字符串方法
```java
        String str = "test String. 1,2,3";
        str.matches(regex);
        str.toLowerCase();
        str.toUpperCase();
        str.charAt(0);
        str.substring(1);//截取1后面的字符串"est String. 1,2,3"
        str.substring(0,1);//截取0到1; "t"

        char c = Character.toUpperCase('a');
```
### 类型
Boolean,Integer,Byte,Short,Long,Float,Double,Character;
### Set 方法
```java
        Set<Integer> set = new HashSet<>();//TreeSet同理，但是TreeSet是红黑树，已经排好顺序
        set.clear();
        set.contains(3);
        set.add(2);
        set.remove(1);
        set.size();
```
```java
        //数组排序
        import java.util.Arrays;
        import java.util.Comparator;
        import java.util.Collections;
        int[] nums = new int[]{2,5,1,4,3};
        Arrays.sort(nums);
        
        ArrayList<Integer> array = new ArrayList<>();
        array.sort(Comparator.naturalOrder());//升序
        array.sort(Comparator.reverseOrder());//降序
        Collections.reverse(array);
```
      
### 读取文件
```java
        import java.util.Scanner;
        import java.io.File;
        File f = new File("D:\\Data.txt");
        Scanner sc = null;
        try{
            sc = new Scanner(f);
        }catch(Exception e){
        
        }
```
### 获取程序执行时间

```java
long begin = System.currentTimeMillis();
long end = System.currentTimeMillis();
```
