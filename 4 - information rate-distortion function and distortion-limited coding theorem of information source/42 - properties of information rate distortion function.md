- [信息率失真函数的性质](#信息率失真函数的性质)
  - [率失真函数的单调递减和连续性](#率失真函数的单调递减和连续性)
- [实现限失真信源编码的方式](#实现限失真信源编码的方式)


## 信息率失真函数的性质

1. R(D)  是非负的实数,  $\mathrm{R}(\mathrm{D}) \geq 0$  。

   其定义域为 $0-\mathbf{D}_{\text {max }}$ , 其值为  $0 \sim \mathbf{H}(\mathrm{X})$  。当  $D>D_{\text {max }}$  时,  $R(D) \equiv 0$ 

2. R(D)  是关于  $\mathrm{D}$  的下凸函数

   R(D)  在定义域内是失真度  $\mathrm{D}$  的  $\mathrm{U}$  型下凸函数

3. R(D)  的单调递减性及连续性

   容许的失真度越大, 所要求的信息率越小。反之亦然。

### 率失真函数的单调递减和连续性

R(D)  的非增性也容易理解。允许的失真越大  $\rightarrow$  信息率越小。

+ 根据率失真函数的定义，它是在平均失真度小于或等于允许的平均失真度  D  的所有信道集合  $B_{D}$  中，取平均互信 息的最小值。
+ 当允许失真度扩大， $B_{D}$  集合也扩大，这时在扩大的  $\boldsymbol{B}_{D}$  集合中找最小值，显然这最小值或者不变，或者变小，所以**R(D) 是非增的。**

根据上述性质, 可以画出率失真函数的一般形式, 如下图示。 

![](https://raw.githubusercontent.com/timerring/picgo/master/picbed/image-20230207184114170.png)

图中  $R(0)=H(X)$,   $R\left(D_{\max }\right)=0$ , 决定了曲线边缘上的两个点。而 在 0 和  $D_{\text {max }}$ 之间,  R(D)  是单调递减的下凸函数。

> **在连续信源情况下**, 当  $D \rightarrow 0$  时,  $R(D) \rightarrow \infty$ , 曲线将不与 R(D) 轴相交。

关于信息率失真函数的说明:

通常我们总希望信息通过信道传输时输入与输出之间的互信息最大，是在信道给定情况下的要求。而这里是在信源给定而不是信道给定条件下传输。信息率失真理论要解决的问题就是**计算满足失真要求的传输所需的最小信道容量或传输速率**，以达到降低信道的复杂度和通信成本的目的。

## 实现限失真信源编码的方式

适应信源方式:认识信源的实际客观概率统计特性，寻找适应此类概率统计特性的编码方法。

改造信源方式:改造信源的客观统计特性，即解除实际信源消息序列各消息间的统计相关性，使之**成为无记忆信源**，进而采用预测编码和变换编码。

参考文献：

1. Proakis, John G., et al. *Communication systems engineering*. Vol. 2. New Jersey: Prentice Hall, 1994.
2. Proakis, John G., et al. *SOLUTIONS MANUAL Communication Systems Engineering*. Vol. 2. New Jersey: Prentice Hall, 1994.
3. 周炯槃. 通信原理（第3版）[M\]. 北京：北京邮电大学出版社, 2008.
4. 樊昌信, 曹丽娜. 通信原理（第7版） [M\]. 北京：国防工业出版社, 2012.



[返回首页](https://github.com/timerring/information-theory)