# [CS50X](https://cs50.harvard.edu/x/2024/)

记录**CS50X**学习过程，学习进度的查阅可以参见[此处](https://cs50.me/cs50x)。

- [编程环境](https://cs50.dev/)

- [ps0](https://cs50.harvard.edu/x/2024/weeks/0/)：一个简单的 scratch 程序，能够在点击绿色旗子后向我问好，并播放周杰伦的歌曲。
- [ps1](https://cs50.harvard.edu/x/2024/weeks/1/)：
  - 用户输入名称并向用户问好
  - 输入金字塔（pyramid）高度并打印它。解题的关键在于先打印空格再打印 `#` 号
  - [cash](https://cs50.harvard.edu/x/2024/psets/1/cash/)：基于贪心算法求解要找给顾客的最小硬币数
- [ps2](https://cs50.harvard.edu/x/2024/psets/2/)
  - [Scrabble](https://cs50.harvard.edu/x/2024/psets/2/scrabble/)：统计两位玩家填词游戏的分数并输出胜者，主要的问题在于获取字符对应的分数。定义一个分数数组，存储a-z共26个字母对应的分数，然后通过将字符减去 ASCII 值就可以得到字符在数组中的索引从而获取分值。
  - [Readability](https://cs50.harvard.edu/x/2024/psets/2/readability/)：计算一段文本的可读性并给出其面向的年级。主要解决的问题是计算文本中的字母个数、单词个数、句子个数，这里保证输入都是合法的，所以计算函数十分简单。
  - [Caesar](https://cs50.harvard.edu/x/2024/psets/2/caesar/)：实现一个凯撒加密程序，主要解决的问题是计算密文字母的ASCII值，这可以通过将明文字母的ASCII值减去97再加上密钥，最后再加上97来解决。
- [ps3](https://cs50.harvard.edu/x/2024/psets/3/)
  - [Sort](https://cs50.harvard.edu/x/2024/psets/3/sort/)：给出三个编译好的排序程序，这三个程序采用了冒泡排序、选择排序、归并排序，问题是分辨出三个程序分别采用了什么排序算法。可从程序对不同规模数字的排序时间以及同规模时数字是否有序的排序时间来判别。
  - [Plurality](https://cs50.harvard.edu/x/2024/psets/3/plurality/)：编写一个基于多数投票原则（票高者赢）的选举程序并打印出赢家。尽管 ps3 讲到了一些排序算法，但求解本题并不需要排序，只需遍历候选者列表找到最高的票数，最后再次遍历打印和最高票数一样的候选者即可。
  - [Runoff](https://cs50.harvard.edu/x/2024/psets/3/runoff/)：实现一个 Runoff 投票程序。选民可对所有候选者投票，并根据对他们的支持程度进行排序。第一轮比较时统计所有选民最支持的候选者的票数，如果有一个候选者票数超过了半数，那么该候选者胜出。如果没有并且所有候选者的票数相同，那么判定凭平局，否则淘汰掉票数最低的候选者。之后开始统计选民第二支持的候选者的票数，重复以上过程完成选举。
- [ps4]()

#### [volume](https://cs50.harvard.edu/x/2024/psets/4/volume/)

修改一个音频文件的音量，涉及的知识点包括：

1. 音频文件的组成：44字节首部以及后续的一系列 samples，每个 samples 一般占据 16 比特，但也不绝对。修改音量主要就是修改 samples 的值。
2. fwrite、fopen 函数的用法、参数的含义。

#### [filter](https://cs50.harvard.edu/x/2024/psets/4/filter/less/)

编写四个 BMP（24 bit）图片过滤函数，分别用于将图片变为黑白、镜像、模糊、？。背后的具体原理不甚了解，但主要的操作就是修改原始图片的像素值。（图片首部的操作已经封装好，我们只需操作图片的像素值）

- 要将图片变为黑白，只需要让像素的RGB值一样，具体的值可以是RGB总值取平均数。
- 要镜像图片，只需对调一行中的像素，左边放到右边，右边放到左边这样。
- 要模糊图片，只需将像素值改为其八个方向的相邻像素之和的平均值

## Week 5 Data Structures







