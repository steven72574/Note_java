## 剑指 Offer II 078. 合并排序链表
![1](https://user-images.githubusercontent.com/83968454/192879378-1940afcf-8f2d-4057-88d6-c31978b2e82c.png)

https://leetcode.cn/problems/vvXgSW/

主要运用分治法

## 遇到的问题
看答案代码之后，抄写下来，运行时发现超时，对了好几遍答案，发现不了错的地方。最后发现是把字母l写成了1。吸取教训。

```Java
class Solution {
    public ListNode mergeKLists(ListNode[] lists) {
        
        return merge(lists,0,lists.length-1);

    }
    public ListNode merge(ListNode[] lists,int l,int r){
        if(l==r){
            //运行超时但是找不出原因，发现是把l写成了1！！<-----------------------------------------------------细节问题
            return lists[l];
        } 
        if(l>r){
            return null;
        }
        int mid = (l+r)>>1;
        return mergeTwoLists(merge(lists, l, mid), merge(lists, mid + 1, r));
    }
    
    public ListNode mergeTwoLists(ListNode list1,ListNode list2){
         if (list1 == null || list2 == null) {
            return list1 != null ? list1 : list2;
        }
        ListNode temp = new ListNode();
        ListNode head =temp;

        ListNode head1=list1,head2=list2;
        while(head1!=null&&head2!=null){
            if(head1.val<head2.val){
                temp.next = head1;
                head1=head1.next;
            }else{
                temp.next = head2;
                head2=head2.next;
            }
            temp = temp.next;
        }
        temp.next=(head1!=null?head1:head2);

        return head.next;
    }
}

```
