- [信源数学模型](#信源数学模型)
  - [离散信源](#离散信源)
  - [连续信源](#连续信源)
    - [单符号离散无记忆信源(DMS, Discrete memoryless source)](#单符号离散无记忆信源dms-discrete-memoryless-source)
    - [单个连续变量信源](#单个连续变量信源)
    - [多维离散无记忆信源](#多维离散无记忆信源)
    - [离散无记忆信源的扩展源](#离散无记忆信源的扩展源)


## 信源数学模型

信源：产生**随机变量、随机序列和随机过程**的信号源。

+ 在通信系统中收信者在未收到消息以前对信源发出什么消息是不确定的，是随机的，所以可用随机变量、随机序列或随机过程来描述信源输出的消息,或者说用一个样本空间及其概率测度——**概率空间**来描述信源

**信源的基本特性:具有随机不确定性。**

香农信息论的基本观点

+ 用**随机变量或随机矢量来表示信源**
+ 用**概率论和随机过程的理论来研究信息**

### 离散信源

用离散随机变量X表示单符号离散信源（一个符号表示一完整消息，符号取值可列)，X的可能取值为信源发出的各种不同符号，X的概率分布为各符号的先验概率。

> 例：信源  X  的取值有 $N$  个, $x_{1}, x_{2}, \ldots, x_{N}$ , 称为信源字符集，各符号概率分布 $P\left(x_{1}\right), P\left(x_{2}\right), \ldots, P\left(x_{n}\right)$  且 $\Sigma_{i} P\left(x_{i}\right)=1$ 

### 连续信源

信源的取值为无穷不可数的连续值,其概率分布用概率密度函数p(x)表示，且

$$
\int_{-\infty}^{\infty} p(x) d x=1
$$

#### 单符号离散无记忆信源(DMS, Discrete memoryless source)

如果信源 $\mathbf{X}$  的符号集 $\mathbf{A}=\{\mathbf{x}_{1}, \ldots, \mathbf{x}_{\mathrm{n}}\}$ , 信源在**离散时间**发出**单个符号**, 且符号发生的概率**相互独立**, 称为单符号离散无记忆信源, **数学模型**为:

$$
\begin{array}{l}
{\left[\begin{array}{l}
X \\
P
\end{array}\right]=\left[\begin{array}{ccc}
x_{1} & \cdots & x_{n} \\
p\left(x_{1}\right) & \cdots & p\left(x_{n}\right)
\end{array}\right]} \\
p\left(x_{i}\right) \geq 0, \quad \sum_{i=1}^{n} p\left(x_{i}\right)=1
\end{array}
$$
其中 $p\left(x_{\mathrm{i}}\right)$  成为符号 $x_{\mathrm{i}}$  的先验概率。

> Example1：一个二元无记忆信源, 符号集  A=\{0,1\} ,  p  为  X=0  的概率,  q  为  X=1  的概率,  q=1-p ; 请写出该信源的模型。
> 解：信源模型为
>
> $\left[\begin{array}{l}
> X \\
> P
> \end{array}\right]=\left[\begin{array}{ll}
> 0 & 1 \\
> p & q
> \end{array}\right]$

#### 单个连续变量信源

$\left[\begin{array}{l}
X \\
P
\end{array}\right]=\left[\begin{array}{c}
x \in(a, b) \\
p(x)
\end{array}\right], \quad \int_{a}^{b} p(x) d x=1$，其中 $p(x) \geq 0$  为信源输出的概率密度函数

#### 多维离散无记忆信源

若一个信源输出是一系列离散的符号, 而每个符号又是随机的, 即信源输出为一系列随机变量 (随机矢量）, 从而信源的输出可用  L  维随机矢量 $\left[X_{1}, X_{2}, \ldots, X_{L}\right]$  来描述, 其中 $\boldsymbol{L}$  为有限正整数或可数 的无限值。

上述随机矢量中, 若每个随机变量 $X_{i}(\boldsymbol{i}=1,2, \ldots, L)$  都是离散的, 则可用  L  维离散概率空间来描述这类信源。

即若 $\boldsymbol{L}$  维随机矢量 $X=\left[X_{1} X_{2} \ldots X_{L}\right], X_{\mathrm{i}}$  的具体取值为 $x \in\left(a_{1}, a_{2}, \ldots a_{n},\right)$ , 对应概率为 $P_{X}(x)=P\left(x_{1} x_{2} \ldots x_{L}\right)$  为 $\boldsymbol{L}$  维联合概率分布, 则该信源的数学模型为

$$
\begin{array}{l}
\left(\begin{array}{c}
X^{L} \\
P(x)
\end{array}\right)
=\left(\begin{array}{ccccc}
\left(a_{1} a_{1} \ldots a_{1}\right) & \ldots & \left(a_{1} a_{2 \ldots} a_{m}\right) & \ldots & \left(a_{n} a_{n} \ldots a_{n}\right) \\
P\left(a_{1} a_{1} \ldots a_{1}\right) & \ldots & P\left(a_{1} a_{2 \ldots} a_{m}\right) & \ldots & P\left(a_{n} a_{n} \ldots a_{n}\right)
\end{array}\right)
\end{array}
$$
其中离散消息序列长度为 $\boldsymbol{L}$ , 序列每符号有 $\boldsymbol{n}$  种取值, 整个消息序列共有 $n^{L}$  种取值。

当输出序列中的前后消息（符号）相互**统计独立**, 且具有**相同的概率分布,** 则  L  维随机矢量的联合概率分布满足

$$
P(X)=\prod_{i=1}^{L} P\left(X_{i}=x_{\boldsymbol{j}}\right), \boldsymbol{j}=1,2, \ldots, n
$$
即 $\boldsymbol{L}$  维随机矢量的联合概率分布可用随机矢量中单个随机变量的概率乘积来表示。这种信源为**离散无记忆信源**。

#### 离散无记忆信源的扩展源

设信源为 $\mathrm{X}$ , 则由 $\mathrm{X}$  构成  N  维随机矢量集合 $\mathbf{X}^{N}=\left[X_{1} X_{2} \ldots X_{N}\right], \quad\left(\right.$  其中 $\mathbf{X}_{\mathbf{i}}$  与 $\mathbf{X}$  同分布, 取自同一信源  X  ），称为**信源 $\mathrm{X}$  的  N  次扩展源**。

> Example2：求例1中信源的二次扩展源模型：
> $\mathbf{E x} 1$  的二元无记忆信源模型为
>
> $\left[\begin{array}{l}
> X \\
> P
> \end{array}\right]=\left[\begin{array}{ll}
> 0 & 1 \\
> p & q
> \end{array}\right]$
>
> 其二次扩展信源为
> $\left[\begin{array}{l}X^{2} \\ p(\alpha)\end{array}\right]=\left[\begin{array}{llll}\alpha_{1}(00) & \alpha_{2}(01) & \alpha_{3}(10) & \alpha_{4}(11) \\ p\left(\alpha_{1}\right) & p\left(\alpha_{2}\right) & p\left(\alpha_{3}\right) & p\left(\alpha_{4}\right)\end{array}\right] \\
> p\left(\alpha_{1}\right)=p^{2}, p\left(\alpha_{2}\right)=p(1-p)=p\left(\alpha_{3}\right) 
> p\left(\alpha_{4}\right)=(1-p)^{2}$ 



一个离散无记忆信源的 $\mathbf{N}$  次扩展信源描述如下：

设 $\mathbf{X}$  为离散无记忆信源, 则 $\mathbf{X}$  的 $\mathbf{N}$  次扩展信源记为$\mathbf{X}^{N} ,  \mathbf{X}^{N}=\left[X_{1} X_{2} \ldots X_{N}\right]$ , 其模型为

$$
\left(\begin{array}{c}
\mathbf{X}^{N} \\
P
\end{array}\right)=\left(\begin{array}{ccc}
a_{1} & \cdots & a_{M} \\
p\left(a_{1}\right) & \cdots & p\left(a_{M}\right)
\end{array}\right)
$$
每个 $X_{i}$  取自同一个字母表 $A=\{a_{1}, a_{2}, \ldots, a_{N}\}$ , 且 $X_{i}$  与 $\mathbf{X}$  同分布，因此, $\mathbf{X}^{\mathrm{N}}$  的符号集为 $A^{N}=\{\boldsymbol{a}_{1}, \ldots, \boldsymbol{a}^{N}\}, \boldsymbol{a}_{j}$  为多维信源中的一个矢量, 即 $a_{j} \in A^{N}$ , 矢量的个数为$n^{N}$,$\boldsymbol{a}_{\boldsymbol{j}}=\left(a_{j_{1}} a_{j_{2}, \ldots,}, a_{j N}\right)$,$a_{j k}$  为 $\boldsymbol{a}_{j} $的第 $\mathbf{k}$  个分量, 且 $p\left(\boldsymbol{a}_{j}\right)=\prod_{k=1}^{N} p_{j k}$  ,$p_{j k}$  为第 $\mathrm{j}$  个矢量第 $\mathrm{k}$  个分量取符号 $\boldsymbol{a}_{\mathrm{jk}}$  的概率。



参考文献：

1. Proakis, John G., et al. *Communication systems engineering*. Vol. 2. New Jersey: Prentice Hall, 1994.
2. Proakis, John G., et al. *SOLUTIONS MANUAL Communication Systems Engineering*. Vol. 2. New Jersey: Prentice Hall, 1994.
3. 周炯槃. 通信原理（第3版）[M\]. 北京：北京邮电大学出版社, 2008.
4. 樊昌信, 曹丽娜. 通信原理（第7版） [M\]. 北京：国防工业出版社, 2012.



[返回首页](https://github.com/timerring/information-theory)