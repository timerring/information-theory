- [随参信道特性](#随参信道特性)
    - [随参信道数学模型的建立](#随参信道数学模型的建立)
    - [随参信道对信号传输的影响](#随参信道对信号传输的影响)
      - [平坦性衰落及频率选择性衰落](#平坦性衰落及频率选择性衰落)
      - [1.平坦性衰落](#1平坦性衰落)
        - [Rayleigh 分布](#rayleigh-分布)
        - [Rice 分布](#rice-分布)
      - [2.频率选择性衰落](#2频率选择性衰落)
    - [多径随参信道的时延扩展与相干带宽](#多径随参信道的时延扩展与相干带宽)
      - [随参信道的多径时延特性](#随参信道的多径时延特性)
      - [多径信道的频域特性](#多径信道的频域特性)
    - [总结](#总结)


# 随参信道特性

随参信道的传输特性主要依赖于传输媒质特性，以电离层反射信道、对流层散射信道为主要代表。 **随参信道是一种信道传输特性随时间随机快速变化的信道**， 包括陆地移动信道，短波电离层反射信道、超短波微波对流层散射信道、超短波视距绕射信道。

随参信道的传输媒介具有以下三个特点：

+ **对信号的衰耗（衰减）随时间而变；**
+ **传输的时延随时间而变；**
+ **会产生多径传播的效果。**

**多径传播** ：指由发射点出发的电波可能经过多条路径到达接收点。每条路径对信号的衰减和时延都随电离层或对流层等传输媒质的变化而变化，接收信号将是衰减和时延随时间变化的各路径信号的叠加与合成。
$$
h(t)=\sum_{i=1}^{L} \mu_{i}(t) \delta\left[t-\tau_{i}(t)\right]
$$

### 随参信道数学模型的建立

设发送信号为  $s(t)=A \sum_{n=-\infty}^{\infty} d_{n} g(t-n T) \cos 2 \pi f_{c} c t$, $A$ 信号幅度,  $d_{n}$  信息码元,  $g(t)$  信息码元波形,  $f_{c}$  载波频率。

令  $b(t)=\sum_{n=-\infty}^{\infty} d_{n} g(t-n T)$ , 则  $s(t)=A b(t) \cos 2 \pi f_{c} t$  。经过多径信道  $h(t)=\sum_{i=1}^{L} u_{i}(t) \delta(t-\tau_{i}(t))$ , 接收信号为
$$
r(t)=A \sum_{i=1}^{L} u_{i}(t) b\left(t-\tau_{i}(t)\right) \cos \left(2 \pi f_{c} t+\varphi_{i}(t)\right)
$$
$ u_{i}(t)$  第  i  条路径的衰落因子,  $\tau_{i}(t)$  为第  i  条路径的传输时延。

令  $\varphi_{i}(t)=-2 \pi f_{c} \tau_{i}(t)$ , 则有
$$
r(t)=A \sum_{i=1}^{L} u_{i}(t) b\left(t-\tau_{i}(t)\right) \cos \left(2 \pi f_{c}\left(t-\tau_{i}(t)\right)\right)
$$
一般情况  $u_{i}(t)$ 、 $\tau_{i}(t)$  较载波  $\cos (2 \pi f_{c} t)$  变化缓慢得多,  $r(t)$  可视为窄带过程, 又可表示为
$$
\begin{array}{c}
r(t)=A \sum_{i=1}^{L} u_{i}(t) b\left(t-\tau_{i}(t)\right) \cos \varphi_{i}(t) \cos 2 \pi f_{c} t \\
-A \sum_{i=1}^{L} u_{i}(t) b\left(t-\tau_{i}(t)\right) \sin \varphi_{i}(t) \sin 2 \pi f_{c} t
\end{array}
$$
即为随参信道的数学模型, 利用它可以分析随参信道对信号传输的影响。

### 随参信道对信号传输的影响

#### 平坦性衰落及频率选择性衰落

#### 1.平坦性衰落

满足:  $|\tau_{i}(t)|_{\max } \ll T$ ,  $T$ 为码元周期, 且  $|\tau_{i}(t)|_{\max } \sim 1 / f_{c}$  ,  $b(t-\tau_{i}(t)) \approx b(t-\overline{\tau(t)}), i=1,2, \ldots, L $, 其中  $\overline{\tau(t)}$  为  $\tau_{i}(t)$  的数学期望。
$$
\begin{aligned}
r(t) &=A \sum_{i=1}^{L} u_{i}(t) b\left(t-\tau_{i}(t)\right) \cos \varphi_{i}(t) \cos 2 \pi f_{c} t-A \sum_{i=1}^{L} u_{i}(t) b\left(t-\tau_{i}(t)\right) \sin \varphi_{i}(t) \sin 2 \pi f_{c} t \\
&=A b(t-\overline{\tau(t)})\left[x_{c}(t) \cos 2 \pi f_{c} t-x_{s}(t) \sin 2 \pi f_{c} t\right]=A b(t-\overline{\tau(t)}) v(t) \cos \left(2 \pi f_{c} t+\varphi(t)\right) \\
&=\operatorname{Re}\left[A b(t-\overline{\tau(t)}) v(t) e^{j\left(2 \pi f_{c} t+\varphi(t)\right)}\right]
\end{aligned}
$$
其中 $ v(t)$  为 $ r(t)$  的随机包络,  $\varphi(t) $ 为 $ r(t)$  的随机相位。
$$
\begin{aligned}
x_{c}(t) &=\sum_{i=1}^{L} u_{i}(t) \cos \varphi_{i}(t) \\
x_{s}(t) &=\sum_{i=1}^{L} u_{i}(t) \sin \varphi_{i}(t) \\
v(t) &=\sqrt{x_{c}^{2}(t)+x_{s}^{2}(t)} \\
\varphi(t) &=\arctan \left(\frac{x_{s}(t)}{x_{c}(t)}\right)
\end{aligned}
$$

$$
r(t)=\operatorname{Re}\left[A b(t-\overline{\tau(t)}) v(t) e^{j\left(2 \pi f_{c} t+\varphi(t)\right)}\right]
$$



多径传输和信道特性的变化导致**接收信号幅度随机变化, 载波相位随机变化, 而基带信号  $\boldsymbol{b}(t)$  波形变化不大**。—**平坦性衰落**

多径传输引起的复包络  $v(t) e^{j \varphi(t)}$  对基带信号而言相当于乘性千扰。

经不同路径到达接收端的不同信号的相关性很小，且根据中心极限定理, 当路径数很大时, 多径信号的概率分布趋于高斯分布, 即  $x_{s} $ ， $x_{c}$  服从高斯分布，从而  v(t)  的概率分布为瑞利（Rayleigh）分布, 相位  $\varphi(t)$  为均匀分布。另外, 如果接收信号中还包括一路直射信号 , 则信号的包络分布为广义瑞利分布或者莱斯 (Rice) 分布。

##### Rayleigh 分布

$$
f(x)=\frac{x}{\sigma^{2}} e^{-\frac{x^{2}}{2 \sigma^{2}}}
$$

![image-20221118211226253](https://raw.githubusercontent.com/timerring/picgo/master/picbed/image-20221118211226253.png)

##### Rice 分布

$$
f(x)=\frac{x}{\sigma^{2}} e^{-\frac{x^{2}+c^{2}}{2 \sigma^{2}}} I_{0}\left(\frac{c x}{\sigma^{2}}\right)
$$


其中  c  为直射 (视距) 信号的峰值,  $I_{0}(\cdot)$  为第一类 0 阶修正贝塞尔函数 。定义  $K=\frac{c^{2}}{2 \sigma^{2}}$ , 表示主信号功率与多径分量功率之比,  $\mathbf{K}=\mathbf{0}$  时（即不存在视距分量), Rice分布等效为 Rayleigh分布。

![image-20221118211411207](https://raw.githubusercontent.com/timerring/picgo/master/picbed/image-20221118211411207.png)

#### 2.频率选择性衰落

若信道时延  $|\tau_{i}(t)|_{\max }>T$ ,  则   $\boldsymbol{b}(\boldsymbol{t}-\boldsymbol{\tau}_{\boldsymbol{i}}(\boldsymbol{t}))$  不能近似为  $\boldsymbol{b}(\boldsymbol{t}-\overline{\boldsymbol{\tau}(\boldsymbol{t})})$  。

干扰可存在于不同码元。

不同路径的不同信息码元之间会产生很大的相互干扰，称为**码间干扰**或者符号间千扰, 产生严重波形失真, 引起很大误码, 影响通信质量。

**接收信号以及其信息信号的幅度和相位都将产生畸变**; **频率域上看, 即不同频率分量受到不同程度的衰落, 称为频率选择性衰落。**

绿色矩形代表码元，红色为信道：

![](https://raw.githubusercontent.com/timerring/picgo/master/picbed/image-20221118211801112.png)

分别为平坦与频率选择性衰落。

### 多径随参信道的时延扩展与相干带宽

此两参量阐明在什么条件下信号通过随参信道传输会引起平坦性或频率选择性衰落

#### 随参信道的多径时延特性

均方根时延扩展 (时延扩展)：
$$
\sigma_{\tau}=\sqrt{\overline{\tau^{2}}-(\bar{\tau})^{2}}
$$
最大时延差:  $\tau_{\max }$  。

#### 多径信道的频域特性

以二径信道模型为例:  $s(t)=A \cos 2 \pi f t$ ,经过二径信道传输, 有  $r(t)=A \cos 2 \pi f t+A \cos 2 \pi f(t-\tau)   =A \cos 2 \pi f t+A \cos (2 \pi f t+\phi), \phi=-2 \pi f \tau$  。
两径矢量之和为向量  $\vec{B}$ , 信道输出  $r(t)$  的幅度和相位与二径信号的相位差  $\phi=-2 \pi f \tau$  有关; 若时延差  $\tau$  为常数,则对不同频率  f, $\phi=-2 \pi f \tau$  不同。

![](https://raw.githubusercontent.com/timerring/picgo/master/picbed/image-20221118212248973.png)

> 当  $\phi=0,2 \pi, 4 \pi, \ldots, r(t)$  的幅度  $|\vec{B}|$  最大为  $2 A$ , 当  $\boldsymbol{\phi}=\boldsymbol{\pi}, 3 \pi, 5 \pi \ldots$ , 幅度  $|\vec{B}|$  最小为 "0."

信道的传输特性:  $H(f)=1+e^{-j 2 \pi f \tau}$ , 其幅频特性  $|H(f)|=2|\cos (\pi f \tau)|$  。

**时延差的倒数称为信道的相干带宽  $B_{c}=1 / \tau$  。**

若信号带宽  $B<B_{c} $  信号通过信道失真可忽略; 若  $B \geq B_{c}$  信号通过信道失真很大。

![](https://raw.githubusercontent.com/timerring/picgo/master/picbed/image-20221118212529107.png)

对于多径信道, 可用时延扩展近似求出信道的相干带宽


$$
B_{c} \approx \frac{1}{\sigma_{\tau}}
$$


**当信号带宽  $B>B_{c}$ , 信号遭受频率选择性衰落, 引起码间干扰;  当  $B \ll B_{c}$  时, 信号遭受平坦衰落。**

### 总结

时域:

 -  信道时延  $|\tau_{i}(t)|_{\max } \ll T$   (T为信号码元周期) ,  且   $|\tau_{i}(t)|_{\max } \sim 1 / f_{c}$  , 信号遭受平坦衰落。接收信号的幅度特性符合瑞利分布或莱斯分布。
- 信道时延  $|\tau_{i}(t)|_{\max }>T$ , 频率选择性衰落。

 频域:

-  信号带宽  $B \ll B_{c}$  （信道相千带宽）时, 信号遭受平坦衰落。
-  信号带宽  $B>B_{c}$ , 信号遭受频率选择性衰落, 引起码间千扰。

> 如下图所示信号频谱与信道频率响应，推测信号经过此信道传输，会遭受[频率选择性]衰落。
>
> ![](https://raw.githubusercontent.com/timerring/picgo/master/picbed/image-20230208164121014.png)





参考文献：

1. Proakis, John G., et al. *Communication systems engineering*. Vol. 2. New Jersey: Prentice Hall, 1994.
2. Proakis, John G., et al. *SOLUTIONS MANUAL Communication Systems Engineering*. Vol. 2. New Jersey: Prentice Hall, 1994.
3. 周炯槃. 通信原理（第3版）[M\]. 北京：北京邮电大学出版社, 2008.
4. 樊昌信, 曹丽娜. 通信原理（第7版） [M\]. 北京：国防工业出版社, 2012.



[返回首页](https://github.com/timerring/information-theory)