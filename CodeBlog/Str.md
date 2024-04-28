# 字符串

## Leetcode 541.反转字符串Ⅱ

<img src="C:\Users\MI\AppData\Roaming\Typora\typora-user-images\image-20240428233635908.png" alt="image-20240428233635908" style="zoom: 50%;" />

解题关键:指针的移动可以是2k倍数的，然后对k倍进行判断。因为k倍都是可以被判断的，如果少于k倍则特殊判断

避开i++这个惯性思维.

代码实现:

<img src="C:\Myfiles\Code\C++\code.png" style="zoom: 33%;" />