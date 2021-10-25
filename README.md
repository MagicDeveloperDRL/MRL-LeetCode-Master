# MRL-LeetCode-Master
 该项目记录作者刷LeetCode的笔记与代码。

[TOC]

## 一、C++基础知识

### 1、容器与容器适配器

[【C++】STL中的容器与容器适配器](./00C++/【C++】STL中的容器与容器适配器.md)

## 二、经典方法分类

### 1、数据结构类

| **LeetCode题目** | **相关题目类型**         | 关键点                                                 | **相关链接**                                                 |
| ---------------- | ------------------------ | ------------------------------------------------------ | ------------------------------------------------------------ |
| 707              | 设计链表（中等难度）     |                                                        | https://leetcode-cn.com/problems/design-linked-list/         |
| 232              | 用栈实现队列（简单难度） | 用两个栈实现，进栈和出栈，出队时从进栈移入出栈         | https://leetcode-cn.com/problems/implement-queue-using-stacks/ |
| 225              | 用队列实现栈（简单难度） | 可用一个队列实现，出栈时将最后一个元素前的元素加入队尾 | https://leetcode-cn.com/problems/implement-stack-using-queues/ |

### 2、二分查找类

从有序的无重复元素序列中快速查找某个元素，常见于数组问题

| **LeetCode题目** | **相关题目类型**                                       | 关键点 | **相关链接**                                                 |
| ---------------- | ------------------------------------------------------ | ------ | ------------------------------------------------------------ |
| 704              | 二分查找（简单难度）                                   |        | https://leetcode-cn.com/problems/binary-search/              |
| 35               | 搜索插入位置（简单难度）                               |        | https://leetcode-cn.com/problems/search-insert-position/     |
| 69               | x的平方根（简单难度）                                  |        | https://leetcode-cn.com/problems/sqrtx/                      |
| 367              | 有效的完全平方数（简单难度）                           |        | https://leetcode-cn.com/problems/valid-perfect-square/       |
| 34               | 在排序数组中查找元素的第一个和最后一个位置（中等难度） |        | https://leetcode-cn.com/problems/find-first-and-last-position-of-element-in-sorted-array/ |

### 3、双指针法类（13道题目）

通过快慢指针化双重循环为单重循环问题，常见于数组、链表、字符串等操作

| **LeetCode题目** | **相关题目类型**                    | 题目简述 | 关键点                                                       | **相关链接**                                                 |
| ---------------- | ----------------------------------- | -------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
|                  |                                     |          |                                                              |                                                              |
| 206              | 反转链表（简单难度）                |          | pre和cur节点边遍历边反转                                     | https://leetcode-cn.com/problems/reverse-linked-list/        |
| 92               | 反转链表II（中等难度）              |          |                                                              | https://leetcode-cn.com/problems/reverse-linked-list-ii/     |
| 234              | 回文链表（简单难度）                |          | 根据快慢指针找到中点；反转后半段；比较前后两端节点值         | https://leetcode-cn.com/problems/palindrome-linked-list/     |
| 19               | 删除链表的倒数第N个节点（中等难度） |          | 让快指针先走N步，让后判断此时快指针是否存在；存在则快慢指针同时走 | https://leetcode-cn.com/problems/remove-nth-node-from-end-of-list/ |
| 141              | 环形链表（简单难度）                |          | 快慢指针，若指针相遇则判断有环                               | https://leetcode-cn.com/problems/linked-list-cycle/          |
| 142              | 环形链表II（中等难度）              |          | 指针环内相遇后，两个节点分别从head和相遇点出发，再次相遇点即是环入口 | https://leetcode-cn.com/problems/linked-list-cycle-ii/       |
| 面试题02.07.     | 链表相交（简单难度）                |          | 长链表的遍历节点先多走和短链表的长度差个节点，然后同时遍历两个节点比较是否存在相同节点 | https://leetcode-cn.com/problems/intersection-of-two-linked-lists-lcci/ |

### 4、哈希频率类

| **LeetCode题目** | **相关题目类型**                       | 关键点                                                       | **相关链接**                                                 |
| ---------------- | -------------------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| 169              | 多数元素（中等难度）                   |                                                              | https://leetcode-cn.com/problems/majority-element/           |
| 242              | 有效的字母异位词（简单难度）           | 统计字母频率，或者排序，API的使用，26个数组值的定义          | https://leetcode-cn.com/problems/valid-anagram/              |
| 383              | 赎金信（简单难度）                     | 统计字母串的先后顺序                                         | https://leetcode-cn.com/problems/ransom-note/                |
| 49               | 字母异位词分组（中等难度）             | 将排序后的字符串作为key去存取；熟悉对哈希表的遍历操作        | https://leetcode-cn.com/problems/group-anagrams/             |
| 438              | 找到字符串中所有字母异位词（中等难度） | 滑动窗口法，滑动窗口和目标字符串大小相同，统计滑动窗口中的字母频率，不断和目标字符串的字母频率比较 | https://leetcode-cn.com/problems/find-all-anagrams-in-a-string/ |
| 1002             | 查找常用字符（简单难度）               | 多个字符串中对应的字母频次最小值就是常用字符                 | https://leetcode-cn.com/problems/find-common-characters/     |
| 349              | 两个数组的交集（简单难度）             | 方法一：使用map 容器统计数字频率；方法二：使用unordered_set 容器，在该容器中查找是否存在另一个数组的元素 | https://leetcode-cn.com/problems/intersection-of-two-arrays/ |
| 350              | 两个数组的交集II（简单难度）           | 使用map 容器统计数字频率                                     | https://leetcode-cn.com/problems/intersection-of-two-arrays-II/ |
| 202              | 快乐数（简单难度）                     | 数值各个位上的单数操作；如果sum**重复出现**则说明要无限循环； | https://leetcode-cn.com/problems/happy-number/               |
| 1                | 两数之和（简单难度）                   | 暴力解法；两数之和等价于差是否在map中重复出现                | https://leetcode-cn.com/problems/two-sum/                    |
| 15               | 三数之和（中等难度）                   | 1.将数组排序 2.定义三个指针，i，j，k。遍历i，那么这个问题就可以转化为在i之后的数组中寻找nums[j]+nums[k]=-nums[i]这个问题，也就将三数之和问题转变为二数之和---（可以使用双指针） | https://leetcode-cn.com/problems/3sum/                       |
| 18               | 四数之和（中等难度）                   | 和三数之和差不多                                             | https://leetcode-cn.com/problems/4sum/                       |
| 454              | 四数相加II（中等难度）                 | 和两数之和差不多，从四个不同数组中查找两数之和               | https://leetcode-cn.com/problems/4sum-ii/                    |
| 344              | 反转字符串（简单难度）                 | 前后指针向内走                                               | https://leetcode-cn.com/problems/reverse-string/             |
| 541              | 反转字符串II（简单难度）               | 每间隔2k个进行循环                                           | https://leetcode-cn.com/problems/reverse-string-ii/          |
| 剑指offer05      | 替换空格（简单难度）                   | string对象可以直接+；                                        | https://leetcode-cn.com/problems/ti-huan-kong-ge-lcof/       |
| 剑指Offer58-II   | 左旋转字符串（简单难度）               | 反转前n；反转后n；整体反转                                   | https://leetcode-cn.com/problems/zuo-xuan-zhuan-zi-fu-chuan-lcof/ |
| 151              | 翻转字符串里的单词（中等难度）         | 移除多余空格；反转整个字符串；将每个单词反转                 | https://leetcode-cn.com/problems/reverse-words-in-a-string/  |
| 844              | 比较含退格的字符串（简单难度）         | O(n)解法借助string对象；O(1)解法比较难，双指针               | https://leetcode-cn.com/problems/backspace-string-compare/   |
| 347              | 前 K 个高频元素（中等难度）            | 使用unordered_map统计频率；使用优先级队列priority_queue对频率排序；使用vector存储前k个高频元素 | https://leetcode-cn.com/problems/top-k-frequent-elements/    |

### 5、字符串匹配

| **LeetCode题目** | **相关题目类型**                         | 关键点                                                       | **相关链接**                                                 |
| ---------------- | ---------------------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| 28               | 实现strSrt()（简单难度）                 | KMP算法和暴力解法                                            | https://leetcode-cn.com/problems/implement-strstr/           |
| 459              | 重复的子字符串（简单难度）               | KMP算法的前缀表                                              | https://leetcode-cn.com/problems/repeated-substring-pattern/ |
| 20               | 有效的括号（简单难度）                   | 对称结构，遍历字符串，若是左括号，则将其对称结构入栈，若是右括号则判断是否匹配 | https://leetcode-cn.com/problems/valid-parentheses/          |
| 1047             | 删除字符串中的所有相邻重复项（简单难度） | 字符串对对消；将当前字符放入栈如果栈顶元素和下一个字符相等则出栈，否则入栈 | https://leetcode-cn.com/problems/remove-all-adjacent-duplicates-in-string/ |
| 150              | 逆波兰表达式求值（中等难度）             | 先进后出的顺序，注意减法和除法的两个数的顺序                 | https://leetcode-cn.com/problems/evaluate-reverse-polish-notation/ |

### 6、滑动窗口类

通过不断地调节子序列的起始位置和终止位置，从而得出我们要想的结果

| **LeetCode题目** | **相关题目类型**             | **相关链接**                                                |
| ---------------- | ---------------------------- | ----------------------------------------------------------- |
| 209              | 长度最小的子数组（中等难度） | https://leetcode-cn.com/problems/minimum-size-subarray-sum/ |
| 904              | 水果成篮（中等难度）         | https://leetcode-cn.com/problems/fruit-into-baskets/        |
| 76               | 最小覆盖子串（困难难度）     |                                                             |
| 239              | 滑动窗口最大值（困难难度）   | 滑动窗口与单调队列                                          |

### 7、模拟行为类

| **LeetCode题目** | **相关题目类型**           | **相关链接**                                                 |
| ---------------- | -------------------------- | ------------------------------------------------------------ |
| 59               | 螺旋矩阵II（中等难度）     | https://leetcode-cn.com/problems/spiral-matrix-ii/           |
| 54               | 螺旋矩阵（中等难度）       | https://leetcode-cn.com/problems/spiral-matrix/              |
| 剑指offer29      | 顺时针打印矩阵（简单难度） | https://leetcode-cn.com/problems/shun-shi-zhen-da-yin-ju-zhen-lcof/ |

## 三、经典题目分类

- [x] ### 【数组】15道

[数组目录](./01数组/00数组目录.md)

- [x] ### 【链表】9道

[链表目录](./02链表/00链表目录.md)

- [x] ### 【哈希表】12道

[哈希表目录](./03哈希表/00哈希表目录.md)

- [x] ### 【字符串】8道

[字符串目录](./04字符串/00字符串目录.md)

- [x] ### 【栈与队列】7道

[栈与队列目录](./05栈与队列/00栈与队列目录.md)

- [x] ### 【二叉树】42道

[二叉树与二叉搜索树目录](./06二叉树/00二叉树与二叉搜索树目录.md)

- [ ] ### 【回溯算法】15道

[回溯算法目录](./07回溯算法/00回溯算法目录.md)

- [ ] ### 【贪心算法】18道

[回溯算法目录](./07回溯算法/00回溯算法目录.md)

- [ ] ### 【动态规划】40道

[回溯算法目录](./07回溯算法/00回溯算法目录.md)
