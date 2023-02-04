- [熵速率 (entropy rate)](#熵速率-entropy-rate)
- [各类熵的关系](#各类熵的关系)


### 熵速率 (entropy rate)

定义：一个平稳的时域离散随机过程的**熵速率 (entropy rate)** 定义为
$$
H=\lim _{n \rightarrow \infty} H(X_{n} \mid X_{1}, X_{2}, \ldots, X_{n-1})
$$
具有记忆性的信源的**熵速率**定义为

$$
H=\lim _{n \rightarrow \infty} \frac{1}{n} H\left(X_{1}, X_{2}, \ldots, X_{n}\right)
$$

> Example  两个二进制随机变量 $\mathbf{X}$  和 $\mathbf{Y}$ , 其联合分布为  p(X=Y=0) = p( X=0, Y=1) = p( X=Y=1) = 1/3 。
>
> 计算  $H(X)$,  $H(Y)$, $H(X \mid Y)$, $H(Y \mid X)$ , and  $H(X, Y)$ 。
>
> Solution:
>
> $\begin{array}{l}
> p(X=0)=p(X=0, Y=0)+p(X=0, Y=1)=\frac{2}{3} \\
> p(X=1)=p(X=1, Y=0)+p(X=1, Y=1)=\frac{1}{3} \\
> p(Y=0)=p(X=0, Y=0)+p(X=1, Y=0)=\frac{1}{3} \\
> p(Y=1)=p(X=0, Y=1)+p(X=1, Y=1)=\frac{2}{3} \\
> H(X)=\frac{1}{3} \log 3+\frac{2}{3} \log \frac{3}{2}=0.9183 \quad H(Y)=\frac{1}{3} \log 3+\frac{2}{3} \log \frac{3}{2}=0.9183 \\
> H(X, Y)=\sum_{i=1}^{n} p(X, Y) \log (X, Y)=\log 3=1.585 \\
> H(X \mid Y)=H(X, Y)-H(Y)=0.6667 \quad H(Y \mid X)=H(X, Y)-H(X)=0.6667
> \end{array}$

### 各类熵的关系

1. 条件熵不大于信息熵

  熵的不增原理: $H(Y / X) \leq H(Y)$

2. 联合熵不大于个信息熵的和，即

   $H\left(X_{1} X_{2} \ldots X_N\right) \leq \sum_{i=1}^{N} H\left(X_{i}\right)$

   仅当各 $X_{i}$ 相互独立时, 等号成立。

3. $H(X Y)=H(X)+H(Y \mid X)=H(Y)+H(X \mid Y)$

4. $H(X) \geq H(X \mid Y) ; H(Y) \geq H(Y \mid X)$



参考文献：

1. Proakis, John G., et al. *Communication systems engineering*. Vol. 2. New Jersey: Prentice Hall, 1994.
2. Proakis, John G., et al. *SOLUTIONS MANUAL Communication Systems Engineering*. Vol. 2. New Jersey: Prentice Hall, 1994.
3. 周炯槃. 通信原理（第3版）[M\]. 北京：北京邮电大学出版社, 2008.
4. 樊昌信, 曹丽娜. 通信原理（第7版） [M\]. 北京：国防工业出版社, 2012.



[返回首页](https://github.com/timerring/information-theory)