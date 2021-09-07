# 【C++】deque
[TOC]

deque也是一个可变长的动态数组，支持随机访问迭代器，所有适用于 vector 的操作都适用于 deque。要使用 deque，需要包含如下头文件和命名空间。

```c++
#include <deque>
using namespace std;
```

## 一、常用函数

### 1、初始化方式

| 使用需求                                                     | 使用样例                              |
| ------------------------------------------------------------ | ------------------------------------- |
| 构建一个空的deque                                            | deque<int> A;                         |
| 构建一个含有n个元素的deque                                   | deque<int> A(26);                     |
| 构建一个含有n个元素、每个元素都是val的deque                  | deque<int> A(26, 0);                  |
| 使用某个deque的区间[first, last)构造一个新的deque，用来裁剪deque | deque<int> B(A.begin(), A.begin()+5); |
| 构建一个含有指定元素的deque                                  | deque<int> A = {2, 3, 4};             |

### 2、容器大小

| 成员函数     | 函数功能                   |
| ------------ | -------------------------- |
| int size()   | 返回容器对象中元素的个数。 |
| bool empty() | 判断容器对象是否为空       |

### 3、添加操作

| 成员函数                                                    | 函数功能                                                     |
| ----------------------------------------------------------- | ------------------------------------------------------------ |
| void push_back( const T & val)                              | 将 val 添加到容器末尾                                        |
| iterator insert(iterator i, const T & val)                  | 将 val 插入迭代器 i 指向的位置，返回 i                       |
| iterator insert( iterator i, iterator first, iterator last) | 将其他容器上的区间 [first, last) 中的元素插入迭代器 i 指向的位置 |

### 4、删除操作

| 成员函数                                     | 函数功能                                                    |
| -------------------------------------------- | ----------------------------------------------------------- |
| void clear()                                 | 删除所有元素                                                |
| void pop_back()                              | 删除容器末尾的元素                                          |
| iterator erase(iterator i)                   | 删除迭代器 i 指向的元素，返回值是被删元素后面的元素的迭代器 |
| terator erase(iterator first, iterator last) | 删除容器中的区间 [first, last)                              |

### 5、获取操作

| 成员函数    | 函数功能                     |
| ----------- | ---------------------------- |
| T & front() | 返回容器中第一个元素的引用   |
| T & back()  | 返回容器中最后一个元素的引用 |

## 二、常见操作

### 1、遍历操作

#### （1）带下标遍历元素

```c++
for (int i =0; i<A.size(); i++) {  
    cout << A[i] << " ";  
}
```

#### （2）直接遍历元素

```c++
//方式一
for (int x:A) {  
    cout <<x<< " ";  
}
//方式二
for (auto x:A) {  
    cout <<x<< " ";  
}
```

#### （3）用迭代器遍历

```c++
//方式一：正向迭代器(从前向后遍历)
for (list<int>::iterator i = v.begin(); i != v.end(); i++) {  //用迭代器遍历容器
    cout << *i << " ";  //*i 就是迭代器i指向的元素
}
//方式二：正向迭代器(从前向后遍历)
for (auto i = v.begin(); i != v.end(); i++) {  //用迭代器遍历容器
    cout << *i << " ";  //*i 就是迭代器i指向的元素
}
//方式一：反向迭代器(从后向前遍历)
for (list<int>::reverse_iterator i = v.rbegin(); i != v.rend(); i++) {  
    cout << *i << " ";  //*i 就是迭代器i指向的元素
}
//方式二：反向迭代器(从后向前遍历)
for (auto i = v.rbegin(); i != v.rend(); i++) {  //用迭代器遍历容器
    cout << *i << " ";  //*i 就是迭代器i指向的元素
}
```

### 2、排序操作

```c++
sort(A.begin(), A.end()); // 将A从小到大排序
```

这里的sort来自STL中的算法模板

### 3、反向操作

```c++
reverse(A.begin(), A.end();  //将A前后颠倒
```

这里的reverse来自STL中的算法模板

## 三、内存特点

### 1、支持高效地随机存取（慢于vector）

deque 和 [vector](http://c.biancheng.net/view/348.html) 有很多类似的地方。在 deque 中，随机存取任何元素都能在常数时间内完成（但慢于vector）。

它相比于 vector 的优点是，vector 在头部删除或添加元素的速度很慢，在尾部添加元素的性能较好，而 deque 在头尾增删元素都具有较好的性能（大多数情况下都能在常数时间内完成）。它有两种 vector 没有的成员函数：

```c++
void push_front (const T & val);  //将 val 插入容器的头部
void pop_front();  //删除容器头部的元素
```



### 2、不支持高效地插入和移动

在中间插入或删除元素时，因为要移动多个元素，因此速度较慢，平均花费的时间和容器中的元素个数成正比。

至于在中间插入或删除元素，必然涉及元素的移动，因此时间不是固定的，而是和元素个数有关。
