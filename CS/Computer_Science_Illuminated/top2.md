top2: 二进制数值和计数系统

这节主要就是理解二进制数值，能够进行相关的转换和操作，理解计算机系统如何使用二进制计数。知识点涵盖如下：

- 数字分类
- 位置计数
- 其他基数的的数字转换成十进制
- 十进制转换为其他基数的数字
- 基数2，8，16之间的关系
- 为什么以2的幂为基数？

# 一.数字和计算
>数字是属于抽象数学系统的一个单位，服从特定的顺序法则，运算法则

数字的分类：

- 自然数：是0和通过在0上重复加1得到的任何数
- 负数：小于0的数
- 整数：所有自然数和他们的负数
- 有理数：包括整数和两个整数的商

数字对计算至关重要，用到那呢？

1. 运算
2. 所有计算机存储和管理的数据都以数字形式存储
3. 所有信息都是用数字0，1存储

# 二.位置记数法
**基数**：决定了系统数字量，从0开始，到基数-1结束。例如以2为基数，有两个数字0和1；以8为基数，有8个数字，0~7；以10为基数，有10个数字，0~9

## 1.1 十进制(Decimal)
基数10， 范围0~9, 标识`D`或下标`10`, 如 (123)D

## 1.2 二进制(Binary)
基数2，范围0~1, 标识`B`或下标`2`, 如 (1001010)B

## 1.3 八进制(Octal)
基数8，范围0~7, 标识`Q`或`O`或下标`8`, **在C/C++中，一定要标识O表明是八进制**

## 1.4 十六进制(Hexadecilmal)
基数16，范围0~15, 标识`H`或下标`16`, **在C/C++， 一定要`0X`开头**

## 1.5 重点小结

- 计算机的运算都是二进制
- 计算机为什么出现这么多进制的原因**数据用二进制表示太长**
- C/C++代码中不能直接写二进制， 而是普遍采用八进制或十六进制
- 为什么不是9进制或20进制，原因就是**2,8,16分别是2的次方，这就是三种进制之间可以直接互相转换**

# 三.不同进制间的互相转换
## 3.1 非十进制转换为十进制
采用**按权相加**

![](https://raw.githubusercontent.com/BeginMan/BookNotes/master/CS/media/cs3.png)

![](https://raw.githubusercontent.com/BeginMan/BookNotes/master/CS/media/cs4.png)

十六进制也同上

## 3.2 十进制转换为非十进制

### 3.2.1 十进制整数转二进制

>这里是**整数**， 方法**除2逆序取余法**， 先将十进制数除以2，得到一个商(也是下一步的被除数)和余数；然后再将商除以2，又得到一个商和余数；以此类推，直到商数小于2为止。然后从最后得到小于2的商开始将其他各步所得的余数(也是小于2)排列起来，就得到了对应的二进制

![](https://raw.githubusercontent.com/BeginMan/BookNotes/master/CS/media/cs5.png)

### 3.2.2 十进制小数转换为二进制

![](https://raw.githubusercontent.com/BeginMan/BookNotes/master/CS/media/cs6.png)

![](https://raw.githubusercontent.com/BeginMan/BookNotes/master/CS/media/cs7.png)

### 3.2.3 十进制转八进制
与转二进制类似，不过基数变成了8

![](https://raw.githubusercontent.com/BeginMan/BookNotes/master/CS/media/cs8.png)

![](https://raw.githubusercontent.com/BeginMan/BookNotes/master/CS/media/cs9.png)

### 3.2.4 十进制转16进制

![](https://raw.githubusercontent.com/BeginMan/BookNotes/master/CS/media/cs10.png)

# 四.二进制数值与计算机

- 位(bit): 一个存储单元，二进制数字的简称
- 字节(byte): 8个二进制位
- 字(word)：一个或多个字节， 字中的位数称为字长


