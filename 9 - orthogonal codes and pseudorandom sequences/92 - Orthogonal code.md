- [正交编码](#正交编码)
  - [正交编码的基本概念](#正交编码的基本概念)
    - [正交性](#正交性)
    - [互相关系数](#互相关系数)
    - [正交编码](#正交编码-1)
    - [自相关系数](#自相关系数)
    - [超正交码](#超正交码)
    - [双正交编码](#双正交编码)
  - [正交沃尔什函数](#正交沃尔什函数)
    - [离散沃尔什函数的构成](#离散沃尔什函数的构成)
    - [沃尔什函数的基本性质](#沃尔什函数的基本性质)


## 正交编码

### 正交编码的基本概念

#### 正交性

若两个周期为  T  的模拟信号  $s_{1}(t)$  和  $s_{2}(t)$  互相正交, 则有
$$
\int_{0}^{T} s_{1}(t) s_{2}(t) d t=0
$$
同理, 若  M  个周期为  T  的模拟信号  $s_{1}(t)$, $s_{2}(t)$, $\ldots$, $s_{M}(t)$  构成一个正交信号集合，则有
$$
\int_{0}^{T} s_{i}(t) s_{j}(t) d t=0 \quad i \neq j ; \quad i, j=1,2, \ldots, M
$$




#### 互相关系数

对于二进制数字信号, 用一数字序列表示码组。这里, 我们只讨论二进制且码长相同的编码。这时, 两个码组的正交性可用如下形式的互相 关系数来表述。

设长为  $\boldsymbol{n}$  的编码中码元只取值  +1  和  -1 , 假设  $\boldsymbol{x}$  和  $\boldsymbol{y}$  是其中两个码组:
$$
x=(x_{1}, x_{2}, x_{3}, \cdots, x_{n}) \quad y=(y_{1}, y_{2}, y_{3}, \cdots, y_{n})
$$
其中:  $x_{i}, y_{i} \in(+1,-1), \quad i=1,2, \cdots, n$ 

若码组  x  和  y  正交, 则必有  $\rho(x, y)=0$  。
$$
\rho(x, y)=\frac{1}{n} \sum_{i=1}^{n} x_{i} y_{i}
$$

#### 正交编码

例如, 右图所示 4 个数字信号可以看作是如下4 个码组:


$$
\{\begin{array}{l}
s_{1}(t):(+1,+1,+1,+1) \\
s_{2}(t):(+1,+1,-1,-1) \\
s_{3}(t):(+1,-1,-1,+1) \\
s_{4}(t):(+1,-1,+1,-1)
\end{array}.
$$


按照互相关系数定义式计算容易得知, 这 4 个码组中任意两者之间的相关系数都为 0 , 即这 4 个码组两两正交。我们把这种两两正交的编码称为**正交编码**。

用二进制数字表示互相关系数

在二进制编码理论中, 常采用二进 制数字 “ 0 ”和 “ 1 ”表示码元的可能 取值。这时, 若规定用二进制数字 “0”代替上述码组中的 “+ 1 ”, 用 二进制数字 “ 1 ”代替 “  -1  ”, 则上 述互相关系数定义式将变为
$$
\rho(x, y)=\frac{A-D}{A+D}
$$
式中,  A——x  和  y  中对应码元相同的个数;

 D—— x  和  y 中对应码元不同的个数。

例如, 按照左式规定, 上面例 子可以改写成


$$
\{\begin{array}{l}
s_{1}(t):(0,0,0,0) \\
s_{2}(t):(0,0,1,1) \\
s_{3}(t):(0,1,1,0) \\
s_{4}(t):(0,1,0,1)
\end{array}.
$$


可以验证互相关系数  $\boldsymbol{\rho}=\mathbf{0}$ .

#### 自相关系数

上式中, 若用  x  的  j  次循环移位代替  y , 就得到  x  的自相关系数  $\rho_{x}(j)$  。 具体地讲，令
$$
\begin{array}{l}
x=(x_{1}, x_{2}, \cdots, x_{n}) \\
y=(x_{1+j}, x_{2+j}, \cdots, x_{n}, x_{1}, x_{2}, \cdots x_{j})
\end{array}
$$
代入定义式
$$
\rho(x, y)=\frac{A-D}{A+D}
$$


就得到自相关系数  $\rho_{x}(j)$  :
$$
\rho_{x}(j)=(A-D) / n
$$
类似上述互相关系数的定义, 可以对于一个长为  n  的码组  x  定义其自相关系数为
$$
\rho_{x}(j)=\frac{1}{n} \sum_{i=1}^{n} x_{i} x_{i+j}, \quad j=0,1, \cdots,(n-1)
$$
式中,  x  的下标按模  n  运算, 即有 $ x_{n+k} \equiv \mathbf{x}_{k} $ 。例如, 设


$$
x=(x_{1}, x_{2}, x_{3}, x_{4})=(+1,-1,-1,+1)
$$
则有
$$
\begin{array}{l}
\rho_{x}(0)=\frac{1}{4} \sum_{i=1}^{4} x_{i}^{2}=1\\
\rho_{x}(1)=\frac{1}{4} \sum_{i=1}^{\overline{\overline{4}}^{4}} x_{i} x_{i+1}=\frac{1}{4}(x_{1} x_{2}+x_{2} x_{3}+x_{3} x_{4}+x_{4} x_{1})=\frac{1}{4}(-1+1-1+1)=0 \\
\rho_{x}(2)=\frac{1}{4} \sum_{i=1}^{1} x_{i} x_{i+2}=\frac{1}{4}(x_{1} x_{3}+x_{2} x_{4}+x_{3} x_{1}+x_{4} x_{2})=-1 \\
\rho_{x}(3)=\frac{1}{4} \sum_{i=1}^{\overline{4}^{1}} x_{i} x_{i+3}=\frac{1}{4}(x_{1} x_{4}+x_{2} x_{1}+x_{3} x_{2}+x_{4} x_{3})=0
\end{array}
$$


#### 超正交码

超正交码：相关系数  $\rho$  的取值范围在  $\pm 1$  之间, 即有 $ -1 \leq \rho \leq+1$  。 若两个码组间的相关系数  $\rho<0$ , 则称这两个码组互相超正交。如果一种编码中任两码组间均超正交, 则称这种编码为超正交码。

例如, 在上例中, 若仅取后 3 个码组, 并且删去其第一位, 构成如下新的编码:


$$
\{\begin{array}{l}
s_{1}{ }^{\prime}(t):(0,1,1) \\
s_{2}{ }^{\prime}(t):(1,1,0) \\
s_{3}{ }^{\prime}(t):(1,0,1)
\end{array}.
$$


则不难验证, 由这 3 个码组所构成的编码是超正交码。

#### 双正交编码

由正交编码和其反码便可以构成双正交编码。

例：上例中

正交码为 


$$
\{\begin{array}{l}s_{1}(t):(0,0,0,0) \\ s_{2}(t):(0,0,1,1) \\ s_{3}(t):(0,1,1,0) \\ s_{4}(t):(0,1,0,1)\end{array}
$$


其反码为


$$
\{\begin{array}{l}(1,1,1,1) \\ (1,1,0,0) \\ (1,0,0,1) \\ (1,0,1,0)\end{array}
$$


上两者的总体即构成如下双正交码:

 $(0,0,0,0) \quad(1,1,1,1) \quad(0,0,1,1) \quad(1,1,0,0)(0,1,1,0) \quad(1,0,0,1) \quad(0,1,0,1) \quad(1,0,1,0)$ 

此码共有 8 种码组, 码长为 4 。

### 正交沃尔什函数

沃尔什(Walsh)函数集是完备的非正弦型的二元（取值为+1与-1）正交函数集, 其相应的离散沃尔什函数简称为沃尔什序列或沃尔什码。 沃尔什函数是定义在半开区间  [0,1)  的矩形波族, 每个矩形波有一个编号  n($n=0,1,2,3, \ldots$)  。

矩形波幅度的取值为  +1  或  -1 , 规定起始时矩形波的取值为  +1 , 然后在  +1  与  -1  之间变化, 变化的次数  (+1  变  -1  与  -1  变  +1  的次数之和）  $m=n$ , 在  +1  或  -1  上持续的时间可以相等, 也可以不相等 (不相等时较长的持续时间  $T_{1}$  为较短的持续时间  $T_{\mathrm{s}}$  的两倍）。 编号为  n  的沃尔什函数用  $\mathrm{Wal}(n, t)$  表示, 沃尔什函数的波形如图所示。

![](https://raw.githubusercontent.com/timerring/picgo/master/picbed/image-20230211102942436.png)

补充（度量空间）的完备性定义:

度量空间  $X=(X, d)$  中的序列  $(x_{n})$ , 如果对任意给定的 $ \varepsilon \gt 0 $, 都存在一个  $\mathrm{N}=\mathrm{N}(\varepsilon)$ , 使得对每个  $\mathrm{m}$, $\mathrm{n}>\mathrm{N}$  都有
$$
\mathrm{d}(\mathrm{x}_{\mathrm{m}}, \mathrm{x}_{\mathrm{n}})<\varepsilon
$$
则称它是一个柯西序列。如果空间  X  中的每个柯西序列都收敛, 则称  X  是完备的。

一个完备的函数集, 应该能表示出其空间上的所有函数。

#### 离散沃尔什函数的构成

离散沃尔什函数也称沃尔什序列或沃尔什码, 用哈达马矩阵的行(或列)可以构成离散沃尔什函数

一阶哈达马矩阵为
$$
H_{1}=\text { [1] }
$$
高阶哈达马矩阵的递推公式如下:
$$
H_{N_{m}}=[\begin{array}{rr}
H_{N_{m-1}} & H_{N_{m-1}} \\
H_{N_{m-1}} & -H_{N_{m-1}}
\end{array}]
$$
式中,  $N_{m}=2^{m}$, $m=1,2,3, \ldots$  。

例如,  m=1  时
$$
\begin{array}{c}
H_{N_{1}}=H_{2}=[\begin{array}{rr}
H_{1} & H_{1} \\
H_{1} & -H_{1}
\end{array}]=[\begin{array}{rr}
1 & \mathbf{1} \\
\mathbf{1} & \mathbf{- 1}
\end{array}] \\
H_{N_{2}}=H_{4}=[\begin{array}{rr}
H_{2} & H_{2} \\
H_{2} & -H_{2}
\end{array}]=[\begin{array}{rrrr}
1 & \mathbf{1} & \mathbf{1} & \mathbf{1} \\
\mathbf{1} & \mathbf{1} & \mathbf{1} & -\mathbf{1} \\
\mathbf{1} & \mathbf{1} & \mathbf{- 1} & -\mathbf{1} \\
\mathbf{1} & \mathbf{- 1} & -\mathbf{1} & \mathbf{1}
\end{array}]
\end{array}
$$
![](https://raw.githubusercontent.com/timerring/picgo/master/picbed/image-20230211103701709.png)

 m=3  时
$$
\begin{array}{c}
H_{N_{3}}=H_{8} \\
=[\begin{array}{rr}
H_{4} & H_{4} \\
H_{4} & -H_{4}
\end{array}]=[\begin{array}{cccccccc}
1 & 1 & 1 & 1 & 1 & 1 & 1 & 1 \\
1 & -1 & 1 & -1 & 1 & -1 & 1 & -1 \\
1 & 1 & -1 & -1 & 1 & 1 & -1 & -1 \\
1 & -1 & -1 & 1 & 1 & -1 & -1 & 1 \\
1 & 1 & 1 & 1 & -1 & -1 & -1 & -1 \\
1 & -1 & 1 & -1 & -1 & 1 & -1 & 1 \\
1 & 1 & -1 & -1 & -1 & -1 & 1 & 1 \\
1 & -1 & -1 & 1 & -1 & 1 & 1 & -1
\end{array}]
\end{array}
$$
 N_{m}  阶哈达马矩阵的通式可表示为
$$
H_{N_{m}}=[\begin{array}{ccccc}
h_{11} & h_{12} & h_{13} & \cdots & h_{1 N_{m}} \\
h_{21} & h_{22} & h_{23} & \cdots & h_{2 N_{m}} \\
\vdots & & & \vdots \\
h_{N_{m} 1} & h_{N_{m} 2} & h_{N_{m} 3} & \cdots & h_{N_{m} N_{m}}
\end{array}]
$$
式中, $ N_{m}=2^{m}, m=1,2,3, \ldots, h_{i k} \in(+1,-1)$ 
用哈达马矩阵  $H_{N m} $ 的行 (或列)可以构成离散沃尔什函数  $W a l[i, t]$ , 它们的对应关系如下:




$$
\begin{array}{c}
\operatorname{Wal}[i, t]=\sum_{k=1}^{N m} h_{i k} g(t-(k-1) T_{c}) \\
g(t)=\{\begin{array}{c}
1,0 \leq t \leq T_{c} \\
0, \text { others }
\end{array}
\end{array}
$$





#### 沃尔什函数的基本性质

(1) 在半开区间  [0,1)  上正交, 即


$$
\int_{0}^{1} \operatorname{wal}(i, t) \operatorname{wal}(j, t) \mathrm{d} t=\{\begin{array}{cc}
1, & i=j \\
0, & i \neq j
\end{array} \quad i, j=0,1,2, \cdots.
$$


该性质为沃尔什函数基本性质中最重要的性质。

(2) 除  $\mathrm{Wal}(0, t)$  外，其他  $\mathrm{Wal}(n, t)$  在半开区间  [0,1)  上的均值为 0 .

(3) 两个沃尔什函数相乘仍为沃尔什函数，即
$$
\operatorname{Wal}(i, t) \operatorname{Wal}(j, t)=\operatorname{Wal}(kt)
$$
这表示沃尔什函数对于乘法是自闭的。

(4) 沃尔什函数集是完备的, 即长度为  $\mathrm{N}$  的离散沃尔什函数 (沃尔什序列)一共有  $\mathrm{N}$  个。

(5) 沃尔什函数在同步时是完全正交的。

(6) 沃尔什函数在不同步时, 其自相关和互相关特性均不理想, 并随同步误差值的增大而快速恶化。

(7) 同长度不同编号的walsh函数的频带宽度不同。





参考文献：

1. Proakis, John G., et al. *Communication systems engineering*. Vol. 2. New Jersey: Prentice Hall, 1994.
2. Proakis, John G., et al. *SOLUTIONS MANUAL Communication Systems Engineering*. Vol. 2. New Jersey: Prentice Hall, 1994.
3. 周炯槃. 通信原理（第3版）[M\]. 北京：北京邮电大学出版社, 2008.
4. 樊昌信, 曹丽娜. 通信原理（第7版） [M\]. 北京：国防工业出版社, 2012.



[返回首页](https://github.com/timerring/information-theory)
