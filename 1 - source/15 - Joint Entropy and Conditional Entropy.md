## 联合熵和条件熵

### 联合熵

联合集  XY  上, 对联合自信息 $I(x y)$  的平均值称为联合熵:

$$
\begin{array}{l}
H(X Y)=\underset{p(x y)}{E}[I(x \rightleftharpoons y)] \\
=-\sum_{x} \sum_{y} p(x y) \log p(x y)
\end{array}
$$
当有n个随机变量 $X=\left(X_{1}, X_{2}, \ldots, X_{n}\right)$ , 有

$$
H(\mathbf{X})=-\sum_{X_{1}, X_{2}, \ldots, X_{n}} p\left(x_{1}, x_{2}, \ldots, x_{n}\right) \log p\left(x_{1}, x_{2}, \ldots, x_{n}\right)
$$
信息熵与热熵的关系

信息熵的概念是借助于热熵的概念而产生的。

1. 信息熵与热熵含义相似
2. 信息熵与热熵的区别:
   + 信息熵的不增原理
   + 热熵不减原理

3. 热熵的减少等于信息熵的增加。

### 条件熵

联合集 $\mathbf{X Y}$ 上, **条件自信息$I(y / x)$的平均值**定义为条件熵：

$$
\begin{array}{l}
H(Y / X)=\underset{p(x y)}{E}[I(y / x)]=-\sum_{x} \sum_{y} p(x y) \log p(y / x) \\
=\sum_{x} p(x)\left[-\sum_{y} p(y / x) \log p(y / x)\right]=\sum_{x} p(x) H(Y / x)
\end{array}
$$
推广：

$$
\begin{array}{l}
H\left(X_{n} \mid X_{1}, \ldots, X_{n-1}\right)
=-\sum_{X_{1}, X_{2}, \ldots, X_{n}} p\left(x_{1}, x_{2}, \ldots, x_{n}\right) \log p\left(x_{n} \mid x_{1}, \ldots, x_{n-1}\right)
\end{array}
$$
注意：当有n个随机变量 $X=\left(X_{1}, X_{2}, \ldots, X_{n}\right)$ 。

$$
\begin{array}{l}
H(X, Y)=H(Y)+H(X \mid Y)=H(X)+H(Y \mid X) \\
H(\mathbf{X})
=H\left(X_{1}\right)+H\left(X_{2} \mid X_{1}\right)+\ldots+H\left(X_{n} \mid X_{1}, X_{2}, \ldots, X_{n-1}\right)
\end{array}
$$
注意： $\mathbf{H}(\mathbf{X} \mid \mathbf{Y})$  表示已知变量 $\mathbf{Y}$  后, 对变量 $\mathbf{X}$  尚存在的平均不确定性（存在疑义）。

> 已知信源  $X=\left[\begin{array}{ccc}A & B & C \\ 1 / 3 & 1 / 3 & 1 / 3\end{array}\right]$  和  $Y=\left[\begin{array}{ccc}D & E & F \\ 1 / 10 & 3 / 5 & 3 / 10\end{array}\right]$  ,请快速两个信源的信息熵的关系。
>
> 答：H(X) > H(Y)。其实不用计算，由上面可知一个简单的结论，等概率时信息熵最大。



参考文献：

1. Proakis, John G., et al. *Communication systems engineering*. Vol. 2. New Jersey: Prentice Hall, 1994.
2. Proakis, John G., et al. *SOLUTIONS MANUAL Communication Systems Engineering*. Vol. 2. New Jersey: Prentice Hall, 1994.
3. 周炯槃. 通信原理（第3版）[M\]. 北京：北京邮电大学出版社, 2008.
4. 樊昌信, 曹丽娜. 通信原理（第7版） [M\]. 北京：国防工业出版社, 2012.



[返回首页](https://github.com/timerring/information-theory)
