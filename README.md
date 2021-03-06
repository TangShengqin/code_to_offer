### 剑指offer题

#### 3. 数组中重复的数字

描述：在一个长度为n的数组里的所有数字都在0到n-1的范围内， 数组中某些数字是重复，请找出数组中**任意一个**重复的数字。 例如，如果输入长度为7的数组{2,3,1,0,2,5,3}，那么对应的输出是重复的数字2或者3。  
Python：Find_Repeat_Num.py  
策略：for循环遍历一次，某个index的对应的数组值不等于index，将其和该index对应的值交换，直到该index值等于该index对应的数组元素值。当遇到numbers[index] = numbers[numbers[index]]时，就返回该值。

#### 4. 二维数组中的查找
描述：  
Python：  
策略：

#### 5. 替换空格
描述：  
Python：  
策略：
#### 6. 从尾到头打印链表
描述：  
Python：  
策略：
#### 7. 重建二叉树
描述：  
Python：  
策略：
#### 8. 二叉树的下一个节点
描述：  
Python：  
策略：
#### 9. 用两个栈实现队列
描述：  
Python：  
策略：
#### 10. 斐波那契数列
描述：  
Python：  
策略：
#### 11. 旋转数组的最小数字
描述：  
Python：  
策略：
#### 12. 矩阵中的路径
描述：  
Python：  
策略：
#### 13. 机器人的运动范围
描述：  
Python：  
策略：
#### 14. 剪绳子
描述：给你一根长度为n的绳子，请把绳子剪成m段 (m和n都是整数，n>1并且m>1)每段绳子的长度记为k[0],k[1],...,k[m].请问k[0]*k[1]*...*k[m]可能的最大乘积是多少？
例如，当绳子的长度为8时，我们把它剪成长度分别为2,3,3的三段，此时得到的最大乘积是18.    
Python：Cut_Rope_Max.py  
策略：当n>=5剪成两段，为4剪成2x2，为3,2,1返回2,1,0，尽可能多的剪出长度为3的段。
#### 15. 二进制中1的个数
描述：输入一个整数，输出该数二进制表示中1的个数。其中负数用补码表示。  
Python：  
策略：n = (n-1)&(n)，每次迭代将当前n最低位1及其右边置0
#### 16. 数值的整数次方
描述：给定一个double类型的浮点数base和int类型的整数exponent。求base的exponent次方。  
Python：Power.py  
策略: 考虑指数为负数和零的情况，异常处理，创建一个全局变量。
#### 17. 打印从1到最大的n位数
描述：给定一个数字N，打印从1到最大的N位十进制数。比如N=3，则依次打印出1,2，...，999  
Python：  
策略：将N位十进制数用字符串表示，用字符加法模拟数字加法。  
#### 18. 删除链表的节点
描述：给定单向链表的头指针和一个节点指针，定义一个函数在O(1)时间删除该节点。  
Python：Delete_Node.py  
策略：分情况考虑，当node有后节点时，直接将node的值替换为后节点值，然后node.next值替换为node.next.next。
#### 19. 正则表达式匹配
描述：  
Python：  
策略
#### 20. 表示数值的字符串
描述：请实现一个函数用来判断字符串是否表示数值（包括整数和小数）。例如，字符串"+100","5e2","-123","3.1416"和"-1E-16"都表示数值。但是"12e","1a3.14","1.2.3","+-5"和"12e+4.3"都不是。  
Python：  
策略：找到数值的一般表达式A[.[B]][e|EC]，A为整数部分，B为小数部分，e或E表示自然底数，C为指数部分，整个字符串前面可以有+和-字符。
#### 21. 调整数组顺序使奇数位于偶数前面
描述： 输入一个整数数组，实现一个函数来调整该数组中数字的顺序，使得所有的奇数位于数组的前半部分，所有的偶数位于位于数组的后半部分，并保证奇数和奇数，偶数和偶数之间的相对位置不变。  
Python：  
策略：比较简单，使用两个index，初始分别指向start和end，然后，交换奇和偶数位置即可。(该方法不能保证奇数与奇数，偶数与偶数之间的相对位置不变)
#### 22. 链表中倒数第k个节点
描述：输入一个链表，输出该链表中倒数第k个结点。  
Python：  
策略：构建两个指针p1和p2，两个指针间隔为k-1个节点，遍历一遍链表，p1和p2指针依次加1，当p2到达链表尾部时，p1就指向倒数第k个节点了。
#### 23. 链表中环的入口节点
描述：一个链表中包含环，请找出该链表的环的入口结点。  
Python：Output_Ring_Entrance_Node.py  
策略：分为两步执行。第一步：判断链表是否有环。设置两个指针，初始都指向头节点，P1一次跳两个，P2一次跳一个，当P1和P2能相遇，则说明有环，然后在for循环遍历环，得到环的长度K；第二步：找到环的起始位置。设置两个指针p1和p2，初始都指向链表头，p2先前向走k步，然后p1和p2再同时走，当p1和p2相遇的位置，即为环的入口。
#### 24. 反转链表
描述：输入一个链表，反转链表后，输出链表的所有元素。  
Python：ReverseList.py    
策略：需要保存临时链表防止断裂，返回节点为原链表的尾节点。
#### 25. 合并两个排序的链表
描述：输入两个单调递增的链表，输出两个链表合成后的链表，当然我们需要合成后的链表满足单调不减规则。  
Python：  
策略：两个链表是有序的，判断其各自的Head节点，返回较小的值。依次获取下一个较小的值，用一个递归来实现。
#### 26. 树的子结构
描述：  
Python：  
策略
#### 27. 二叉树的镜像
描述：  
Python：  
策略
#### 28. 对称的二叉树
描述：  
Python：  
策略
#### 29. 顺时针打印矩阵
描述：输入一个矩阵，按照从外向里以顺时针的顺序依次打印出每一个数字，例如，如果输入如下矩阵： 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 则依次打印出数字1,2,3,4,8,12,16,15,14,13,9,5,6,7,11,10.  
Python：Clockwise_Print_Matrix.py    
策略: 采用旋转魔方的方式 一次取一行，然后将剩余的矩阵逆时针旋转，再取出一行，迭代的进行。
#### 30. 包含min函数的栈
描述：  
Python：  
策略
#### 31. 栈的压入，弹出序列
描述：  
Python：  
策略：
#### 32. 从上到下打印二叉树
描述：  
Python：  
策略：
#### 33. 二叉搜索树的后序遍历序列
描述：  
Python：  
策略：
#### 34. 二叉搜索树和为某一值的路径
描述：  
Python：  
策略：
#### 35. 复杂链表的复制 
描述：  
Python：  
策略：
#### 36. 二叉搜索树与双向链表
描述：  
Python：  
策略
#### 37. 序列化二叉树
描述：  
Python：  
策略
#### 38. 字符串的排列
描述：  
Python：  
策略
#### 39. 数组中出现次数超过一半的数字
描述：  
Python：  
策略
#### 40. 最小的k个数
描述：输入n个整数，找出其中最小的K个数。例如输入4,5,1,6,2,7,3,8这8个数字，则最小的4个数字是1,2,3,4,。  
Python：  
策略：
#### 41. 数据流中的中位数
描述：  
Python：  
策略
#### 42. 连续子数组的最大和
描述：  
Python：  
策略
#### 43. 1-n整数中1出现的次数
描述：  
Python：  
策略
#### 44. 数字序列中某一位的数字
描述：  
Python：  
策略
#### 45. 把数组排成最小的数
描述：输入一个正整数数组，将它们连接起来排成一个数，输出能排出的所有数字中最小的一个。例如输入数组{32,  321}，则输出这两个能排成的最小数字32132。    
Python：Find_Largest_Num_Spliced_By_Two_Arrays.py    
策略：用快排，这里组成数字可能超过Python中可能表示的长度，所以用字符串来表示。然后判断两个数字大小的标准是，AB>BA，则A>B，表明A应该排在B的前面。
#### 46. 把数字翻译成字符串
描述：  
Python：  
策略
#### 47. 礼物的最大价值
描述：  
Python：  
策略
#### 48. 最长不含重复字符的子字符串
描述：  
Python：  
策略
#### 49. 丑数
描述：  
Python：  
策略
#### 50. 第一个只出现一次的字符
描述：  
Python：  
策略
#### 51. 数组中的逆序对
描述：  
Python：  
策略：
#### 52. 两个链表的第一个公共节点
描述：  
Python：  
策略：
#### 53. 在排序数组中查找数字
描述：  
Python：  
策略：
#### 54. 二叉搜索树的第k大节点
描述：  
Python：  
策略：
#### 55. 二叉树的深度
描述：  
Python：  
策略：
#### 56. 数组中数字出现的次数
描述：  
Python：  
策略
#### 57. 和为s的数字
描述：  
Python：  
策略
#### 58. 翻转字符串
描述：  
Python：  
策略
#### 59. 队列的最大值
描述：  
Python：  
策略
#### 60. n个骰子的点数
描述：  
Python：  
策略
#### 61. 扑克牌中的顺子
描述：  
Python：  
策略
#### 62. 圆圈中最后剩下的数字
描述：  
Python：  
策略
#### 63. 股票的最大利润
描述：  
Python：  
策略
#### 64. 求1+2+3+...+n
描述：  
Python：  
策略
#### 65. 不用加减乘除做加法
描述：  
Python：  
策略
#### 66. 构建乘积数组
描述：  
Python：  
策略

#### 67. 跳台阶
描述：一只青蛙一次可以跳上1级台阶，也可以跳上2级。求该青蛙跳上一个n级的台阶总共有多少种跳法。   
Python：Jump_One_Two_Sum.py  
策略：找规律，结果是一个斐波那契数列。

#### 68. 变态跳台阶
描述：一只青蛙一次可以跳上1级台阶，也可以跳上2级……它也可以跳上n级。求该青蛙跳上一个n级的台阶总共有多少种跳法。  
Python：Jump_Difficult.py  
策略：找规律，结果是一个指数数列1 2 4 8 16...。



### 其他公司面试题

#### 1. 求数的立方根
描述：输入一个数x和允许的误差范围，要求只用普通的加减乘除运算，求得该数的立方根的近似值，要求该值的立方与x的误差小于eps。    
Python：GetCubicRoot.py    
策略：输入一个数x，其立方根是有范围的，假设x最大为2^31-1，则当x>0，立方根范围为[0,1e+4]，这个时候用二分法逐步缩小范围。

#### 2. 快排
python: quickSort.py  
策略：递归调用，每次随机选取一个值key，保证key值左边比key小，右边比key大。否则交换。

#### 3. 二分查找
描述：输入一个有序的数组，查找某个元素。  
python：BinarySearch.py  
策略：每次将数组分成两份，两边为start和end，中间值为mid，当x大于中间值时，下次从右边搜索，否则从左边搜索，搜索过程start和end会被更新，当start>=end时，返回mid值。  

#### 4. 求重复出现数字(2次或3次)数组中的唯一数
描述：一个整型数组里除了两个数字之外，其他的数字都出现了两次。请写程序找出这两个只出现一次的数字。要求时间复杂度是O(n)，空间复杂度是O(1)。  
python：FindNumsAppearOnce.py    
策略：情况一：如果数组重复数字出现2次，则先遍历一遍数组，两两之间做异或，根据得到的异或值，找到值为1的任意一个位置作为划分条件，该位位置为0换分为一堆，为1划分为另一堆。  情况二：单个元素，其他重复元素出现三次，这时候统计32个位置上1的个数，判断是否能被3整除。  


#### 5. StdInOut.py
描述：使用Python做与标准输入输出相关的题目。