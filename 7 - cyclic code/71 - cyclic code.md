- [循环码](#循环码)
  - [循环码的特点](#循环码的特点)
  - [基本概念](#基本概念)
  - [循环码的多项式描述](#循环码的多项式描述)
    - [多项式的加法和乘法运算 GF (2)](#多项式的加法和乘法运算-gf-2)
    - [多项式的模运算](#多项式的模运算)


# 循环码

能够识记循环码的基本概念;

能够说明循环码生成多项式的特点;

能够应用多项式运算完成循环码（系统型和非系统型)的编译码;

能根据生成多项式求出循环码的生成矩阵（系统型和非系统型）;

能够解释循环码的编译码电路;

了解循环冗余校验(CRC) ，BCH和RS三种线性循环码

## 循环码的特点

1.可以用**线性反馈移位寄存器**很容易地实现编码和伴随式计算;

2.由于循环码有许多固有的代数结构，从而可以找到各种简单实用的译码方法。

由于循环码具有很多的良好性质，所以它在理论和实践中都很重要。

## 基本概念

定义: 设  $\mathrm{C}$  是某  ($\boldsymbol{n}, \boldsymbol{k}$)  线性分组码的码字集合, 如果对任何
$$
\mathbf{c}=(c_{n-1}, c_{n-2}, \cdots, c_{0}) \in \mathbf{C}
$$
它的循环移位(左移)
$$
\mathbf{c}^{(1)}=(c_{n-2}, c_{n-3}, \cdots, c_{0}, c_{n-1})
$$
也属于  $\mathrm{C}$ , 则称该  ($\boldsymbol{n}, \boldsymbol{k}$)  码为循环码。

同理, 左移  i  位
$$
\mathbf{c}^{(i)}=(c_{n-i-1}, c_{n-i-2}, \cdots, c_{0}, c_{n-1}, \ldots, c_{n-i})
$$
仍是这个循环码的一个码字。

> 下面A、B、C、D四个码集，哪个码集是循环码? A
>
> 提示:先判断是否线性分组码，再看是否符合循环特性
>
> A. (000,110,101,011)
>
> B. (000,010,101,111)
>
> C. (001,110,101,111)
>
> D. (000,010,100,001)

## 循环码的多项式描述

对任意一个长为  $n$  的码字
$$
\mathbf{c}=(c_{n-1}, c_{n-2}, \cdots, c_{1}, c_{0}) \in \mathbf{C}
$$
可用一多项式来表示, 称其为码多项式:
$$
c(x)=c_{n-1} x^{n-1}+c_{n-2} x^{n-2}+\cdots+c_{1} x+c_{0}
$$




$$
\begin{array}{l}
\mathrm{C}=(c_{n-1}, c_{n-2}, \ldots, c_{1}, c_{0}) \\
\lt C(x)=c_{n-1} x^{n-1}+c_{n-2} x^{n-2}+\ldots+c_{1} x+c_{0}
\end{array}
$$



 $\boldsymbol{c}_{i}$  是多项式的系数, 一切系数的运算均是在  $\boldsymbol{G F}(2)$  上的运算。

多项式的阶数一系数不为 0 的  x  的最高幂次:
$$
\operatorname{deg} c(x) \leq n-1
$$


### 多项式的加法和乘法运算 GF (2) 

加法
$$
\begin{array}{l}
u(x)=u_{2} x^{2}+u_{1} x+u_{0}, g(x)=g_{1} x+g_{0} \\
u(x)+g(x)=(u_{2}+0) x^{2}+(u_{1}+g_{1}) x+(u_{0}+g_{0})
\end{array}
$$
乘法
$$
\begin{array}{l}
u(x) g(x) \\
=u_{2} g_{1} x^{3}+(u_{2} g_{0}+u_{1} g_{1}) x^{2}+(u_{1} g_{0}+u_{0} g_{1}) x+u_{0} g_{0}
\end{array}
$$
写成矩阵形式
$$
c=(u_{2}, u_{1}, u_{0})(\begin{array}{llll}
g_{1} & g_{0} & 0 & 0 \\
0 & g_{1} & g_{0} & 0 \\
0 & 0 & g_{1} & g_{0}
\end{array})=(u_{2} g_{1},(u_{2} g_{0}+u_{1} g_{1}),(u_{1} g_{0}+u_{0} g_{1}), u_{0} g_{0})
$$
例:  
$$
\begin{array}{l}
(x^{6}+x^{2}+1)+(x^{3}+x^{2})\\
=x^{6}+x^{3}+(1+1) x^{2}+1 \\
=x^{6}+x^{3}+1
\end{array}
$$
基本多项式关系
$$
\begin{array}{c}
(x+1)^{2}=x^{2}+1 \\
(x+1)(x^{3}+x+1)(x^{3}+x^{2}+1)=x^{7}+1 \\
(x+1)(x^{n-1}+x^{n-2}+\cdots+x+1)=x^{n}+1
\end{array}
$$


### 多项式的模运算

模  $\mathbf{N}$  运算：  $M / N=Q+R / N \quad 0 \leq R \lt N$ ; 其中  M, N  为 正 整数,  $\mathbf{Q}$  为整数, 则在模  $\mathbf{N}$  运算下, 有  $M \equiv \mathbf{R}$  （模  $\mathbf{N} $, 记为  $\bmod \mathbf{N}$  )

例 :  $14 \equiv 2(\bmod 12)$, $1+1=2 \equiv 0 (mod 2)$, $3+2=5   \equiv 1(\bmod 2)$, $5 \times 4=20 \equiv 0(\bmod 2)$ 



给定任意两个系数在  $G F(2) $ 上的多项式  a(x)  和  p(x) , 一定存在有唯一的多项式  Q(x)  和  r(x) , 使
$$
a(x)=Q(x) p(x)+r(x)
$$
称  Q(x)  是  a(x)  除以  p(x)  的商式,  r(x)  是  a(x)  除以  p(x)  的余式， 在模  p(x)  运算下,
$$
a(x) \equiv r(x) \quad[\bmod p(x)]
$$
记  a(x)  除以  p(x)  的余式为  $r(x)=[a(x)] \bmod p(x)$ , 其中
$$
0 \leq \operatorname{deg} r(x)<\operatorname{deg} p(x) \text {, 或 } r(x)=0
$$


> $x^6$被$x^3+x+1$除，求余式
>
> 注:GF(2)的运算中，用加法代替减法。
>
> 计算过程省略：$r(x) = x^2 + 1$

对于任意多项式  a(x) 、 b(x)  和  p(x) , 可以证明


$$
\{b(x)[a(x)]_{\bmod p(x)}\}_{\bmod p(x)}=[b(x) \cdot a(x)]_{\bmod p(x)}
$$



若：



$$
\begin{array}{c}
a(x)=x^{7}+x+1 \\
b(x)=x^{2}+1 \\
p(x)=x^{3}+x+1
\end{array}
$$


请验证上式。余式=1。



对于  (n, k)  循环码, 若  c(x)  对应码字
$$
\mathbf{c}=(c_{n-1}, c_{n-2}, \ldots, c_{1}, c_{0}),
$$




 $\boldsymbol{c}^{(1)}(\boldsymbol{x})$  对应  $\boldsymbol{c}$  的一次移位  $\mathbf{c}^{(1)}=(c_{n-2}, \ldots, c_{1}, c_{0}, c_{n-1})$ , 对  $c^{(i)}(x)$  对应  c  的  i  次移位  $c^{(i)}$  ，则
$$
\begin{array}{c}
c^{(1)}(x)=[x c(x)] \bmod (x^{n}+1) \\
c^{(i)}(x)=[x^{i} c(x)] \bmod (x^{n}+1)
\end{array}
$$
证：


$$
\begin{array}{l}
c^{(1)}(x)=[x c(x)] \bmod (x^{n}+1) \text {, } \\
c^{(i)}(x)=[x^{i} c(x)] \bmod (x^{n}+1) \\
c(x)=c_{n-1} x^{n-1}+c_{n-2} x^{n-2}+\cdots+c_{1} x+c_{0} \\
x c(x)=c_{n-1} x^{n}+c_{n-2} x^{n-1}+\cdots+c_{1} x^{2}+c_{0} x \\
=c_{n-1} x^{n}+c_{n-2} x^{n-1}+\cdots+c_{1} x^{2}+c_{0} x+c_{n-1}+c_{n-1} \\
=c_{n-1}(x^{n}+1)+c^{(1)}(x) \\
arrow[x c(x)]_{\bmod (x^{n}+1)}=[c_{n-1}(x^{n}+1)+c^{(1)}(x)]_{\bmod (x^{n}+1)} \\
=c^{(1)}(x) \\
\end{array}
$$



> 例  (7,4)  循环码的第 12 个码字  $c_{12}$  的码多项式 为  $C(x)=x^{6}+x^{4}+x^{3}$ , 写出左循环移位 3 次的码字。
>
> 解:  $i=3, x^{3} C(x)=x^{9}+x^{7}+x^{6}$ , 与  $x^{7}+1$  作除法, 得  $C^{(3)}(x)=x^{6}+x^{2}+1$  。对应码字 1000101 。
>
> 另: 由简单移位给出, 原始码字 1011000 , 左移三位为: 1000101 。





参考文献：

1. Proakis, John G., et al. *Communication systems engineering*. Vol. 2. New Jersey: Prentice Hall, 1994.
2. Proakis, John G., et al. *SOLUTIONS MANUAL Communication Systems Engineering*. Vol. 2. New Jersey: Prentice Hall, 1994.
3. 周炯槃. 通信原理（第3版）[M\]. 北京：北京邮电大学出版社, 2008.
4. 樊昌信, 曹丽娜. 通信原理（第7版） [M\]. 北京：国防工业出版社, 2012.



[返回首页](https://github.com/timerring/information-theory)
