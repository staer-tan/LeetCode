## Java程序设计基础内容

### 1. 数组及相关操作

示例为int型数组

（1）创建数组 int[] nums = new nums[5]

（2）排序数组 Arrays.sort(nums)

（3） 求数组长度 nums.length

### 2. 字符串

示例字符串为：String s

（1）字符串转字符数组（string -> char[]） s.toCharArray()

（2）字符串长度 s.length()（注意此时有括号，与数组不同）

### 3. 构建hash表

说明：由于Java本身的结构的丰富性，在构造hash表时可使用的方法非常丰富，如：HashMe, HashSet, HashTable等

但这些不同的结构建立的hash表，调用方法不一定一样，需要非常关注。

#### 3.1 用Set构建

（1）构建hash表 Set<Integer> nums = new HashSet<Integer>()

（2）查询hash表是否存在某个元素 nums.contains(num) 

