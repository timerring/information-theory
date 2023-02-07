- [信息率失真函数](#信息率失真函数)
- [平均互信息再讨论](#平均互信息再讨论)
  - [信道容量](#信道容量)
  - [信息率失真函数](#信息率失真函数-1)


### 信息率失真函数

Theorem [Rate-Distortion]. 以小于或等于失真  D  去重构无记忆信源所需的最小信源输出 bit/sym 称为率失真函数 (rate-distortion function)，用  R(D)  表示, 记为


$$
R(D)=\min _{p\left(x^{\prime} \mid x\right) \mathrm{P}_{\mathrm{D}}\left(X, X^{\prime}\right) \leq D} I\left(X ; X^{\prime}\right)
$$


若平均失真度  $\bar{D}$  不大于我们所允许的失真,即 $\bar{D} \leq D$，则称此为**保真度准则**。

当信源  $p\left(x_{i}\right)$  给定, 单个符号失真度  $d\left(x_{i},y_{j}\right)$  给定时, 选择不同的试验信道  $p\left(y_{j} \mid x_{i}\right)$ , 相当于不同的编码方法, 其所得的平均失真度不同。

试验信道


$$
\left\{\begin{array}{l}
\bar{D} \leq D  \text { 满足保真度准则 }\\
\bar{D}>D
\end{array}\right.
$$


满足  $\bar{D} \leq D$  条件的所有转移概率分布  $p_{i j}$  构成了一个信道集合


$$
P_{D}=\{p(b_{j} \mid a_{i}): \bar{D} \leq D\}
$$



+ **D失真允许的试验信道: 满足保真度准则的试验信道。**
+ $\mathbf{P}_{\mathrm{D}}$  : **所有D失真允许的试验信道组成的一个集合。**

$\mathbf{R}(\mathbf{D}) $ : 在限定失真为  $\mathbf{D}$  的条件下信源输出的最小信息速率。


$$
R(D)=\min _{P_{D}} I(X, Y)
$$


在信源给定后,我们希望在满足一定失真的情况下,使信源必须传输给收信者的信息传输率  R  尽可能地小。若从接收端来着, 就是在满足保真度准则下, 寻找再**现信源消息所必须获得的最低平均信息量**。即在**满足保真度准则的条件下寻找平均互信息  $\mathrm{I}(\mathrm{X}, \mathrm{Y})$  的最小值。**

 $\mathbf{P}_{\mathbf{D}}$  是所有满足保真度准则的试验信道集合,因而可以在集合 $\mathbf{P}_{\mathbf{D}}$ 中寻找某一个信道 $p_{ij}$ , 使 $\mathrm{I}(\mathrm{X}, \mathrm{Y})$ 取极小值。

对于离散无记忆信源


$$
R(D)=\min _{p_{j i} \in P_{D}} \sum_{i} \sum_{j} p\left(a_{i}\right) p\left(b_{j} \mid a_{i}\right) \log \frac{p\left(b_{j} \mid a_{i}\right)}{p\left(b_{j}\right)}
$$



> 例 已知编码器输入的概率分布为  $p(x)=\{0.5,0.5\}$ , 信道矩阵
>
> (1)  $p_{i j}=\left[\begin{array}{ll}0.6 & 0.4 \\ 0.2 & 0.8\end{array}\right]$  ;  (2)  $p_{i j}=\left[\begin{array}{ll}0.9 & 0.1 \\ 0.2 & 0.8\end{array}\right]$ 
>
> 求互信息
>
> ![](https://raw.githubusercontent.com/timerring/picgo/master/picbed/image-20230207134043576.png)
>
> (1) 
> $$
> \begin{array}{l}
> \because p\left(x_{i} y_{j}\right)=p\left(x_{i}\right) p\left(y_{j} \mid x_{i}\right) \\
> \therefore p\left(x_{1} y_{1}\right)=0.3 p\left(x_{1} y_{2}\right)=0.2 p\left(x_{2} y_{1}\right)=0.1 p\left(x_{2} y_{2}\right)=0.4 \\
> p\left(y_{1}\right)=0.4 p\left(y_{2}\right)=0.6 \\
> p\left(x_{1} \mid y_{2}\right)=\frac{3}{4} p\left(x_{1} \mid y_{2}\right)=\frac{1}{3} p\left(x_{2} \mid y_{1}\right)=\frac{1}{4} p\left(x_{2}\mid y_{2}\right)=\frac{2}{3} \\
> \quad I(X ; Y)=\sum_{i} \sum_{j} p\left(x_{i} y_{j}\right) \log \frac{p\left(x_{i} \mid y_{j}\right)}{p\left(x_{i}\right)}=0.125 \text { bit } / \text { 符号 }
> \end{array}
> $$
> (2)
> $$
> I(X ; Y)=\sum_{i} \sum_{j} p\left(x_{i} y_{j}\right) \log \frac{p\left(x_{i} \mid y_{j}\right)}{p\left(x_{i}\right)}=0.397 b i t / \text { 符号 }
> $$

可见当  $\boldsymbol{p}(\boldsymbol{x})$  一定时,  $I(X, Y)$  随  $p\left(y_{j} \mid x_{i}\right)$  而变。因为  $p(x)$  分布一定时,信道受干扰不同，所能传递的信息量是一定时,  $I(X, Y)$  是关于  $p\left(y_{j} \mid x_{i}\right)$  的下凸函数。因此当改变  $p\left(y_{j} \mid x_{i}\right)$  时,  $I(X, Y)$  有一极小值。

### 平均互信息再讨论

平均互信息  $I(X ; Y)$: 

+ 信源的概率分布  $p\left(x_{i}\right)$  的上凸函数。
+ 信道传递概率  $p\left(y_{j} \mid x_{i}\right)$  的下凸函数。
  

#### 信道容量

$$
C=\max _{p\left(x_{i}\right)} I(X ; Y)
$$

+ 假定信道固定的前提下，选择一种试验信源使信息传输率最大。
+ 它所反映的是信道传输信息的能力,是信道可靠传送的最大信息传输率。

一旦找到了信道容量，它就与信源不再有关，而是信道特性的参量，**随信道特性的变化而变化，不同的信道其信道容量不同**。

+ 研究目的：充分利用已给信道，使传输的信息量最大，而发生错误的概率任意小。

#### 信息率失真函数

$$
R(D)=\min _{P_{D}} I(X ; Y)
$$

**假定信源给定的情况下，用户可以容忍的失真度内再现信源消息所必须获得的最小平均信息量。它反映的是信源可以压缩的程度，是在满足一定失真度要求下信源可压缩的最低值。**

+ 率失真函数一旦找到，就与求极值过程中选择的试验信道不再有关，而只是信源特性的参量
+ 不同的信源其R(D)不同。

+ 研究目的：解决在已知信源和允许失真度D的条件下，使信源必须传送给信宿的信息率最小。即用尽可能少的码符号尽快地传送尽可能多的信源消息，以提高通信的有效性。



例: 设信源的符号表为  $\mathrm{A}=\{a_{1}, a_{2}, \ldots, a_{2 n}\}$ ,概率分布为  $p(a_{\mathrm{i}})=1 / 2 \mathrm{n}$, $i=1,2 \ldots 2 n$ , 失真函数规定为


$$
d\left(a_{i}, a_{j}\right)=\left\{\begin{array}{ll}
0 & i=j \\
1 & i \neq j
\end{array}\right.
$$


即不发生差错时失真为0 , 出错失真为1 。研究 在一定编码条件下信息压缩的程度。

解：信源熵：


$$
H\left(\frac{1}{2 n}, \frac{1}{2 n} \cdots \frac{1}{2 n}\right)=\log 2 n
$$


如果对信源进行无失真编码, **平均每个符号至少需要  $\log 2 \mathrm{n}$  个二进制码元**。

现在假定允许有一定失真,失真度为D=1/2，设想采用下面的编码方案;
$$
\begin{array}{l}
a_{1} \rightarrow a_{1}, \quad a_{2} \rightarrow a_{2}, \quad \ldots a_{\mathrm{n}} \rightarrow a_{\mathrm{n}} \\
a_{\mathrm{n}+1} \rightarrow a_{\mathrm{n}}, a_{\mathrm{n}+2} \rightarrow a_{\mathrm{n}}, \ldots a_{2 \mathrm{n}} \rightarrow a_{\mathrm{n}}
\end{array}
$$
![](https://raw.githubusercontent.com/timerring/picgo/master/picbed/image-20230207142053477.png)

则平均失真
$$
\bar{D}=\sum_{i} \sum_{j} p\left(a_{i}\right) p\left(a_{j} \mid a_{i}\right) d\left(a_{i}, a_{j}\right)=\frac{1}{2}
$$
它是一个确定信道
$$
\begin{aligned}
p\left(a_{j} \mid a_{i}\right) & =\boldsymbol{p}_{\mathrm{ij}}=\mathbf{1}(\text { 或 } \mathbf{0}), \boldsymbol{H}(\boldsymbol{Y} \mid \boldsymbol{X})=\mathbf{0} \\
& I(X, Y)=H(Y)-H(Y \mid X)=H(Y)
\end{aligned}
$$
则输出熵  H(Y) 
$$
\begin{array}{l}
H(Y)=H\left(\frac{1}{2 n}, \frac{1}{2 n} \cdots \frac{1}{2 n}, \frac{1+n}{2 n}\right) \\
=\log 2 n-\frac{n+1}{2 n} \log (n+1)
\end{array}
$$
比如:  $\mathbf{N}=\mathbf{8}$ , 则  $H(\mathrm{X})=\mathbf{4 b i t / s y m b o l}$ ,  $I(X, Y)=H(Y)=\mathbf{2 . 2 2 b i t} /  symbol$



> 已知信源符号x = 0.5,经过信道传输后变为y = 1.5,若采用汉明失真作为两个符号的失真度量，则d(x, y)= 1



参考文献：

1. Proakis, John G., et al. *Communication systems engineering*. Vol. 2. New Jersey: Prentice Hall, 1994.
2. Proakis, John G., et al. *SOLUTIONS MANUAL Communication Systems Engineering*. Vol. 2. New Jersey: Prentice Hall, 1994.
3. 周炯槃. 通信原理（第3版）[M\]. 北京：北京邮电大学出版社, 2008.
4. 樊昌信, 曹丽娜. 通信原理（第7版） [M\]. 北京：国防工业出版社, 2012.



[返回首页](https://github.com/timerring/information-theory)