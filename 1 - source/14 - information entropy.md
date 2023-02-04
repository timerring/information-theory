- [信息熵](#信息熵)
  - [信息熵的物理含义](#信息熵的物理含义)


## 信息熵

信源符号**自信息的数学期望**为信源的平均信息量——**信息熵**  
$$
H(X)=E\left(I\left(X_{i}\right)\right)=-\sum_{i=1}^{N} p_{i} \log p_{i} \quad  bit/symbol
$$
注意: $\mathbf{H}(\mathbf{X})$  是一个数, 不是随机变量.

> Example  请计算下述离散无记忆二进制信源的信息熵。
>
> $\left(\begin{array}{l}
> X \\
> p
> \end{array}\right)=\left(\begin{array}{cc}
> 0 & 1 \\
> p & 1-p
> \end{array}\right)$
>
> Solution
>
> $H(X)=-p \log p-(1-p) \log (1-p)$

### 信息熵的物理含义

1.信息熵H(X)表示信源输出后，**每个消息（符号）所提供的平均信息量**;

2.信息熵H(X)表示信源输出前，**信源的平均不确定性**;

3.用信息熵H(X)来表征变量X的随机性。

注: **信息熵不等于平均获得的信息量(仅是能提供的信息量)**。一般情况下获得的信息量是两熵之差，而不是信息熵本身（获得的还是需要根据实际计算）。

> Example:
>
> 甲地天气预报， $\left[\begin{array}{c}X \\ p(X)\end{array}\right]=\left[\begin{array}{cccc}\text {晴} & \text {阴} & \text {雨} & \text {雪}\\ \frac{1}{2} & \frac{1}{2} & \frac{1}{8} & \frac{1}{8}\end{array}\right]$ 
>
> 乙地天气预报 $\left[\begin{array}{c}Y \\ p(Y)\end{array}\right]=\left[\begin{array}{cc}\text { 晴 } & \text { 雨 } \\ \frac{7}{8} & \frac{1}{8}\end{array}\right]$ 
>
> 求：两地天气预报各自提供的平均信息量
>
> 解:  
>
> - $\mathrm{H}(\mathrm{X})=-\frac{1}{2} \log \frac{1}{2}-\frac{1}{4} \log \frac{1}{4}-\frac{1}{8} \log \frac{1}{8}-\frac{1}{8} \log \frac{1}{8}=1.75 \quad$  比特/符号  
> - $\mathrm{H}(\mathrm{Y})=-\frac{7}{8} \log \frac{7}{8}-\frac{1}{8} \log \frac{1}{8}=0.544 \quad$ 比特/符号 
> - **甲地提供的平均信息量大于乙地。**
>
> 甲、乙地天气预报为两极端情况:
>
> $\left[\begin{array}{l}
> X \\
> p(x)
> \end{array}\right]=\left[\begin{array}{cccc}
> \text { 晴 } & \text { 阴 } & \text { 雨 } & \text { 雪 } \\
> 1 & 0 & 0 & 0
> \end{array}\right] \quad\left[\begin{array}{l}
> \mathrm{Y} \\
> \mathrm{p}(\mathrm{y})
> \end{array}\right]=\left[\begin{array}{cc}
> \text { 晴 } & \text { 雨 } \\
> 1 & 0
> \end{array}\right]$
>
> $\mathrm{H}(\mathrm{X})=-1 \log 1-0 \log 0-0 \log 0-0 \log 0 = 0$比特/符号
>
> $\mathrm{H}(\mathrm{Y})=-1 \log 1-0 \log 0=0$  比特/符号
>
> $\lim \varepsilon \log \varepsilon=0$
>
> + 信源是**确定**信源, 所以不存在不确定性, 信息熵等于零。
>
> 甲、乙地天气预报为两极端情况:
>
> $\left[\begin{array}{c}X \\ p(x)\end{array}\right]=\left[\begin{array}{cccc}\text { 晴 } & \text { 阴 } & \text { 雨 } & \text { 雪 } \\ 1 / 4 & 1 / 4 & 1 / 4 & 1 / 4\end{array}\right] \quad\left[\begin{array}{l}\mathrm{Y} \\ \mathrm{p}(\mathrm{y})\end{array}\right]=\left[\begin{array}{cc}\text { 晴 } & \text { 雨 } \\ 1 / 2 & 1 / 2\end{array}\right]$
>
> $\mathrm{H}(\mathrm{X})=-\log \frac{1}{4}=2$  比特/符号
>
> $\mathrm{H}(\mathrm{Y})=-\log \frac{1}{2}=1$  比特/符号
>
> - 这种情况下,**信源的不确定性最大,信息熵最大**。
> - 甲地比乙地提供更多的信息量。因为甲地可能出现的消 息数多于て地可能出现的消息数, 不确定性更大。

结论:  由上可知，信源熵大于等于0（若信源输出为确定符号)而小于等于log(N)（信源输出的不确定性最大)。
$$
0≤H(X)≤ log(N)
$$
其中N为信源字符集元素的个数

> Example 某信号带宽为4000Hz ，以奈奎斯特速率抽样。假设其抽样序列可以建模成一个字符集为A={-2,-1,0,1,2} 的DMS，相应的概率为{1/2,1/4,1/8,1/16,1/16},求信源的速率(b/s)
>
> $H(X)=\frac{1}{2} \log 2+\frac{1}{4} \log 4+\frac{1}{8} \log 8+2 \times \frac{1}{16} \log 16 =\frac{15}{8} \quad \mathrm{bit} / \mathrm{symbol}$
>
> $R_{b}=2 \times 4000 \times H(X)=15 K  bit  / \mathrm{sec}$
>
> 其中 $R_{\mathrm{b}}$ 为信息速率。
>
> 注：奈奎斯特抽样速率为 $2 \mathbf{W}$。信息速率Rb=平均信息量H(X)×码元率B（波特率），单位为bit/s。



参考文献：

1. Proakis, John G., et al. *Communication systems engineering*. Vol. 2. New Jersey: Prentice Hall, 1994.
2. Proakis, John G., et al. *SOLUTIONS MANUAL Communication Systems Engineering*. Vol. 2. New Jersey: Prentice Hall, 1994.
3. 周炯槃. 通信原理（第3版）[M\]. 北京：北京邮电大学出版社, 2008.
4. 樊昌信, 曹丽娜. 通信原理（第7版） [M\]. 北京：国防工业出版社, 2012.



[返回首页](https://github.com/timerring/information-theory)
