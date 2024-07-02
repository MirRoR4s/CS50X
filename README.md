# [CS50X](https://cs50.harvard.edu/x/2024/)

记录**CS50X**学习过程

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