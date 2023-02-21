- [交织技术](#交织技术)
  - [1.突发错误](#1突发错误)
  - [2.抗突发错的有效手段——交织](#2抗突发错的有效手段交织)
  - [3.交织器的三个重要参数](#3交织器的三个重要参数)


## 交织技术

### 1.突发错误

+ 干扰、衰落、均衡等等都会引入突发错。
+ 经过信道编译码后，其译码输出的错误也将呈现突发性，无论是分组码，还是卷积码都是如此。
  + 信道编译码的门限效应

卷积码抗突发错能力很差

- 卷积码是靠相邻符号间的相关性提供保护的，而此相关性的维系时间一般较短
- 分组码对突发错和随机错的纠错能力基本相当，但码长较短，稍长一些的突发也无能为力
- 也有专门针对突发错设计的分组码，但纠随机错的能力相应降低

### 2.抗突发错的有效手段——交织

交织 (interleaving) 就是一种将数据序列的顺序进行变换的一种处理方法。又可称为置换（permutation）。

交织器的一般表示方法

+ 交织表:  $\boldsymbol{j}=\boldsymbol{T}(i)$ , 表示输出序列的第  j  个符号取自输入序列的第  i  个符号。即当输入序列为  $x_{1}, x_{2}, \ldots$ , 输出 序列为  $y_{1}, y_{2}, \ldots$  时, $ y_{j}=x_{T(i)}$  。

### 3.交织器的三个重要参数

+ 交织延迟
+ 交织前相邻的符号在交织后的最小距离称为交织深度
+ 交织后相邻的符号在交织前的最小距离称为交织宽度

基本交织（块交织, block interleaver）

将数据流分成长度为  $\mathbf{W} * \mathbf{L}$  的块, 将数据逐行写入一个  $\mathbf{L}$  行  $\mathbf{W}$  列的矩阵形缓冲区, 写满后再逐列读出。

深度为  $\mathbf{L}$ , 宽度为  $\mathbf{W}$ , 延时为  $\mathbf{W L}$  。交织和解交织的延时总和为 2WL。

输入序列为  $x_{1}, x_{2}, \ldots, x_{R C}$ ; 输出序列为  $y_{1}, y_{2}, \ldots, y_{R C}$  。

![](https://raw.githubusercontent.com/timerring/picgo/master/picbed/image-20230210160532927.png)

总结

+ 卷积码:概念，编码、连接矢量、状态图、网格图、维特比译码算法。
+ 交织技术:抵抗突发错误

信道编码总结:

+ 分组码(n，k)、循环码——无记忆编码
+ 卷积码（n，k，L)——有记忆编码







参考文献：

1. Proakis, John G., et al. *Communication systems engineering*. Vol. 2. New Jersey: Prentice Hall, 1994.
2. Proakis, John G., et al. *SOLUTIONS MANUAL Communication Systems Engineering*. Vol. 2. New Jersey: Prentice Hall, 1994.
3. 周炯槃. 通信原理（第3版）[M\]. 北京：北京邮电大学出版社, 2008.
4. 樊昌信, 曹丽娜. 通信原理（第7版） [M\]. 北京：国防工业出版社, 2012.



[返回首页](https://github.com/timerring/information-theory)