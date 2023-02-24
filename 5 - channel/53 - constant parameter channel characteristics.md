- [恒参信道特性及其对信号传输的影响](#恒参信道特性及其对信号传输的影响)
    - [无失真信道满足的条件](#无失真信道满足的条件)
    - [时延特性](#时延特性)
    - [群时延特性](#群时延特性)
    - [带通信号的复包络无失真](#带通信号的复包络无失真)
    - [信道不理想对输出信号的影响](#信道不理想对输出信号的影响)



# 恒参信道特性及其对信号传输的影响

恒参信道 ：信道特性不随时间变化或者变化很缓慢，信道特性主要由传输媒介所决定，如传输媒介基本不随时间变化，则它构成的信道属于恒参信道。

若信道的冲激响应为 ℎ(𝑡)，信道输入为 𝑥(𝑡)，则信道的输出为$𝑦(𝑡)=𝑥(𝑡)∗ℎ(𝑡)+𝑛(𝑡)$,其中𝑛(𝑡)为加性高斯白噪声，双边功率谱密度为$\frac{N_{0}}{2}$W/Hz。

### 无失真信道满足的条件

设信道输入信号为𝑥(𝑡)，输出信号为 𝑦(𝑡)，信道传输函数为 𝐻(𝑓) 。

若满足：
$$
y(t)=\alpha x\left(t-t_{0}\right)  \alpha \in R, t_{0}>0
$$
则称信道为理想的无失真信道。

若信道无失真, 有$H(f)=\alpha e^{-j 2 \pi f t_{0}}$, 即$|H(f)|=\alpha \quad \angle H(f)=\varphi(f)=-2 \pi f t_{0}$

### 时延特性

$$
\tau(f)=-\frac{\varphi(f)}{2 \pi f}=t_{0}, f>0
$$

### 群时延特性

$$
\tau_{\mathrm{G}}(f)=-\frac{1}{2 \pi} \frac{d \varphi(f)}{d f}=t_{0}, f>0
$$

> 信道为理想带通信道，即在信道的通带范围内，信道的幅频特性是常数，群时延特性是常数，则相应的带通信号（通带范围相同）经过该信道时，下面描述正确的是 （B）
>
> A. 信道输出波形无失真
>
> B. 信道输出波形的复包络无失真



### 带通信号的复包络无失真

若带通系统的等效基带系统能使输入输出的复包络满足无失真关系，即


$$
y_{L}(t)=K x_{L}\left(t-t_{0}\right)
$$


其中  K  是任意常数, 则称此带通系统对复包络无失真。 复包络无失真要求:


$$
\begin{aligned}
H(f)=&\{\begin{array}{c}
H_{L}(f-f_{c}), f>0 \\
H_{L}^{*}(-f-f_{c}), f<0
\end{array}=\{\begin{array}{l}
a e^{-j(2 \pi f t_{0}-\theta), f>0} \\
a e^{-j(2 \pi f t_{0}+\theta), f<0}
\end{array}..\\
& \angle H(f)=\varphi(f)=-2 \pi f t_{0}+\theta, f>0 \\
& \tau_{\mathrm{G}}(f)=-\frac{1}{2 \pi} \frac{d \varphi(f)}{d f}=t_{0}, f>0
\end{aligned}
$$


例如最经典的希尔伯特变换器:


$$
\begin{array}{c}
H(f)=-j \operatorname{sgn}(f)=\left\{\begin{array}{ll}
e^{-j \frac{\pi}{2}}, & f>0 \\
e^{j \frac{\pi}{2}}, & f<0
\end{array}\right. \\
\angle H(f)=\varphi(f)=-\frac{\pi}{2}, f>0 \\
\tau_{\mathrm{G}}(f)=-\frac{1}{2 \pi} \frac{d \varphi(f)}{d f}=0, f>0
\end{array}
$$


带通信号


$$
x(t)=m(t) \cos 2 \pi f_{c} t-s(t) \sin 2 \pi f_{c} t \rightarrow x_{L}(t)=m(t)+j s(t)
$$


经过Hilbert 变换器后有


$$
\begin{array}{l}
\hat{x}(t)=s(t) \cos 2 \pi f_{c} t+m(t) \sin 2 \pi f_{c} t \rightarrow \hat{x}_{L}(t)=s(t)-j m(t) \\
=-j x_{L}(t)
\end{array}
$$

### 信道不理想对输出信号的影响

+ **幅频失真**：信号中不同频率分量分别受到信道不同的衰减。它对模拟通信影响较大，导致信号波形畸变，输出信噪比降低。
+ **相频失真**（群时延失真）：信号中不同频率的分量受到信道不同的时延。它对数字通信影响较大，会引起严重的码间干扰，造成误码。
+ **时延特性为常数时，信号传输不引起信号的波形失真；群时延特性为常数时，信号传输不引起信号复包络的失真。**



参考文献：

1. Proakis, John G., et al. *Communication systems engineering*. Vol. 2. New Jersey: Prentice Hall, 1994.
2. Proakis, John G., et al. *SOLUTIONS MANUAL Communication Systems Engineering*. Vol. 2. New Jersey: Prentice Hall, 1994.
3. 周炯槃. 通信原理（第3版）[M\]. 北京：北京邮电大学出版社, 2008.
4. 樊昌信, 曹丽娜. 通信原理（第7版） [M\]. 北京：国防工业出版社, 2012.



[返回首页](https://github.com/timerring/information-theory)