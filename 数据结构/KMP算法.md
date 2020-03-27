## 参考网址
https://www.cnblogs.com/luomeng/p/10587492.html

## 思路

问题介绍，文本串和模式串找到匹配相同的开始位置。

例如：

文本串：ssdfgasdbababa

模式串：ababa

KMP算法特点：如果用暴力方法解决的话就会有大量的回溯，每次只移动一位，若是不匹配，移动到下一位接着判断，浪费了大量的时间。

所以，kmp方法算法就利用之前判断过信息，通过一个next数组，保存模式串中前后最长公共子序列的长度。

每次回溯时，通过next数组找到，前面匹配过的位置，省去了大量的计算时间。kmp算法的核心时间复杂度就是O（m+n）

## 算法技巧

其实kmp算法的核心代码就几行而已

在匹配阶段，若是模式串和文本串相同，那就继续匹配下一位，若是不相同，就去找next数组记录的位置，继续匹配。

这个也是kmp算法和普通暴力算法的主要区别，暴力是从头开始匹配，而kmp通过next数组，发现前面可以跳过大量重复计算的东西。

下面讲一下，next数组的计算方法：next数组的计算主要跟模式串有关，与文本串并没有关系，因为，模式串前后公共最长子序列。这样才会让我们跳过大量的重复计算

next数组的主要实现方法有很多，就是要找到前后最长公共子序列的长度 比如：

模式串：ababa：

模式串的各个子串： 前缀： 后缀： 最大公共元素长度（前后缀长度至少为1）

a 0
ab a b 0
aba a ab a ba 1
abab a ab aba b ab bab 2
ababa a ab aba abab a ba aba baba 3
如上图，next数组中的元素就是 0 0 1 2 3;

## 代码
```java
/**
 * KMP算法
 */
public class KMP {
    public static int kmp(String str, String dest,int[] next){//str文本串  dest 模式串
        for(int i = 0, j = 0; i < str.length(); i++){
            while(j > 0 && str.charAt(i) != dest.charAt(j)){
                j = next[j - 1];
            }
            if(str.charAt(i) == dest.charAt(j)){
                j++;
            }
            if(j == dest.length()){
                return i-j+1;
            }
        }
        return 0;
    }
    public static int[] kmpnext(String dest){
        int[] next = new int[dest.length()];
        next[0] = 0;
        for(int i = 1,j = 0; i < dest.length(); i++){
            while(j > 0 && dest.charAt(j) != dest.charAt(i)){
                j = next[j - 1];
            }
            if(dest.charAt(i) == dest.charAt(j)){
                j++;
            }
            next[i] = j;
        }
        return next;
    }
    public static void main(String[] args){
        String a = "ababa";
        String b = "ssdfgasdbababa";
        int[] next = kmpnext(a);
        int res = kmp(b, a,next);
        System.out.println(res);
        for(int i = 0; i < next.length; i++){
            System.out.println(next[i]);            
        }
        System.out.println(next.length);
    }
}

```
