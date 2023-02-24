- [信道容量](#信道容量)
  - [信道容量的定义](#信道容量的定义)
    - [信息传输率 R](#信息传输率-r)
    - [信息传输速率](#信息传输速率)
    - [平均互信息](#平均互信息)
    - [信道容量](#信道容量-1)
  - [三种特殊信道的容量](#三种特殊信道的容量)
    - [无噪无损信道](#无噪无损信道)
    - [有噪无损信道](#有噪无损信道)
    - [无噪有损信道](#无噪有损信道)
  - [典型信道的信道容量](#典型信道的信道容量)
    - [BSC信道容量](#bsc信道容量)
    - [连续信道的信道容量](#连续信道的信道容量)
      - [单符号高斯连续信道](#单符号高斯连续信道)
      - [限频、限功率高斯信道的容量](#限频限功率高斯信道的容量)
      - [单符号信号一\>多符号多维信道](#单符号信号一多符号多维信道)
      - [Shannon信道编码定理](#shannon信道编码定理)
  - [信源与信道的匹配](#信源与信道的匹配)


# 信道容量

写出并解释信道容量的定义

分析计算如下信道的信道容量

+ 无噪无损信道
+ 有噪无损信道
+ 无噪有损信道
+ 二进制对称信道
+ AWGN信道

## 信道容量的定义

香农指出信道中的噪声对信道造成的根本限制是**信道的传信率**, 而不是可靠性。

### 信息传输率 R

我们研究信道的目的是要讨论信道中平均每个符号所能传送的信息量, 即**信道的信息传输率 R** , 即
$$
\begin{aligned}
R=I(X ; Y) & =H(X)-H(X \mid Y) \\
& =H(Y)-H(Y \mid X) \text { bit } / \text { symbol }
\end{aligned}
$$

### 信息传输速率

若每个符号传输时间为  $t(\mathrm{s})$ , 则**信道在单位时间内平均的信息量**定义为**信息传输速率**
$$
R_{t}=\frac{I(X ; Y)}{t} \quad \mathrm{bit} / \mathrm{s}
$$


### 平均互信息

信道的信息传输率就是平均互信息

接收到符号  $\mathrm{Y} $ 后平均每个符号获得的关于  $\mathrm{X}$  的信息量。
$$
\begin{array}{l}
I(X ; Y)=\sum_{i} \sum_{j} p(x_{i}) p(y_{j} \mid x_{i}) \log \frac{p(y_{j} \mid x_{i})}{p(y_{j})} \\
p(y_{j})=\sum_{i=1}^{n} p(x_{i}) p(y_{j} \mid x_{i})
\end{array}
$$
定理：

给定信道转移概率矩阵P后,平均互信息  I(X ; Y)  是输入信源的概率分布  $p(\boldsymbol{x})$  的  $\cap$  型上凸函数。

**信道容量是完全描述信道特性的参量,是信道能够传输的最大信息量。**使 $ I(\boldsymbol{X} ; \boldsymbol{Y}) $ 达到最大的**信源的概率分布  $p(\boldsymbol{x})$**  称为该信道的最佳输入分布。

### 信道容量

最大的信息传输率, 单位 bit/symbol


$$
C=\max _{p(\boldsymbol{x}_{i})} I(X ; Y)
$$


单位时间的信道容量, 单位 bit/s:


$$
C=\frac{1}{T} \max _{p(x_{i})} I(X ; Y)
$$

## 三种特殊信道的容量

### 无噪无损信道

输入输出一一对应, 信道无噪声无信息损失。
$$
\begin{array}{c}
H(X \mid Y)=H(Y \mid X)=0 \\
C=\max _{p(x)} I(X ; Y)=\max _{p(x)}\{H(X)-H(X \mid Y)\} \\
=\max _{p(x)} H(X)=\operatorname{logr}=\log s
\end{array}
$$
其中$ \mathbf{r} $ 为信道输入符号个数,  $\mathbf{s}$  为信道输出符号个数,  $\mathbf{r}=s$  。**最佳输入为等概输入**。

![](https://raw.githubusercontent.com/timerring/picgo/master/picbed/image-20230208211654250.png)

### 有噪无损信道

根据接收的符号, 可以完全确定发送符号, 无信息损失。
$$
\begin{array}{c}
H(X \mid Y)=0 \\
C=\max _{p(x)} I(X ; Y)=\max _{p(x)}\{H(X)-H(X \mid Y)\} \\
=\max _{p(x)} H(X)=\operatorname{logr}
\end{array}
$$
**最佳输入为等概输入**

![](https://raw.githubusercontent.com/timerring/picgo/master/picbed/image-20230208212351331.png)

### 无噪有损信道

发送不会出错, 无噪声。但是根据接收符号, 无法准确判断发送符号, 有信息损失。
$$
\begin{array}{c}
H(Y \mid X)=0 \\
C=\max _{p(x)} I(X ; Y)=\max _{p(x)}\{H(Y)-H(Y \mid X)\} \\
=\max _{p(x)} H(Y)=\operatorname{logs}
\end{array}
$$
**最佳输入为使输出等概**。

## 典型信道的信道容量

### BSC信道容量

设二进制对称信道的输入概率空间为
$$
[\begin{array}{l}
X \\
P
\end{array}]=[\begin{array}{cc}
0 & 1 \\
\omega & \bar{\omega}
\end{array}]
$$
信道矩阵:
$$
P=[\begin{array}{cc}
1-p & p \\
p & 1-p
\end{array}]=[\begin{array}{ll}
\bar{p} & p \\
p & \bar{p}
\end{array}]
$$
![](https://raw.githubusercontent.com/timerring/picgo/master/picbed/image-20230208213436225.png)
$$
\begin{array}{l}
p(y=0)=\sum_{i=0}^{1} p(x_{i}) p(y_{0} \mid x_{i})=\omega \bar{p}+\bar{\omega} p \\
p(y=1)=\sum_{i=0}^{1} p(x_{i}) p(y_{1} \mid x_{i})=\omega p+\bar{\omega} \bar{p} \\
H(Y) \\
=(\omega \bar{p}+\bar{\omega} p) \log \frac{1}{\omega \bar{p}+\bar{\omega} p}+(\omega p+\bar{\omega} \bar{p}) \log \frac{1}{\omega p+\bar{\omega} \bar{p}} \\
=H(\omega \bar{p}+\bar{\omega} p)
\end{array}
$$

$$
\begin{array}{l}
H(Y \mid X)=-\sum_{i} p(x_{i}) \sum_{j} p(y_{j} \mid x_{i}) \log p(y_{j} \mid x_{i}) \\
=-\sum_{j} p(y_{j} \mid x_{i}) \log p(y_{j} \mid x_{i})=-[p \log p+\bar{p} \log p] \\
=H(p) \\
I(X ; Y)=H(Y)-H(Y \mid X)=H(\omega \bar{p}+\bar{\omega} p)-H(p) \\
\leq 1-H(p)
\end{array}
$$

当  p  固定时,  I(X ; Y)  是  $\omega$  的  $\cap$  型上凸函数。

![](https://raw.githubusercontent.com/timerring/picgo/master/picbed/image-20230208213917009.png)
$$
\begin{array}{l}
I(X ; Y)=H(Y)-H(Y \mid X) \\
=H(\omega \bar{p}+\bar{\omega} p)-H(p) \\
\leq 1-H(p)
\end{array}
$$
I(X, Y)  对  $\omega$  存在一个极大值,该极大值为信源的压缩极限。

BSC 信道容量  $C=1-H(p) $

当固定信源的概率分布  $\omega$  时, $I(X ; Y)$  是  p  的U型下凸函数。

+ 当  $\boldsymbol{p}=\mathbf{0}$ ,
  $C=1-0=1  bit  =H(X) $   (信道无噪声)
+ 当  $p=1 / 2$ ,
  $C=1-H(\frac{1}{2}, \frac{1}{2})=0 $    (信道强噪声)

![](https://raw.githubusercontent.com/timerring/picgo/master/picbed/image-20230208214210353.png)

当信源输入符号的速率为  $r_{s}$  (符号/秒), 信道容量
$$
C_{t}=r_{s}[1-H(p)]
$$
实际信息传输速率  $R_{t}$  为
$$
R_{t}=r_{s}[H(X)-H(X \mid Y)]
$$
进入信道输入端的信息速率
$$
D_{\text {in }}=r_{s} H(X)
$$

> BSC信道如下图,  $r_{s}=1000$  符号/秒,错误传递概率  $p=0.1$ 求:信道容量和实际信息传输速率。
>
> ![](https://raw.githubusercontent.com/timerring/picgo/master/picbed/image-20230208215957814.png)
> $$
> \begin{aligned}
> C_{t} & =r_{s}[1-H(p)] \\
> & =1000[1+(0.1 \log 0.1+0.9 \log 0.9)] \\
> & =1000[1-0.469]=531 \mathrm{bit} / \mathrm{s}
> \end{aligned}
> $$
> 信道实际信息传输速率
>
> $$
> \begin{array}{l}
> R_{t}=r_{s}[H(X)-H(X \mid Y)] \\
> =1000 \times[0.811-0.398]=413 \mathrm{bit} / \mathrm{s} \\
> D_{i n}=r_{s} H(X)=1000 \times 0.811=811 \mathrm{bit} / \mathrm{s}
> \end{array}
> $$
> ![](https://raw.githubusercontent.com/timerring/picgo/master/picbed/image-20230208221348926.png)
>
> 解:  $I(X ; Y)=H(Y)-H(Y \mid X)$ 
> $$
> \begin{aligned}
> H(Y \mid X) & =\sum_{x} p(x) H(Y \mid X=x) \\
> & =q H(Y \mid X=0)+(1-q) H(Y \mid X=1)
> \end{aligned}
> $$
> 因为:
> $$
> \begin{array}{l}
> H(Y \mid X=0) \\
> =p(0 \mid x=0) \log p(0 \mid x=0)+p(1 \mid x=0) \log p(1 \mid x=0) \\
> =1 \log 1+0 \log 0=0 \\
> H(Y \mid X)=(1-q) H(Y \mid X=1)=(1-q) h(0.5)=1-q
> \end{array}
> $$
>
> $$
> \begin{array}{l}
> p(Y=0) \\
> =q p(Y=0 \mid X=0)+(1-q) p(Y=0 \mid X=1) \\
> =q+(1-q) \times 0.5=0.5+0.5 q p(Y=1)=q \\
> p(Y=1 \mid X=0)+(1-q) p(Y=1 \mid X=1) \\
> =(1-q) \times 0.5=0.5-0.5 q
> \end{array}
> $$
>
> 故:
> $$
> \mathrm{C}=\max _{q}[H(0.5-0.5 q)-(1-q)]
> $$
> 令  $\frac{d C}{d q}=0$ , 有  $q=\frac{3}{5}=0.6$ 
> $$
> C=h(0.2)-0.4=0.3219
> $$
> 
>
> 

### 连续信道的信道容量

#### 单符号高斯连续信道

输入为连续随机变量  $X \in(-\infty, \infty)$ ,输出为  $Y=X+n$, $n$  : 均值为 0 , 方差为  $\sigma^{2}$  的高斯变量, 与  X  统计独立。由条件概率可知, 当  X  已知时,  Y  也为正态变量, 均值为 0 , 方差为  $\sigma^{2}$ ,
$$
p(y \mid x)=\frac{1}{\sqrt{2 \pi \sigma^{2}}} \exp [-\frac{1}{2 \sigma^{2}}(y-x)^{2}]
$$

$$
\begin{array}{l}
I[X ; Y, p(x)] \\
=H(Y)-\int_{-\infty}^{\infty} p(x) \int_{-\infty}^{\infty} p(y \mid x) \log p(y \mid x) d y d x \\
=H(Y)-\int_{-\infty}^{\infty} p(x) \log (\sqrt{2 \pi e} \sigma) d x \\
=H(Y)-\log (\sqrt{2 \pi e} \sigma)
\end{array}
$$

注:  p(x)  高斯分布, 则有
$$
\int_{-\infty}^{\infty} p(x) \log p(x) d x=\log (\sqrt{2 \pi e} \sigma)
$$
当信道输入功率为时  $P_{W i}$ , 输出功率可表示为  $P_{W o}$ , 且输入与噪声独立时
$$
P_{W o}=P_{W i}+\sigma^{2}
$$
使  H(Y)  最大的  Y  是均值为 0 的正态分布随机变量。而由  $Y=X+n$  可知,  $X$  也应该为均值为零方差为  $P_{W_{i}}$  的随机变量。所以
$$
C=\log \sqrt{2 \pi e P_{W o}}-\log \sqrt{2 \pi e \sigma^{2}}=\frac{1}{2} \log \frac{P_{W o}}{\sigma^{2}}=\frac{1}{2} \log (1+\frac{P_{W i}}{\sigma^{2}})
$$
如不限制输入信号,  $H(\boldsymbol{H})$ 、 $P_{W_{o}}$  可趋于无限, 此时信道容量无限大一一实际不可行。

#### 限频、限功率高斯信道的容量

信道输入信号为平稳随机过程  $X(t)$ , 加性干扰为  $n(t)$ , 输出为  $Y(t)=X(t)+n(t)$  。输入信号功率受限, 即  $E[X^{2}(t)] \leq S$  。

限带信道的频率特性:


$$
H(f)=\{\begin{array}{ll}
1, & |f|<B \\
0, & |f|>B
\end{array}.
$$


$ Y(t), X(t), n(t)$  的带宽为  B , 以  2B  采样，得  $Y(t_{1}), Y(t_{2}), \ldots$ ,
$ Y(t_{n}), \ldots, Y(t_{L}) \ldots, X(t_{1}), X(t_{2}), \ldots, X(t_{n}), \ldots, X(t_{L}) \ldots, n(t_{1}), n(t_{2}), \ldots ,
 n(t_{n}), \ldots, n(t_{L}) \ldots$  。时刻  $t_{n}, Y(t_{n})=X(t_{n})+n(t_{n})$  。

由单符号高斯信道容量公式可得


$$
\begin{aligned}
C & =\max _{p(x)}[I(X(t_{n}), Y(t_{n}), p(x))] \\
& =\frac{1}{2} \log (1+\frac{s}{\sigma^{2}})
\end{aligned}
$$


上式中  $\frac{S}{\sigma^{2}}$  为信号功率与噪声功率的比, 也即信噪比 , 其中  $S=E[X^{2}(t_{n})], \sigma^{2}=E[n^{2}(t_{n})]$  。

#### 单符号信号一>多符号多维信道

$X_{L}, Y_{L}$  分别表示  L  个抽样  $X(t_{n}), Y(t_{n})  (n=1,2, \ldots, L)$  的  L  维向量, 则对多符号信道
$$
I(X_{L}, Y_{L}) \leq \frac{L}{2} \log (1+\frac{S}{\sigma^{2}})
$$
当  $X(t_{n}), Y(t_{n})$  统计独立时
$$
\max [I(X_{L}, Y_{L})]=\frac{L}{2} \log (1+\frac{S}{\sigma^{2}})
$$


 T  时间内抽样数  L=2BT , 则信道传输最大信息量
$$
C_{T}=B T \log (1+\frac{S}{\sigma^{2}})
$$
对连续信道, 定义单位时间内传送的最大信息量为信道容量
$$
C=\frac{C_{T}}{T}=B \log (1+\frac{S}{\sigma^{2}})
$$
**限频、限功率高斯信道的信道容量公式, 也即 Shannon公式。**

香农公式的另一种表达: 因为  $\lim _{x arrow 0} \frac{1}{x} \log (1+x)=\log _{2} e \approx 1.44 $, 所以 $\lim _{B arrow \infty} C \approx 1.44 \frac{S}{N_{0}}$  。  

$C=B \log (1+\frac{S}{N_{0} B}) b i t / s, N_{0}$  为限带高斯白噪声  n(t)  的单边功率谱密度。

当  $S arrow \infty$  时,  $C arrow \infty$ ; 当 $ B arrow \infty$  时,  $C arrow$  一确定值。


$$
\begin{array}{c}
C=B \log (1+\frac{S}{N_{0} B})=\frac{S}{N_{0}} \frac{N_{0} B}{S} \log (1+\frac{S}{N_{0} B}) \\
\lim _{B arrow \infty} C=\frac{S}{N_{0}} \lim _{B arrow \infty}[\frac{N_{0} B}{S} \log (1+\frac{S}{N_{0} B})] \approx 1.44 \frac{S}{N_{0}}
\end{array}
$$


当  $C_{\infty}=1 \mathrm{bit} / \mathrm{s}$ ,有  $\frac{P_{s}}{N_{0}}=\ln 2=0.693 \sim-1.6 d B$ ,即带宽不受限制时, 传输1bit信息, 信噪比最低只需要-1.6dB, 这是加性高斯噪声信道信息传输速率的极限值, 是一切编码方式所能达到的理论极限。

$\gamma=\frac{C_{t}}{W}=\log (1+S N R) b p s / H z$--  单位频带的信息传输速率（频带利用率）。

当  $\gamma arrow 0$  时,  $\mathrm{SNR}=-1.6 \mathrm{~dB}$ , 此时信道完全丧失通信能力。



![](https://raw.githubusercontent.com/timerring/picgo/master/picbed/image-20230208222841918.png)

![](https://raw.githubusercontent.com/timerring/picgo/master/picbed/image-20230208223007823.png)

小结：

保证一定的信道容量的带宽  B  和信噪比  $S / N_{0}$  可以互换, 即增加带宽 可以降低必须的信橾比, 或增加信噪比也可以降低所必须的带宽。

#### Shannon信道编码定理

揭示了信源信息速率与信道容量的关系

如果信源的信息率 (即每秒发出的信息量）小于信道容量, 则存在一种编码方式, 可保证通过该信道传送信息的差错率任意小；反之 , 如果信源的信息率大于信道容量, 则不可能存在此种编码方式, 传送信息的差错率将很大。

> 现设计一个M进制数字通信系统，要求码元速率为  $10^{4}$  波特。已知信道为 $ A W G N $ 信道，带宽为  $10 \mathrm{kHz}$  ， 噪声的功率谱密度为  $N_{0}=1 \times 10^{-12} \mathrm{~W} / \mathrm{Hz}$ , 系统最大发送功率为  $10 \mathrm{~W}$  ，信道衰减  $80 \mathrm{~dB}$  。问  $\mathrm{M}$  最大取值是多少?
>
> 解:  $C=B \log (1+\frac{S}{N}) $
> $$
> 10 \lg (\frac{P_{T}}{P_{R}})=10 \lg (10 / P_{R})=80 arrow P_{R}=10^{-7} \mathrm{~W}
> $$
>
>
> 故
> $$
> \begin{array}{c}
> \frac{S}{N}=\frac{10^{-7}}{1 \times 10^{-12} \times 10^{4}}=10 \\
> C=B \log (1+\frac{S}{N}) \approx 3.46 \times 10^{4} \mathrm{bit} / \mathrm{s} \\
> C \geq R_{B} \times \log M arrow 3.46 \times 10^{4} \geq 10^{4} \times \log M arrow M \leq 3.46
> \end{array}
> $$
> 故：M最大取值为 8 。
>

## 信源与信道的匹配

信道的信息的传输速率  $\mathbf{R}$  与信源分布密切相关。 

$\mathbf{R}=\mathbf{C}$ , 信源与信道匹配。

$\mathbf{R} \neq \mathbf{C}$ , 信源与信道不匹配, 信道有冗余

定义
$$
信道冗余度  = C - I (X ; Y)
$$
其中  $I(X ; Y)$  是信道实际通过的平均信息速率
$$
信道相对冗余度  =1-\frac{I(X ; Y)}{C} 
$$



参考文献：

1. Proakis, John G., et al. *Communication systems engineering*. Vol. 2. New Jersey: Prentice Hall, 1994.
2. Proakis, John G., et al. *SOLUTIONS MANUAL Communication Systems Engineering*. Vol. 2. New Jersey: Prentice Hall, 1994.
3. 周炯槃. 通信原理（第3版）[M\]. 北京：北京邮电大学出版社, 2008.
4. 樊昌信, 曹丽娜. 通信原理（第7版） [M\]. 北京：国防工业出版社, 2012.



[返回首页](https://github.com/timerring/information-theory)
