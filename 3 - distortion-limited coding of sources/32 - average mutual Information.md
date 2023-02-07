- [平均互信息](#平均互信息)
  - [平均互信息与各类熵的关系](#平均互信息与各类熵的关系)
  - [维拉图](#维拉图)
  - [条件熵](#条件熵)
  - [平均互信息的性质](#平均互信息的性质)


## 平均互信息

平均互信息定义

$$
I(X ; Y)=E[I(x, y)]=H(X)-H(X \mid Y)
$$

1.  Y 末知,  $\mathrm{X}$  的不确定度为  $\mathrm{H}(\mathrm{X})$ 
2.  Y 已知,  $\mathrm{X}$  的不确定度变为  $\mathbf{H}(\mathbf{X} \mid \mathbf{Y})$ 

**互信息  =  先验不确定性 - 后验不确定性  =  不确定性减少的量**

通信系统中若发端的符号为 X 收端的符号为 Y。如果是 一一对应信道, 接收到 Y 后对 X 的不确定性将完全消除： H(X|Y) = 0，一般情况 H(X|Y) < H(X), 即了解 Y 后对 X 的不确定度将减少。

通过信道传输消除了一些不确定性, 获得了一定的信息， 故$0 \leq I(X ; Y) \leq H(X)$

> $I(X ; Y)=\sum_{i} \sum_{j} p(x_{i} y_{j}) \log \frac{p(x_{i} \mid y_{j})}{p(x_{i})}$
>
> $=\sum_{i} \sum_{j} p(x_{i} y_{j}) \log \frac{p(x_{i} y_{j})}{p(x_{i}) p(y_{j})}=\sum_{i} \sum_{j} p(x_{i} y_{j}) \log \frac{p(y_{j} \mid x_{i})}{p(y_{j})}$
>
> $=I(Y ; X)$

由上，平均互信息具有**互易性**:

$$
I(X ; Y)=I(Y ; X)
$$

> 例 假设一条电线上串联了 8 个灯泡 $ x_{1}, x_{2}, \ldots x_{8}$  如图, 这 8 个灯泡损坏的概率相等  $p(x_{\mathbf{i}})=1 / 8$ , 现 假设只有一个灯泡已损坏, 致使串联灯泡都不能点亮。
>
> 未测量前, 8 个灯泡都有可能损坏, 它们损坏的先验概率:  $p(x_{\mathrm{i}})=1 / 8$ , 这时存在的不确定性
>
> 
> $$
> \mathrm{I}(\mathrm{x}_{i})=\log \frac{1}{\mathrm{p}(\mathrm{x}_{i})}=\log _{2} 8=3 \text { bit }
> $$
> 
>
> 测量 1 次后, 可知 4 个灯泡是好的, 另 4 个灯泡中有一个是坏的,这时后验概率  $p(x_{\mathrm{i}} \mid y)=1 / 4$ ，尚存在的不确定性：
>
> 
> $$
> \mathrm{I}(\mathrm{x}_{i} \mid \mathrm{y})=\log \frac{1}{\mathrm{p}(\mathrm{x}_{i} \mid \mathrm{y})}=\log _{2} 4=2 \text { bit }
> $$
> 
>
> 所获得的信息量就是测量前后不确定性减少的量, 测量1次获得的信息量:
>
> 
> $$
> I(x_{i} ; y_{j})=I(x_{i})-I(x_{i} \mid y)=3-2=1 b i t
> $$

### 平均互信息与各类熵的关系

$$
\begin{array}{c}
I(X ; Y)=H(X)-H(X \mid Y)=H(Y)-H(Y \mid X) \\
=H(X)+H(Y)-H(X Y) \\
H(X Y)=H(X)+H(Y \mid X)=H(Y)+H(X \mid Y) \\
H(X Y) \leq H(X)+H(Y)
\end{array}
$$

熵只是平均不确定性的描述，不确定性的消除两熵之差才等于接收端所获得的信息量；

获得的信息量不应该和不确定性混为一谈。

I(X;Y)表示X和Y之间的密切程度，越大，越密切。



下表有12条训练数据，记录了女性的择偶标准，每条数据包含了4个特征。这4个特征对结果的体现程度是不一样的。如何度量这种不同? 用平均互信息

![](https://raw.githubusercontent.com/timerring/picgo/master/picbed/image-20230205203900235.png)

4 个特征和结果的概率分布分别为
$$
\begin{array}{c}
{\left[\begin{array}{l}
X_{1} \\
P
\end{array}\right]=\left[\begin{array}{ccc}
\text { 帅 } & \text { 不帅 } \\
2 / 3 & 1 / 3
\end{array}\right]\left[\begin{array}{c}
X_{2} \\
P
\end{array}\right]=\left[\begin{array}{ccc}
\text { 好 } & \text { 不好 } & \text { 非常好 } \\
1 / 2 & 1 / 3 & 1 / 6
\end{array}\right]} \\
{\left[\begin{array}{c}
X_{3} \\
P
\end{array}\right]=\left[\begin{array}{ccc}
\text { 矮 } & \text { 高 } & \text { 中 } \\
7 / 12 & 1 / 4 & 1 / 6
\end{array}\right] \quad\left[\begin{array}{c}
X_{4} \\
P
\end{array}\right]=\left[\begin{array}{ll}
\text { 上进 } & \text { 不上进 } \\
2 / 3 & 1 / 3
\end{array}\right]} \\
{\left[\begin{array}{l}
Y \\
P
\end{array}\right]=\left[\begin{array}{cc}
\text { 嫁 } & \text { 不嫁 } \\
1 / 2 & 1 / 2
\end{array}\right]}
\end{array}
$$
特征和结果之间的条件概率为 :

![](https://raw.githubusercontent.com/timerring/picgo/master/picbed/image-20230205204146243.png)
$$
\begin{array}{l}
P\left(Y \mid X_{2}\right)=\left[\begin{array}{cc}
1 / 2 & 1 / 2 \\
1 / 4 & 3 / 4 \\
1 & 0
\end{array}\right] \quad P\left(Y \mid X_{3}\right)=\left[\begin{array}{cc}
1 / 7 & 6 / 7 \\
1 & 0 \\
1 & 0
\end{array}\right] \\
P\left(Y \mid X_{4}\right)=\left[\begin{array}{ll}
5 / 8 & 3 / 8 \\
1 / 4 & 3 / 4
\end{array}\right] \\
\end{array}
$$
从而联合概率为 :
$$
\begin{array}{l}
P\left(X_{1}, Y\right)=\left[\begin{array}{ll}
1 / 4 & 5 / 12 \\
1 / 4 & 1 / 12
\end{array}\right] P\left(X_{2}, Y\right)=\left[\begin{array}{cc}
1 / 4 & 1 / 4 \\
1 / 12 & 1 / 4 \\
1 / 6 & 0
\end{array}\right] \\
P\left(X_{3}, Y\right)=\left[\begin{array}{cc}
1 / 12 & 1 / 2 \\
1 / 4 & 0 \\
1 / 6 & 0
\end{array}\right] P\left(X_{4}, Y\right)=\left[\begin{array}{ll}
5 / 12 & 1 / 4 \\
1 / 12 & 1 / 4
\end{array}\right]
\end{array}
$$
得条件熵:  $H(Y \mid X_{1})=0.9067, H(Y \mid X_{2})=0.7704 ,  H(Y \mid X_{3})=0.3451, H(Y \mid X_{4})=0.9067$ 

平均互信息为:  $I(X_{1} ; Y)=0.0933, I(X_{2} ; Y)=0.2296 ,  I(X_{3} ; Y)=0.6549, I(X_{4} ; Y)=0.0933$ .

结论：身高是最主要特征, 其次是性格。只保留这两项即可。

### 维拉图

![](https://raw.githubusercontent.com/timerring/picgo/master/picbed/image-20221014112645460.png)

$$
\begin{array}{l}
I(X ; Y)=H(X)-H(X \mid Y) \\
=H(Y)-H(Y \mid X) \\
=H(X)+H(Y)-H(X Y) \\
H(X Y)=H(X)+H(Y \mid X) \\
=H(Y)+H(X \mid Y) \\
H(X Y) \leq H(X)+H(Y) \\
H(X) \geq H(X \mid Y) \\
H(Y) \geq H(Y \mid X) \\
\end{array}
$$
若信道是无噪一一对应信道,信道传递概率：
$$
\begin{array}{c}
p(y \mid x)=\left\{\begin{array}{ll}
0 & y \neq f(x) \\
1 & y=f(x)
\end{array}\right. \\
p(x \mid y)=\frac{p(x y)}{p(y)}=\frac{p(x) p(y \mid x)}{\sum p(x) p(y \mid x)}=\left\{\begin{array}{ll}
0 & y \neq f(x) \\
1 & y=f(x)
\end{array}\right.
\end{array}
$$
计算得:
$$
H(X \mid Y)=0 ; H(Y \mid X)=0
$$

$$
I(X ; Y)=H(X)=H(Y)
$$

![](https://raw.githubusercontent.com/timerring/picgo/master/picbed/image-20230205211111462.png)

若信道输入端  $\mathbf{X}$  与输出端 $Y$ 完全统计独立
$$
\begin{array}{cc}
p(y \mid x)=p(y) & p(x \mid y)=p(x) \\
H(X \mid Y)=H(X) ; & H(Y \mid X)=H(Y)
\end{array}
$$
则: $I(X ; Y)=0$

![](https://raw.githubusercontent.com/timerring/picgo/master/picbed/image-20230205211119998.png)



### 条件熵

$H(X|Y)$: **信道疑义度，损失熵**

+ 信源符号通过有噪信道传输后所引起的信息量的损失。

信源X的熵等于接收到的信息量加上损失掉的信息量。

$H(Y|X)$: **噪声熵，散布熵**

+ 它反映了信道中噪声源的不确定性。

输出端信源Y的熵 $H(Y)$ 等于接收到关于X的信息量 $I(X;Y)$ 加上 $H(Y|X)$ ,这完全是由于信道中噪声引起的。

![](https://raw.githubusercontent.com/timerring/picgo/master/picbed/image-20230205211716275.png)

### 平均互信息的性质

非负性：  $I(X ; Y) \geq 0$ 

互易性：  $I(X ; Y)=I(Y ; X)$ 

凸函数性：

+ I(X ; Y)  为概率分布  p(x)  的上凸函数
+ 对于固定的概率分布  p(x), I(X ; Y)  为条件概率  $p(y \mid x)$  的 下凸函数

极值性：$I(X ; Y) \leq H(X) ; I(X ; Y) \leq H(Y)$



> 若信道是下图所示的无躁一一对应信道，则有
>
> ![](https://raw.githubusercontent.com/timerring/picgo/master/picbed/image-20230205212316697.png)
> $$
> \begin{array}{l}
> H(X \mid Y)=0 \\
> H(Y \mid X)=0 \\
> I(X ; Y)=H(X) \\
> I(X ; Y)=H(Y)
> \end{array}
> $$





参考文献：

1. Proakis, John G., et al. *Communication systems engineering*. Vol. 2. New Jersey: Prentice Hall, 1994.
2. Proakis, John G., et al. *SOLUTIONS MANUAL Communication Systems Engineering*. Vol. 2. New Jersey: Prentice Hall, 1994.
3. 周炯槃. 通信原理（第3版）[M\]. 北京：北京邮电大学出版社, 2008.
4. 樊昌信, 曹丽娜. 通信原理（第7版） [M\]. 北京：国防工业出版社, 2012.



[返回首页](https://github.com/timerring/information-theory)