## 总结

283和27两道题的思路其实是很相似的。
都是原地更改list,一个是移除某一个元素，一个是将0移动到list尾部。
其实都是通过对List的重新赋值来实现的。
用一个标记位i=0,每当有符合条件的数，就移动到List的第i位上，然后i+=1。

## 136 只出现一次的数字

给定一个非空整数数组，除了某个元素只出现一次以外，其余每个元素均出现两次。找出那个只出现了一次的元素。

要求
- 线性时间复杂度
- 不使用额外的空间

思路: 肯定不能按照平常的数组思路来看待这道题了，要求是线性时间复杂度和不使用额外的空间。

^= ：对一个数进行异或运算。  a^=b 将a,b都转换为2进制。每位都进行异或运算
异或运算: 只有两个数不相等才为1
a b
0 1 1
1 0 1
1 1 0
0 0 0

在list 中出现两次的数，取异或运算最后的结果肯定为0，
对数组中每个数和0去取异或运算，剩下的结果就是那个数


### 137 只出现一次的数字2
