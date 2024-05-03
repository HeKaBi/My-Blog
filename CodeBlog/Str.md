# 字符串

------



## Leetcode 541.反转字符串Ⅱ

<img src="C:\Users\MI\AppData\Roaming\Typora\typora-user-images\image-20240428233635908.png" alt="image-20240428233635908" style="zoom: 50%;" />

解题关键:**<u>指针的移动可以是2k倍数的</u>**，然后对k倍进行判断。因为k倍都是可以被判断的，如果少于k倍则特殊判断

避开i++这个惯性思维.

代码实现:

<img src="C:\Users\MI\AppData\Roaming\Typora\typora-user-images\image-20240429192701269.png" alt="image-20240429192701269" style="zoom:50%;" />

------



## Kamacoder 54.替换数字

<img src="C:\Users\MI\AppData\Roaming\Typora\typora-user-images\image-20240429192837901.png" alt="image-20240429192837901" style="zoom:50%;" />

解题关键:用resize()接口扩展原来字符串的大小，然后设立双指针，一个指向新大小的尾部，一个指向原大小的尾部，**<u>然后从后往前复制</u>**(这个是关键)，不能从前往后(因为从前往后会导致O(n²)的时间复杂度，因为每次移动还要复制后面的内容)

代码实现:

<img src="C:\Users\MI\AppData\Roaming\Typora\typora-user-images\image-20240429193416297.png" alt="image-20240429193416297" style="zoom:50%;" />

------

## Leetcode 151.反转字符串的单词

<img src="C:\Users\MI\AppData\Roaming\Typora\typora-user-images\image-20240429220734719.png" alt="image-20240429220734719" style="zoom:50%;" />

解题关键: 

1.**分析步骤**: 删除多余空格 -> 整体反转 -> 每个单词反转

2.**删除多余空格**：设立快慢指针，快指针指向目标元素，慢指针指向更新位置，注意的是 不能超出size 每个单词前面要加空格(除了第一个)

具体代码:

<img src="C:\Users\MI\AppData\Roaming\Typora\typora-user-images\image-20240429221349857.png" alt="image-20240429221349857"  />

------

## KamaCoder 55.右旋转字符串

<img src="C:\Users\MI\AppData\Roaming\Typora\typora-user-images\image-20240503223340092.png" alt="image-20240503223340092" style="zoom:50%;" />

解题关键: 整体反转再局部反转

------

## LeetCode 28.找到字符串中第一个匹配项的下标

<img src="C:\Users\MI\AppData\Roaming\Typora\typora-user-images\image-20240503223539230.png" alt="image-20240503223539230" style="zoom:50%;" />

解题关键:

**1.kmp算法**：kmp匹配的精髓就是前缀表，通过前缀表去跳转，那么在实现的过程分为两个主部分：**求next数组** 和 **kmp匹配**，两个方法:前缀表减一和不减一 

2.**求next数组**：设立两个指针，前指针指向前缀尾部，后指针指向后缀尾部，然后匹配，如果String[前指针]不等于String[后指针]，就让前指针跳转。如果相等，就让前指针加一，最后更新next[i]

3.**kmp匹配**: 设立两个指针，一个指向文本串，一个指向模式串，如果两个数值不相等，就让模式串指针跳转，相等，就让模式串指针加一，如果模式串指针出局，就判定。

注意前缀表的特性在两个方法的实现下的区别。

------

## LeetCode 459.重复的子字符串

<img src="C:\Users\MI\AppData\Roaming\Typora\typora-user-images\image-20240503224804431.png" alt="image-20240503224804431" style="zoom:50%;" />

解题关键:

**发现长度%(长度-最大公共前后缀长度)==0这个式子**
