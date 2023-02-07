- [离散信源 R(D)计算](#离散信源-rd计算)
  - [二元对称信源的  R(D)  函数](#二元对称信源的--rd--函数)
- [高斯信源的 R(D)函数](#高斯信源的-rd函数)
- [限失真信源编码定理](#限失真信源编码定理)


## 离散信源 R(D)计算

给定信源概率  $p_{\mathrm{i}}$  和失真函数  $d_{\mathrm{i} j}$  就可以求得该信源的  R(D)  函数。

它是在保真度准则下求极小值的问题。

但要得到它的显式表达式,一般比较困难。通常用参量表达式。即使如此,除简单的情况外实际计算还是困难的, 只能用迭代逐级逼近的方法。

### 二元对称信源的  R(D)  函数

设二元对称信源  $X=\{0,1\}$ , 其概率分布  $p(x)=[p, 1-p]$ ,接收变量  $\mathbf{Y}=\{\mathbf{0}, \mathbf{1}\}$ ,汉明失真矩阵


$$
d=\left[\begin{array}{ll}
0 & 1 \\
1 & 0
\end{array}\right]
$$


因而最小允许失真度  $D_{\min }=0$  。并能找到满足该最小失真的试验信道, 且是一个无噪无损信道, 其信道矩阵为


$$
p=\left[\begin{array}{ll}
1 & 0 \\
0 & 1
\end{array}\right]
$$

计算得:  $\mathrm{R}(0)=\mathrm{I}(\mathrm{X} ; \mathrm{Y})=\mathrm{H}(p)$ 

![](https://raw.githubusercontent.com/timerring/picgo/master/picbed/image-20230207184801859.png)

最大允许失真度为


$$
\begin{aligned}
D_{\text {max }} & =\min _{j=0,1} \sum_{i=0}^{1} p_{i} d_{i j} \\
& =\min \{p(0) d(0,0)+p(1) d(1,0), p(0) d(0,1)+p(1) d(1,1)\} \\
& =\min _{j}\{(1-p), p\}=p \\
\end{aligned}
$$


要达到最大允许失真度的试验信道, 唯一确定为


$$
p=\left[\begin{array}{ll}
0 & 1 \\
0 & 1
\end{array}\right]
$$


![](https://raw.githubusercontent.com/timerring/picgo/master/picbed/image-20230207185620649.png)

这个试验信道能正确传送信源符号  x=1 , 而传送信源符号  x=0  时,接收符号 一定为  $\mathrm{y}=1$  。凡发送符号  x=0  时,一定都错了。而  x=0  出现的概率为  p , 所以信道的平均失真度为  $\boldsymbol{p}$  。

在这种试验信道条件下, 可计算得



$$
\mathbf{R}\left(\mathbf{D}_{\max }\right)=\min _{P_{D \max }} I(X ; Y)=\boldsymbol{H}(\boldsymbol{Y})-\boldsymbol{H}(\boldsymbol{Y} \mid \boldsymbol{X})=\mathbf{0}
$$


对于二进制无记忆信源, 若  $P(X_{\mathrm{i}}=0)=p, P(X_{\mathrm{i}}=1)=1-   p$ , 且采用汉明失真, 其率失真函数为

$$
R(D)=\left\{\begin{array}{cc}
H_{b}(p)-H_{b}(D), & 0 \leq D \leq \min \{p, 1-p\} \\
0, & \text { otherwise }
\end{array}\right.
$$
![](https://raw.githubusercontent.com/timerring/picgo/master/picbed/image-20230207185829915.png)



> 有一个二进制无记忆信源，以概率p=0.25输出“1”，以概率1-p=0.75输出“0”。请问:
>
> (1）若要求采用无失真信源编码，信息率失真函数是多少?
>
> (2）若重构该信源的错误概率不超过0.1，信息率失真函数是多少?
>
> (3）若重构该信源的错误概率不超过0.25，信息率失真函数是多少?这种情况下，最佳的译码策略是什么?
>
> 解:
> (1)  $H(x)=-0.25 \log 0.25-0.75 \log 0.75=0.8113  bit/sym$
>
> (2)  $H(0.25)-H(0.1)=0.3423 bit/sym$
>
> (3) 0. 最佳译码策略是将接收到的信号都译码为 ' 0 '

## 高斯信源的 R(D)函数

对于均值为 0 , 方差为  $\sigma^{2}$  的高斯信源, 采用平方失真时的率失真函数为


$$
R(D)=\left\{\begin{array}{cc}
\frac{1}{2} \log \frac{\sigma^{2}}{D}, & 0 \leq D \leq \sigma^{2} \\
0, & \text { otherwise }
\end{array}\right.
$$



![](https://raw.githubusercontent.com/timerring/picgo/master/picbed/image-20230207202532495.png)

可见, 随着D的增大, R（D）减小。 当  $D \geqslant D \max$  时,  R(D)=0 

一般信息率失真函数的图形如下所示

![](https://raw.githubusercontent.com/timerring/picgo/master/picbed/image-20230207202608123.png)

## 限失真信源编码定理

设离散无记忆信源  $\mathrm{X}$  的信息率失真函数为  $R(\mathrm{D})$ ,

+ 当信息率  R>R(D)  时, 只要信源序列长度  L  足够长,一定存在一种编码方法,其译码失真小于或等于  $D+\varepsilon$, $\varepsilon$  为任意小的正数;
+ 反之, 若  R<R  (D), 则无论采用什么样的编码方法, 其译码失真必大于 D。

如是二元信源, 则对于任意小的  $\varepsilon>0$ , 每一个信源符号的平均码长满足如下公式:


$$
R(D) \leq \bar{K} \leq R(D)+\varepsilon
$$



参考文献：

1. Proakis, John G., et al. *Communication systems engineering*. Vol. 2. New Jersey: Prentice Hall, 1994.
2. Proakis, John G., et al. *SOLUTIONS MANUAL Communication Systems Engineering*. Vol. 2. New Jersey: Prentice Hall, 1994.
3. 周炯槃. 通信原理（第3版）[M\]. 北京：北京邮电大学出版社, 2008.
4. 樊昌信, 曹丽娜. 通信原理（第7版） [M\]. 北京：国防工业出版社, 2012.



[返回首页](https://github.com/timerring/information-theory)
