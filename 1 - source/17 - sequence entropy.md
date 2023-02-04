- [离散无记忆信源的序列熵](#离散无记忆信源的序列熵)
  - [信源的序列熵](#信源的序列熵)
- [离散有记忆信源的序列熵](#离散有记忆信源的序列熵)
  - [平稳有记忆N次扩展源的熵](#平稳有记忆n次扩展源的熵)


### 离散无记忆信源的序列熵

![](https://raw.githubusercontent.com/timerring/picgo/master/picbed/image-20220923102438487.png)

马尔可夫信源的特点：无后效性。

发出**单个符号**的信源

- 指信源每次只发出一个符号代表一个消息;

发出**符号序列**的信源

- 指信源每次发出一组含二个以上符号的符号序列代表一个消息。

当信源**无记忆**时：
$$
\begin{aligned}
p(\bar{X}&\left.=x_{i}\right)=p\left(x_{i_{1}}, x_{i_{2}}, \cdots, x_{i_{L}}\right)
=p\left(x_{i_{1}}\right) p\left(x_{i_{2}}\right) p\left(x_{i_{3}}\right) \cdots p\left(x_{i_{L}}\right)=\prod_{l=1}^{L} p\left(x_{i_{l}}\right)
\end{aligned}
$$

#### 信源的序列熵

$$
\begin{aligned}
H(\bar{X}) &=-\sum_{i=1}^{n^{L}} p\left(x_{i}\right) \log p\left(x_{i}\right) \\
&=-\sum_{i} \prod_{l=1}^{L} p\left(x_{i_{i}}\right) \log p\left(x_{i_{i}}\right)=\sum_{l=1}^{L} H\left(X_{l}\right)
\end{aligned}
$$

- 若又满足**平稳特性**（平稳信号包含的信息量小，其统计特性随时间不变化）,即与序号l无关时:

  $$
  p(\overline{\mathrm{X}})=\prod_{l=1}^{L} p\left(x_{i_{\mathrm{i}}}\right)=p^{L}
  $$

- 信源的序列熵

  $$
  H(\overline{\mathrm{X}})=\operatorname{LH}(X)
  $$

- 平均每个符号(消息)熵(符号熵) 为

  $$
  H_{L}(\bar{X})=\frac{1}{L} H(\bar{X})=H(X)
  $$

> 例: 有一个无记忆信源随机变量 $\mathrm{X} \in(0,1)$ , 等概率分布, 若以单个符号出现为一事件, 则此时的信源熵:
>
> $H(X)=\log _{2} 2=1$ bit/符号
>
> 即用 1 比特就可表示该事件。
>
> - 如果以两个符号出现 ($\mathrm{L}=2$  的序列 )为一事件, 则随机序 列 $\mathrm{X} \in(00,01,10,11)$ , 信源的序列熵
>
>   $H(\bar{X})=\log _{2} 4=2$ bit/序列
>
> 即用2比特才能表示该事件。
>
> - 信源的**符号熵**
>
>   $H_{2}(\overline{\mathrm{X}})=\frac{1}{2} H(\overline{\mathrm{X}})=1$ bit/符号

> ![](https://raw.githubusercontent.com/timerring/picgo/master/picbed/image-20220923104715215.png)
>
> - 信源的序列熵
>
> $H(\overline{\mathrm{X}})=H\left(X^{L}\right)=-\sum_{i=1}^{9} p\left(a_{i}\right) \log p\left(a_{i}\right)=3 b i t / \text { 序列 }$
>
> - 平均每个符号 (消息) 熵为
>
> $\begin{array}{c}
> H(X)=-\sum_{i=1}^{3} p\left(x_{i}\right) \log p\left(x_{i}\right)=1.5 \text { bit/符号 } \\
> H(\bar{X})=2 H(X)=2 \times 1.5=3 \mathrm{bit} / \text { 序列 }
> \end{array}$

### 离散有记忆信源的序列熵

- 对于**有记忆**信源,就不像无记忆信源那样简单, 它必须引入条件熵的概念, 而且只能在某些特殊情况下才能得到一些有价值的结论。

- 对于由**两个符号**组成的联合信源, 有下列结论:
  $$
  H\left(X_{1} X_{2}\right)=H\left(X_{1}\right)+H\left(X_{2} \mid X_{1}\right)=H\left(X_{2}\right)+H\left(X_{1} \mid X_{2}\right)
  $$

  $$
  H\left(X_{1}\right) \geq H\left(X_{1} \mid X_{2}\right), H\left(X_{2}\right) \geq H\left(X_{2} \mid X_{1}\right)
  $$

- 当前后符号**无依存关系**时,有下列推论:
  $$
  \begin{array}{l}
  H\left(X_{1} X_{2}\right)=H\left(X_{1}\right)+H\left(X_{2}\right) \\
  H\left(X_{1} \mid X_{2}\right)=H\left(X_{1}\right), H\left(X_{2} \mid X_{1}\right)=H\left(X_{2}\right)
  \end{array}
  $$

- 若信源输出一个**L长序列**,则信源的**序列熵**为

  $$
  \begin{aligned}
  H(\overline{\mathrm{X}}) &=H\left(X_{1} X_{2} \cdots X_{L}\right) \\
  &=H\left(X_{1}\right)+H\left(X_{2} \mid X_{1}\right)+\cdots+H\left(X_{L} \mid X_{L-1} \cdots X_{1}\right) \\
  &=\sum_{l}^{L} H\left(X_{l} \mid X^{l-1}\right)=H\left(X^{L}\right)
  \end{aligned}
  $$

- 平均每个符号的熵为：

  $$
  H_{L}(\bar{X})=\frac{1}{L} H\left(X^{L}\right)
  $$

- 若当信源退化为**无记忆**时: 若进一步又满足平稳性时

  $$
  H(\bar{X})=\sum_{l}^{L} H\left(X_{l}\right) \quad H(\bar{X})=L H(X)
  $$

#### 平稳有记忆N次扩展源的熵

设 $\mathbf{X}$  为离散平稳有记忆信源, $\mathbf{X}$  的 $\mathbf{N}$  次扩展源记为 $X^{N}$ ,

$$
X^{N}=\left[X_{1} X_{2} \cdots X_{N}\right]
$$
根据熵的可加性,得
$$
H\left(X^{N}\right)=H\left(X_{1} X_{2} \cdots X_{N}\right)=H\left(X_{1}\right)+H\left(X_{2} / X_{1}\right)+\cdots H\left(X_{N} / X_{1} \cdots X_{N-1}\right)
$$
根据平稳性和熵的不增原理,得$H\left(X^{N}\right) \leq N H\left(X_{1}\right)$, 仅当无记忆信源时等式成立。

对于 $\mathrm{X}$  的 $\mathrm{N}$  次扩展源, 定义平均符号熵为:

$$
H_{N}(X)=\frac{1}{N} H\left(X^{N}\right)=\frac{1}{N} H\left(X_{1} \cdots X_{N}\right)
$$
**信源 $\mathrm{X}$  的极限符号熵定义为：**
$$
H_{\infty}(X)=\lim _{N \rightarrow \infty} \frac{1}{N} H(X^{N})=\lim _{N \rightarrow \infty} \frac{1}{N} H(X_{1} \cdots X_{N})
$$
极限符号熵简称**符号熵**, 也称**熵率**。

定理: 对任意离散平稳信源, 若 $H_{1}(X)<\infty$ , 有:

(1) $H\left(X_{N} / X_{1} \cdots X_{N-1}\right)$ 不随 $\mathbf{N}$而增加;
(2) $H_{N}(X) \geq H\left(X_{N} / X_{1} \cdots X_{N-1}\right) ;$
(3)$H_{N}(X)$ 不随  N  而增加;
(4) $H_{\infty}(X)$ 存在,且 $H_{\infty}(X)=\lim _{N \rightarrow \infty} H(X_{N} / X_{1} \cdots X_{N-1})$

该式表明, 有记忆信源的符号熵也可通过计算极限条件熵得到。





参考文献：

1. Proakis, John G., et al. *Communication systems engineering*. Vol. 2. New Jersey: Prentice Hall, 1994.
2. Proakis, John G., et al. *SOLUTIONS MANUAL Communication Systems Engineering*. Vol. 2. New Jersey: Prentice Hall, 1994.
3. 周炯槃. 通信原理（第3版）[M\]. 北京：北京邮电大学出版社, 2008.
4. 樊昌信, 曹丽娜. 通信原理（第7版） [M\]. 北京：国防工业出版社, 2012.



[返回首页](https://github.com/timerring/information-theory)