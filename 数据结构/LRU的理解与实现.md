## 问题地址
https://leetcode-cn.com/problems/lru-cache-lcci/

## 思路

LRU总体规则是这样的，最近使用的放在前边（最左边），最近没用的放到后边（最右边）（模型实现）。来了一个新的数，如果内存满了，把旧的数淘汰掉，那位了方便移动数据，我们肯定不能考虑用数组，呼之欲出，就是使用链表了。

解决方案：双向链表（处理新老关系）+哈希（查询在不在），分析如下

底层应该用链表，按照数据的新旧程度来排列，旧的在左边，新的在右边，新来一个加到尾部，删除是删头,除了这两个操作，还有就是把一个数据从中间拿出来放尾巴上（这个数组就很难做到）

这里还有一个需求，就是要知道这个数据有没有存在于链表中，如果不在链表中，加到尾巴即可，如果已经在链表中，就只要更细数据的位置,如何查找这个数据在不在呢，这就用哈希表。

考虑删除操作，要把当前节点的前一个节点的指针的改变，获取它前一个节点，方便的数据结构就是 双向链表

所以数据结构就是底层是双向链表（自己构建）+ HashMap看面试官要求是啥了。

写的时候为了方便，我们肯定是把最近使用的放尾巴就好了，删除的时候就删除头。

## 代码
```java
/**
 * LRU
 */
class LRUCache {
     // 定义一个双向链表
    private class ListNode{
        int key;
        int val;
        ListNode pre;
        ListNode next;

        public ListNode(int key, int val){
            this.key = key;
            this.val = val;

            pre = null;
            next = null;
        }
    }
    
    // LRU的容量
    private int capacity;
    // 用来快速定位节点和记录节点数量
    private HashMap<Integer, ListNode> map;
    // 虚拟头节点
    private ListNode head;
    // 虚拟尾节点
    private ListNode tail;

    public LRUCache(int capacity) {
        this.capacity = capacity;
        map = new HashMap<>();
        head = new ListNode(-1, -1);
        tail = new ListNode(-1, -1);
        
        // 建立虚拟头和虚拟尾节点的关系
        head.next = tail;
        tail.pre = head;
    }
    
    public int get(int key) {
        // 如果map中没有这个key,证明没有命中缓存,直接返回-1即可
        if(!map.containsKey(key)){
            return -1;
        }
        
        ListNode node = map.get(key);
        
        node.pre.next = node.next;
        node.next.pre = node.pre;
        // 将命中缓存的节点移到链表的最末尾（虚拟尾节点前面）
        moveToTail(node);

        return node.val;
    }
    
    public void put(int key, int value) {
      //直接调用这边的get方法，如果存在，它会在get内部被移动到尾巴，不用再移动一遍,直接修改值即可
        if(get(key) != -1){
            map.get(key).val = value;
            return;
        }
        
        // 如果map不存在的话,需要在map和链表的最末尾（虚拟尾节点前面）新增这个节点,
        // 并且检查现在缓存超没超容量,如果超了的话需要删除链表的最前面的节点(虚拟头节点的后面)
        ListNode node = new ListNode(key, value);
        map.put(key, node);
        moveToTail(node);

        if(map.size() > capacity){
            map.remove(head.next.key);
            head.next = head.next.next;
            head.next.pre = head;
        }
    }

    public void moveToTail(ListNode node){
        node.pre = tail.pre;
        tail.pre = node;
        node.pre.next = node;
        node.next = tail;
    }
}

/**
 * Your LRUCache object will be instantiated and called as such:
 * LRUCache obj = new LRUCache(capacity);
 * int param_1 = obj.get(key);
 * obj.put(key,value);
 */
```


