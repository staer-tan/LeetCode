## Java程序设计基础内容

### 1. 数组及相关操作

示例为int型数组

（1）创建数组 int[] nums = new nums[5]

（2）排序数组 Arrays.sort(nums)

（3） 求数组长度 nums.length

-  ArrayList

说明：ArrayList相当于C++ 的vector，用于存储对象。

与数组不同，数组一旦创建，长度固定，但是ArrayList的长度是动态的，不受限制，可以存储任意多的对象。

但是只能存储对象，不能存储原生数据类型例如int。详细方法点击[[这里](https://blog.csdn.net/ftell/article/details/80826235)]

初始创建示例：ArrayList<String> cities = new ArrayList<String>(); //创建一个存储字符串的ArrayList对象
  
### 2. 字符串

- String

示例字符串为：String s

（1）字符串转字符数组（string -> char[]） s.toCharArray()

（2）字符串长度 s.length()（注意此时有括号，与数组不同）

（3）字符串分割  String[] words = s.split(" "); // 将字符串以空格形式分割，转为字符串（单词）数组

（4）翻转 单纯的String类似没有直接可用的翻转函数，可以将其转为StringBuilder形式调用函数进行翻转

- StringBuilder / StringBuffer

StringBuilder对象则代表一个字符序列可变的字符串，当一个StringBuffer被创建以后，

通过StringBuilder提供的append()、insert()、reverse()、setCharAt()、setLength()等方法可以改变这个字符串对象的字符序列。

StringBuilder与StringBuffer功能类似，区别在性能部分；详细见网络资料

- String与StringBuilder可相互转换

（1）StringBuilder -> String: StringBuilder.toString()

（2）String -> StringBuilder: StringBuilder(string)

### 3. 构建hash表

说明：由于Java本身的结构的丰富性，在构造hash表时可使用的方法非常丰富，如：HashMe, HashSet, HashTable等

但这些不同的结构建立的hash表，调用方法不一定一样，需要非常关注。

#### 3.1 用Set构建

（1）构建hash表 Set<Integer> nums = new HashSet<Integer>()

（2）查询hash表是否存在某个元素 nums.contains(num) 


