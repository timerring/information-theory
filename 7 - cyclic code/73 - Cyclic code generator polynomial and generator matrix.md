- [循环码生成多项式与生成矩阵](#循环码生成多项式与生成矩阵)
  - [系统码生成矩阵的构造](#系统码生成矩阵的构造)
  - [系统码的循环码生成矩阵](#系统码的循环码生成矩阵)
- [循环码的监督 (校验)  矩阵](#循环码的监督-校验--矩阵)


## 循环码生成多项式与生成矩阵

定义：记  $\mathrm{C}(x)$  为  (n, k)  循环码的所有码字对应的多项式的集合, 若 g(x)  是  $\mathrm{C}(x)$  中除 0 多项式以外次数最低的多项式, 则称  g(x)  为这个循环码的**生成多项式**。

定理1:  $(\boldsymbol{n}, \boldsymbol{k})$  循环码中, 必定存在一个次数最小的唯一的码多项式g(x) , 称为生成多项式,
$$
g(x)=x^{r}+g_{r-1} x^{r-1}+\cdots+g_{1} x+1
$$
其中:  $r=n-k$ .

该码集中任意码字的码多项式必为g(x)的倍式。

非系统循环码的编码:
$$
c(x)=u(x) g(x)
$$

> 设某  (7,4)  循环码的生成多项式为$g(x)=x^{3}+x+1$，问信息串 0110 的循环码是什么?
>
> 解:  
>
> 
> $$
> c(x)=u(x) g(x)=(x^{2}+x)(x^{3}+x+1)=x^{5}+x^{4}+x^{3}+x
> $$
> 
>
> 故码字为: 0111010

定理2: 当且仅当  g(x)  是  $x^{n+1}$  的  $r=n-k$  次因式时,  g(x)是(n, k)循环码的生成多项式。

定理3: (n, k) 循环码的校验多项式为
$$
\begin{array}{l}
h(x)=\frac{x^{n}+1}{g(x)} \\
=h_{k} x^{k}+h_{k-1} x^{k-1}+\cdots+h_{1} x+h_{0}
\end{array}
$$
写出下面(7,3)循环码的生成多项式

![](https://raw.githubusercontent.com/timerring/picgo/master/picbed/image-20230210134143802.png)
$$
g(x)=x^{4}+x^{3}+x^{2}+1 arrow 0011101
$$
(1) 生成多项式、生成矩阵

循环码生成多项式的特点:

+ g(x)  的 0 次项是 1 ;
+ g(x)  唯一确定, 即它是码多项式中除 0 多项式以外次数最低的多项式;
+ 循环码每一码多项式都是  g(x)  的倍式, 且每一个小于等于 (n-1) 次的 g(x) 倍式一定是码多项式;
+ g(x) 的次数为 (n-k) ;
+ g(x) 是 $x^{n}+1$  的一个因子。

为了保证构成的生成矩阵  G  的各行线性不相关, 通常用生成多项式  g(x)  来构造生成矩阵; 若码多项式为降幂排列,
$$
\begin{array}{l}
g(x)=g_{n-k} x^{n-k}+g_{n-k-1} x^{n-k-1}+\cdots+g_{1} x+g_{0}, r=n-k \\
C(x)=\mathbf{u G}(x)=(u_{k-1} u_{k-2} \cdots u_{0}) \mathbf{G}(x) \\
=u_{k-1} x^{k-1} g(x)+u_{k-2} x^{k-2} g(x)+\cdots+u_{0} g(x) \\
G(x)=[\begin{array}{c}
x^{k-1} g(x) \\
x^{k-2} g(x) \\
\vdots \\
g(x)
\end{array}] rightarrow G=[\begin{array}{ccccccccc}
g_{r} & g_{r-1} & \cdots & g_{1} & g_{0} & 0 & 0 & \cdots & 0 \\
0 & g_{r} & g_{r-1} & \cdots & g_{1} & g_{0} & 0 & \cdots & 0 \\
& \vdots & & & & & \vdots & & \\
0 & \cdots & 0 & 0 & g_{r} & g_{r-1} & \cdots & g_{1} & g_{0}
\end{array}] \\
\end{array}
$$
显然, 上式不符合  $\mathbf{G}=(\mathbf{I}_{k}: \mathbf{Q})$  形式, 所以此生成矩阵不是典型形式。

### 系统码生成矩阵的构造

系统码-信息位在码字高位, 因此编码时需要先将信息位置于码字高位, 即  u(x) \bullet x^{n-k}  。 码字低位为校验位，如何获得?
$$
\begin{array}{c}
c(x)_{\bmod g(x)}=0 \\
c(x)=u(x) \cdot x^{n-k}+r(x) \\
\mathbf{0}=\{[u(x) x^{n-k}]_{\bmod g(x)}+r(x)\}
\end{array} \quad \stackrel{r(x)}{=}[u(x) x^{n-k}] \bmod g(x)
$$
(2) 系统循环码

系统循环码的编码:

a. 选择一信息码多项式  $\mu(x)$ , 使  $\quad r(x)=x^{n-k} \mu(x) \bmod g(x)$ 

b. 产生系统循环码式$\mathrm{c}(x)=x^{n-k} \mu(x)+r(x)$

> 有一 (15, 11) 汉明循环码, 其生成多项式  $g(x)=x^{4}+x+1$ , 若输入信息分组为 (10010010010), 求出  (15,11)  系统循环码字。
>
> 解:  $u(x)=x^{10}+x^{7}+x^{4}+x$ 
> $$
> \begin{array}{l}
> x^{n-k} u(x)=x^{4} u(x)=x^{14}+x^{11}+x^{8}+x^{5} \\
> r(x)=[x^{4} u(x)] \bmod g(x)=x^{2} \\
> \therefore c(x)=x^{14}+x^{11}+x^{8}+x^{5}+x^{2} \\
> c=10010010010(0100)监督位
> \end{array}
> $$
> 非系统码:  $c(x)=u(x) g(x)=x^{14}+x^{10}+x^{7}+x^{4}+x^{2}+x$   c=1000100100101100 

> 已知某循环码生成多项式为$g(x)=x^{8}+x^{6}+x^{4}+x^{2}+1$，那么采用此多项式生成循环码时，校验位有 [8] 位。
>
> 已知某循环码生成多项式为$g(x)=x^{8}+x^{6}+x^{4}+x^{2}+1$，证明该多项式是$x^{10}+1$的一个因式。 直接长除即可，这里不多赘述。
>
> 请写出生成多项式为$g(x)=x^{8}+x^{6}+x^{4}+x^{2}+1$的系统型循环码  (10 ，2)  的码表。并说明该码至少能纠几位错。
>
> ![](https://raw.githubusercontent.com/timerring/picgo/master/picbed/image-20230210140039097.png)
>
> $d_{\min }$=5, 能纠2位错 

### 系统码的循环码生成矩阵

$$
G(x)=[\begin{array}{c}
x^{n-1}+(x^{n-1})_{\bmod g(x)} \\
x^{n-2}+(x^{n-2})_{\bmod g(x)} \\
\vdots \\
x^{n-i}+(x^{n-i})_{\bmod g(x)} \\
\vdots \\
g(x)
\end{array}]=[\begin{array}{cccccccc}
1 & 0 & \cdots & 0 & r_{1,1} & r_{1,2} & \cdots & r_{1, n-k} \\
0 & 1 & \cdots & 0 & r_{2,1} & r_{2,2} & \cdots & r_{2, n-k} \\
\vdots & \vdots & & \vdots & \vdots & \vdots & & \vdots \\
0 & 0 & \cdots & 1 & r_{k, 1} & r_{k, 2} & \cdots & r_{k, n-k}
\end{array}]
$$

某  (7,4)  循环码的生成多项式是  $g(x)=x^{3}+x+1$ , 求系统码的生成矩阵。

解：
$$
\begin{array}{l}
(x^{6}) \bmod g(x)=x^{2}+1 \\
(x^{5}) \bmod g(x)=x^{2}+x+1 \\
(x^{4}) \bmod g(x)=x^{2}+x
\end{array} \quad arrow G=[\begin{array}{lllllll}
1 & 0 & 0 & 0 & 1 & 0 & 1 \\
0 & 1 & 0 & 0 & 1 & 1 & 1 \\
0 & 0 & 1 & 0 & 1 & 1 & 0 \\
0 & 0 & 0 & 1 & 0 & 1 & 1
\end{array}]
$$

## 循环码的监督 (校验)  矩阵

关系:  $\boldsymbol{G} \boldsymbol{H}^{T}=\mathbf{0}$  。

a. 监督矩阵构造：由性质  $x^{n}+1=g(x) h(x)$ ;
$$
\begin{array}{l}
h(x)=h_{k} x^{k}+h_{k-1} x^{k-1}+\ldots+h_{1} x+h_{0} \\
H=[\begin{array}{ccccccc}
h_{0} & h_{1} & \cdots & h_{k} & 0 & \cdots & 0 \\
0 & h_{0} & h_{1} & \cdots & h_{k} & \cdots & 0 \\
& \vdots & & & & \vdots & \\
0 & 0 & \cdots & h_{0} & h_{1} & \cdots & h_{k}
\end{array}] \\
\end{array}
$$
b. 利用循环码的特点来确定监督矩阵  H  :

由于  (n, k)  循环码中  g(x)  是  $x^{n+1}$  的因式, 因此可令:  $h(x)=\frac{x^{n}+1}{g(x)}=h_{k} x^{k}+h_{k-1} x^{k-1}+\cdots+h_{1} x+h_{0}$  监督矩阵表示为:


$$
H(x)=[\begin{array}{c}
x^{n-k-1} h^{*}(x) \\
x^{n-k-2} h^{*}(x) \\
\vdots \\
x h^{*}(x) \\
h^{*}(x)
\end{array}]
$$




$$
h^{*}(x)=h_{0} x^{k}+h_{1} x^{k-1}+h_{2} x^{k-2}+\cdots+h_{k-1} x
$$





参考文献：

1. Proakis, John G., et al. *Communication systems engineering*. Vol. 2. New Jersey: Prentice Hall, 1994.
2. Proakis, John G., et al. *SOLUTIONS MANUAL Communication Systems Engineering*. Vol. 2. New Jersey: Prentice Hall, 1994.
3. 周炯槃. 通信原理（第3版）[M\]. 北京：北京邮电大学出版社, 2008.
4. 樊昌信, 曹丽娜. 通信原理（第7版） [M\]. 北京：国防工业出版社, 2012.



[返回首页](https://github.com/timerring/information-theory)