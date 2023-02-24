- [卷积码基础](#卷积码基础)
  - [卷积码的概念](#卷积码的概念)
  - [卷积码编码器的结构](#卷积码编码器的结构)
  - [卷积编码器表示](#卷积编码器表示)
    - [1、连接矢量（生成矢量)](#1连接矢量生成矢量)
    - [2、状态描述和状态图](#2状态描述和状态图)
    - [3、树图](#3树图)
    - [4、网格图（The trellis Diagram）](#4网格图the-trellis-diagram)


# 卷积码基础

分组码—无记忆编码

卷积码—记忆编码

+ 能够识记卷积码的基本概念;
+ 能够根据连接矢量画出卷积码的编码器，并进行编码;
+ 能够根据编码器画出该卷积码状态转移图和网格图;
+ 能够运用维特比译码算法对卷积码进行译码;
+ 了解交织的概念。

## 卷积码的概念

卷积码由三个整数描述, (n, k, L), 其中k/n也表示编码效率，L称为约束长度; 表示在编码移位寄存器中k元组的级数，k表示编码时一次输入编码器的码元数。

卷积码不同于分组码的一个重要特征就是编码器的记忆性，即卷积编码过程产生的n元组，不仅是当前输入k元组的函数，而且还是前面L-1个输入k元组的函数。通常，n和k取较小的值，通过L的变化来控制编码的能力和复杂度。

## 卷积码编码器的结构

(n, k, L) 卷积码: 下图为卷积码的编码器, 其中有  kL  级 移位寄存器,  $\boldsymbol{L}$  称为卷积码的约束长度。

卷积码的编码器是一种有限状态机，它的状态数目为  $2^{(L-1) k}$  。状态和当前输入的  $\boldsymbol{k}$  元组决定了当前输出的  n  元组。

![](https://raw.githubusercontent.com/timerring/picgo/master/picbed/image-20230210145547498.png)

## 卷积编码器表示

这是一个 (2,1,3）卷积码，即n=2, k=1,L=3。

![](https://raw.githubusercontent.com/timerring/picgo/master/picbed/image-20230210145822407.png)

为什么叫卷积码? 

![](https://raw.githubusercontent.com/timerring/picgo/master/picbed/image-20230210145937092.png)

编码过程:

设输入信息序列100101.

输出信息序列为11 01 11 11 01 00 **01 11**

**卷积码编码器初始状态为0，编码之后需保证状态清零**

### 1、连接矢量（生成矢量)

描述编码器的一种方法是指定n个连接矢量，每个矢量对应于一个模2加法器。每个矢量都是L维的，表示该模2加法器和编码移位寄存器之间的连接。矢量中第i位上的**1表示移位寄存器相应级与模2加法器连接**，**若是0，则表示相应级与模2加法器之间无连接**。

![](https://raw.githubusercontent.com/timerring/picgo/master/picbed/image-20230210153643794.png)

### 2、状态描述和状态图

卷积码编码器属于一类称为有限状态机的器件。

“有限”表明状态机制只有有限个不同的状态。“状态”可以用设备的当前输入和最少的信息数量，来预测设备的输出。状态提供了有关过去序列过程及一组将来可能输出序列的限制，下一状态总是受到前一状态的限制。

以编码效率为1/n的卷积码编码器为例,状态就用最右端（L-1)级寄存器内容来表示（注意这里的最右端是指当前信息码元输入后移位寄存器最右端的寄存器）。

了解当前状态以及下一个输入，是确定下一输出的充要条件。

表示简单编码器的一种方法是状态图。

![](https://raw.githubusercontent.com/timerring/picgo/master/picbed/image-20230210153857897.png)

状态图方框内的状态表示寄存器最右端(L-1）级的可能内容，状态间的路径表示由此状态转移是的输出分支字。寄存器的状态表示为a=00，b=01，c=10，d=11.对应于两种可能的输入比特，从每一个状态出发只有两种转移，状态转移时的输出分支字标注在相应的转移路径旁。图中实线表示输入比特为0的路径，虚线表示输入比特为1的路径。

注意:状态转移不是任意的。由于每次移入1个信息比特，故寄存器在每个比特时间上只有两种可能的状态转移。

![](https://raw.githubusercontent.com/timerring/picgo/master/picbed/image-20230210154008154.png)

### 3、树图

虽然状态图完全的描述了编码器的特性，但由于没有表示时间的过程，采用状态图跟踪编码器的状态转移很不方便。如果要展示出编码器输入、输出的所有可能情况，则可用树图描述。它是将编码器的状态图按时间展开而成的。

![](https://raw.githubusercontent.com/timerring/picgo/master/picbed/image-20230210154111014.png)

### 4、网格图（The trellis Diagram）

网格图将树图上处于同一状态的同一级节点合并。

下图为  (2,1,3)  卷积码的网格图。网格图的节点代表了编码器的状态; 在每个时间单元内, 网格图用  $2^{L-1}$  个节点表示  $2^{L-1}$  个可能的编码器状态。可见，会有重复。



![](https://raw.githubusercontent.com/timerring/picgo/master/picbed/image-20230210154137062.png)



某  (2,1,3)  卷积码的连接矢量为:
$$
g_{1}=\left[\begin{array}{lll}
1 & 1 & 0
\end{array}\right], \quad g_{2}=\left[\begin{array}{lll}
0 & 1 & 1
\end{array}\right]
$$
(1) 请画出该卷积码的编码器、状态图和网格图。

(2) 当输入序列为 100011101001 时，求编码输出。

![](https://raw.githubusercontent.com/timerring/picgo/master/picbed/image-20230210154746921.png)







参考文献：

1. Proakis, John G., et al. *Communication systems engineering*. Vol. 2. New Jersey: Prentice Hall, 1994.
2. Proakis, John G., et al. *SOLUTIONS MANUAL Communication Systems Engineering*. Vol. 2. New Jersey: Prentice Hall, 1994.
3. 周炯槃. 通信原理（第3版）[M\]. 北京：北京邮电大学出版社, 2008.
4. 樊昌信, 曹丽娜. 通信原理（第7版） [M\]. 北京：国防工业出版社, 2012.



[返回首页](https://github.com/timerring/information-theory)
