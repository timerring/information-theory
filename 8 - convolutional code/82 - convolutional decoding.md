- [卷积译码](#卷积译码)
  - [最大似然译码](#最大似然译码)
  - [卷积译码-维特比卷积译码算法](#卷积译码-维特比卷积译码算法)


## 卷积译码

### 最大似然译码

如果所有的输入信息序列等概, 则通过比较各个条件概率, 也称为似然函数  $\mathbf{P}\left(\mathbf{Z} \mid \mathbf{U}^{(\mathbf{m})}\right)$ , 就可以得到具有最小差错概率的译码器, 这里  $\mathbf{Z}$  是接收序列 ,  $\mathbf{U}^{(\mathrm{m})}$  是可能发送的序列。如果满足如下公式, 译码器就选择  $\mathbf{U}^{\left(\mathrm{m}^{\prime}\right)}$ 
$$
\mathbf{P}\left(\mathbf{Z} \mid \mathbf{U}^{\left(\mathbf{m}^{\prime}\right)}\right)=\max \mathbf{P}\left(\mathbf{Z} \mid \mathbf{U}^{(\mathbf{m})}\right) \text { over all } \mathbf{U}^{(\mathbf{m})}
$$
对于 BSC信道, 上式相当于**选择和序列Z具有最小汉明距离的码字**  $\mathbf{U}^{\left(\mathrm{m}^{\prime}\right)}$  。译码器总是从所有可能的发送序列  $\mathbf{U}^{(\mathrm{m})}$  中选择和Z距离最小的序列  $\mathbf{U}^{\left(\mathrm{m}^{\prime}\right)}$  。

对于高斯信道, 距离为欧式距离。

假设接收端收到的码序列为1011010010010010, 如何译码？

计算下图中所有可能路径的概率, 然后比较, 选出最大值。

有多少条路径  ? $\leq 2^{8}$  (穷举法, 需要比较  $2^{l}$ , 其中 l 为码序列长度)

![](https://raw.githubusercontent.com/timerring/picgo/master/picbed/image-20230210155054366.png)

### 卷积译码-维特比卷积译码算法

维特比译码算法是维特比在1967年提出。维特比算法的实质是最大似然译码，但它利用了编码网格图的特殊结构，从而降低了计算的复杂度，与完全比较译码相比，它的优点是使得译码器的复杂性不再是码字序列中所含码元数的函数。

该算法包括计算网格图上在时刻t到达各个状态的路径和接收序列之间的相似度，或者说距离。维特比算法考虑的是，去除不可能成为最大似然选择对象的网格图上的路径，即如果**有两条路径到达同一个状态，则具有最佳量度的路径被选中，称为幸存路径**。

对所有状态都将进行这样的选路操作，译码器不断的在网格图上深入，通过去除可能性最小的路径实现判决。较早地抛弃不可能的路径降低了译码的复杂性。注意，**选择最优路径可以表述为选择具有最大似然度量的码字，或者选择具有最小距离的码字**。

假设为BSC信道，汉明距离为合适的距离度量。

维特比译码算法的精髓可以总结为:加、比、选。

+ 加:距离（概率，分支度量值)相加;
+ 比:累加距离（概率，累计度量值）的比较;
+ 选:选出距离小（概率大）的路径作为幸存路径

维特比译码算法是基于网格图进行的。译码时先将接收序列按照n分组，然后计算每分组与相应网格图中各分支的输出之间的汉明距离。

![](https://raw.githubusercontent.com/timerring/picgo/master/picbed/image-20230210155512415.png)

![](https://raw.githubusercontent.com/timerring/picgo/master/picbed/image-20230210155641037.png)

![](https://raw.githubusercontent.com/timerring/picgo/master/picbed/image-20230210155703983.png)

![](https://raw.githubusercontent.com/timerring/picgo/master/picbed/image-20230210155710856.png)

> 下图所示的(2,1,3)卷积码，若接收序列为:11 01 10 11 00 10 11,求译码结果。
>
> ![](https://raw.githubusercontent.com/timerring/picgo/master/picbed/image-20230210155818044.png)
>
> 译码的路径，译码结果是:10011
>
> ![](https://raw.githubusercontent.com/timerring/picgo/master/picbed/image-20230210155925175.png)
>
> 输入为:10011时，编码结果是 11 01 **11** 11 **10** 10 11
>
> 对比接收序列                             11 01 **10** 11 **00** 10 11
>
> 错了2位，译码过程中都纠正了过来。

卷积码的距离特性:自由距:从0状态回到0状态的距离

![](https://raw.githubusercontent.com/timerring/picgo/master/picbed/image-20230210160045414.png)

$d_{\text {free }}=5 \quad t=\left[\left(d_{f}-1\right) / 2\right]$







参考文献：

1. Proakis, John G., et al. *Communication systems engineering*. Vol. 2. New Jersey: Prentice Hall, 1994.
2. Proakis, John G., et al. *SOLUTIONS MANUAL Communication Systems Engineering*. Vol. 2. New Jersey: Prentice Hall, 1994.
3. 周炯槃. 通信原理（第3版）[M\]. 北京：北京邮电大学出版社, 2008.
4. 樊昌信, 曹丽娜. 通信原理（第7版） [M\]. 北京：国防工业出版社, 2012.



[返回首页](https://github.com/timerring/information-theory)