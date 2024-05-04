# 双指针专题

## LeetCode 27.移除元素

<img src="C:\Users\MI\AppData\Roaming\Typora\typora-user-images\image-20240504134847114.png" alt="image-20240504134847114" style="zoom:50%;" />

解题关键:快慢指针，慢指针用来覆盖要更新的区域(比如从0下标开始更新)，快指针是指向要判断的元素.

------



## LeetCode 344.反转字符串

<img src="C:\Users\MI\AppData\Roaming\Typora\typora-user-images\image-20240504135012886.png" alt="image-20240504135012886" style="zoom:50%;" />

解题关键:运用前后指针(left,right)，不断向中间靠拢，然后两两交换.

------



## KamaCoder 54.替换数字

<img src="C:\Users\MI\AppData\Roaming\Typora\typora-user-images\image-20240504141733893.png" alt="image-20240504141733893" style="zoom:50%;" />

解题关键:预分配空间，然后**设立前后指针，前指针指向要判断的元素，后指针指向要更新的位置**。此题关键是从后往前填充，因为从后往前填充时间复杂度为线性，而从前往后填充要移动后面的元素，时间复杂度为二次方。

------

## LeetCode 151.反转字符串的单词

<img src="C:\Users\MI\AppData\Roaming\Typora\typora-user-images\image-20240504142151256.png" alt="image-20240504142151256" style="zoom:50%;" />

解题关键:消除空格 整体反转 局部反转

消除空格:跟移除元素类似也是设立快慢指针，不过区别是，要在慢指针上的数字前加入空格和对下标为0进行判断。

------

## LeetCode 206.反转链表

<img src="C:\Users\MI\AppData\Roaming\Typora\typora-user-images\image-20240504142441389.png" alt="image-20240504142441389" style="zoom:50%;" />

解题关键:设立快慢指针，慢指针指向NULL，快指针指向头节点，然后快慢指针同时向后移动。

------

## LeetCode 19.删除链表的倒数N个结点

<img src="C:\Users\MI\AppData\Roaming\Typora\typora-user-images\image-20240504142636871.png" alt="image-20240504142636871" style="zoom:50%;" />

解题关键:设立快慢指针，快指针先走N步(差出N+1个空间)，然后快慢指针同时走，这样就找到倒数N+1的结点的位置了。

------

## LeetCode 02.07 链表相交

<img src="C:\Users\MI\AppData\Roaming\Typora\typora-user-images\image-20240504142929535.png" alt="image-20240504142929535" style="zoom:50%;" />

解题关键：求两个链表的长度之差，然后让短指针走差数，使长短指针离公共节点距离一样，然后同时走。

------

## LeetCode 142.环形链表Ⅱ

<img src="C:\Users\MI\AppData\Roaming\Typora\typora-user-images\image-20240504143233751.png" alt="image-20240504143233751" style="zoom:50%;" />

解题关键：快慢指针，快指针走两步，慢指针走一步。

1.找环(看看快指针到不到NULL)

2.数学公式：头节点到环入口为X，环入口到第一次相交的位置为Y，第一次相交的位置到入口为Z，所以有S-fast=X+N(Y+Z)+Z，S-slow = X+Y，S-fast = 2*S-slow，所以解得X = Z + N圈，因此在头节点设立临时指针，同时移动临时指针和快指针，一定能在入口处相交。

------

## LeetCode 15.三数之和

<img src="C:\Users\MI\AppData\Roaming\Typora\typora-user-images\image-20240504143801732.png" alt="image-20240504143801732" style="zoom:50%;" />

解题关键：

1.设立三个指针（三数之和用三个指针），第一个指针从0遍历，第二三个指针是前后指针，不断向中间靠拢

2.剪枝判断

3.去重（遍历指针用nums[i]==nums[i-1]） 快慢指针直接用nums[left]==nums[left+1]向中间靠拢

------

## LeetCode 18.四数之和



<img src="C:\Users\MI\AppData\Roaming\Typora\typora-user-images\image-20240504144304376.png" alt="image-20240504144304376" style="zoom:50%;" />

解题关键：和三数之和类似，设立四个指针，其中两个遍历指针和快慢指针，注意不要超出判断范围了。