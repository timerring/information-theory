- [有（限）失真信源编码](#有限失真信源编码)
- [互信息](#互信息)
  - [互信息定义](#互信息定义)
  - [互信息的性质](#互信息的性质)


## 有（限）失真信源编码

有失真信源编码的数学模型如下图所示，将编码过程看成信息经过有扰信道传输的过程。信道输出 Y 即为编码输出。

![](https://raw.githubusercontent.com/timerring/picgo/master/picbed/image-20221014103056798.png)

对离散信道，用信道转移概率（条件概率）p(y|x)表示信道。

![](https://raw.githubusercontent.com/timerring/picgo/master/picbed/image-20221014103343649.png)

如BSC信道：

![](https://raw.githubusercontent.com/timerring/picgo/master/picbed/image-20221014103406732.png)

## 互信息

设有两个随机事件X和Y ,

+ X取值于信源**发出**的离散消息集合
+ Y取值于信宿**收到**的离散符号集合

$$
\left[\begin{array}{l}
X \\
P
\end{array}\right]=\left[\begin{array}{cccc}
x_{1} & x_{2} & \cdots & x_{n} \\
p\left(x_{1}\right) & p\left(x_{2}\right) & \cdots & p\left(x_{n}\right)
\end{array}\right] \quad\left[\begin{array}{l}
Y \\
P
\end{array}\right]=\left[\begin{array}{cccc}
y_{1} & y_{2} & \cdots & y_{n} \\
p\left(y_{1}\right) & p\left(y_{2}\right) & \cdots & p\left(y_{n}\right)
\end{array}\right]
$$

如果信道是**无噪**的,当信源发出消息  $x_{i}$  后,信宿必能准确无误地收到该消息, 彻底消除对  $x_{i}$  的不确定性, 所获得的信息量就是  $x_{i}$  的**自信息  $I(x_{i})$ ，即 $x_{i}$ 本身含有的全部信息**。

一般而言，信道中总是存在着噪声和干扰，信源发出消息  $x_{i}$ ，通过信道后, 信宿只可能收到由于干扰作用引起的某种变形 $y_{j}$ 。(例如BSC信道，可能发出0收到1)

+ 信宿收到  $y_{j}$  后推测信源发出  $x_{i}$  的概率  $p(x_{i} \mid y_{j})$  称为**后验概率**。
+ 信源发出消息  $x_{i}$  的概率  $p(x_{i})$  称为**先验概率**。

### 互信息定义

定义为  **$x_{i}$  的后验概率与先验概率比值的对数**

$$
\begin{array}{c}
I(x_{i} ; y_{j})=\log _{2} \frac{p(x_{i} \mid y_{j})}{p(x_{i})} \\
I(x_{i} ; y_{j})=\log \frac{p(x_{i} \mid y_{j})}{p(x_{i})}=\log \frac{p(x_{i} y_{j})}{p(x_{i}) p(y_{j})}=\log \frac{p(y_{j} \mid x_{i})}{p(y_{j})}=I(y_{j} ; x_{i}) \\
I(x_{i} ; y_{j})=I(x_{i})-I(x_{i} \mid y_{j})=I(y_{j})-I(y_{j} \mid x_{i})
\end{array}
$$
**互信息  $I(x_{i} ; y_{j})$  表示接收到某消息  $y_{j}$  后获得的关于事件  $x_{i}$  的信息量。**单位和自信息相同。



例  、某地二月份天气构成的信源为:
$$
\left[\begin{array}{c}
X \\
p(x)
\end{array}\right]=\left[\begin{array}{cccc}
\text { 晴 } & \text { 阴 } & \text { 雨 } & \text { 雪 } \\
1 / 2 & 1 / 4 & 1 / 8 & 1 / 8
\end{array}\right]
$$
求得自信息量分别为

$$
I\left(x_{1}\right)=1 \text { bit }, I\left(x_{2}\right)=2 \text { bit }, I\left(x_{3}\right)=I\left(x_{4}\right)=3 \text { bit }
$$
若得知 “今天不是晴天” ，作为收到的消息  $y_{1}$ 

当收到  $y_{1}$  后, 各种天气发生的概率变成后验概率:
$$
p\left(x_{1} \mid y_{1}\right)=0, p\left(x_{2} \mid y_{1}\right)=1 / 2, p\left(x_{3} \mid y_{1}\right)=1 / 4, p\left(x_{4} \mid y_{1}\right)=1 / 4
$$

$$
\begin{array}{c}
I\left(x_{1} ; y_{1}\right)=\log _{2} \frac{p\left(x_{1} \mid y_{1}\right)}{p\left(x_{1}\right)}=0 \\
I\left(x_{2} ; y_{1}\right)=\log _{2} \frac{p\left(x_{2} \mid y_{1}\right)}{p\left(x_{2}\right)}=\log _{2} \frac{1 / 2}{1 / 4}=\mathbf{1 b i t} \\
I\left(x_{3} ; y_{1}\right)=I\left(x_{4} ; y_{1}\right)=\log _{2} \frac{1 / 4}{1 / 8}=1 \mathrm{bit}
\end{array}
$$

表明从  $y_{1}$  分别得到了  $x_{2} x_{3} x_{4}$  各 1 比特的信息量。 消息  $y_{1}$  使  $x_{2} x_{3} x_{4}$  的不确定度各减少  1 bit。

### 互信息的性质

- 互易性  $I(x ; y)=I(y ; x)$ 
- 当事件  $\mathbf{x}$,  $\mathbf{y}$  统计独立时,  互信息为 0 , 即  $I(x ; y)=0$
- 互信息**可正可负**
- 任何两事件之间的互信息不可能大于其中任一事件的自信息(见上述公式3)

> 例：设 e 表示事件“降雨”， f 表示事件“空中有乌云”，且 𝒑（𝒆）=𝟎.𝟏𝟐𝟓，𝒑（𝒆|𝒇）=𝟎.𝟖
>
> 求：
>
> 1. 事件“降雨”的自信息
> 2. 在“空中有乌云”条件下，“降雨”的自信息
> 3. 事件“无雨”的自信息
> 4. 在“空中有乌云”条件下，“无雨”的自信息
> 5. “降雨”与“空中有乌云”的互信息
> 6. “无雨”与“空中有乌云”的互信息
>
> 解:  $\bar{e}$  表示 “无雨”, 则  $p(\bar{e})$= 1- p(e) = 0.875 ,  $p(\bar{e} \mid f)$ = 1- $p(e \mid f)$ = 0.2
>
> 故:
> $$
> I(e)=-\log (0.125)=3 b i t \\
> I(e \mid f)=-\log (0.8)=0.322 b i t \\
> I(\bar{e})=-\log (0.875)=0.193  bit\\
> I(\bar{e} \mid f)=-\log (0.2)=2.322 b i t \\
> I(e ; f)=I(e)-I(e \mid f)=3-0.322=2.678 b i t ; \\
> I(\bar{e} ; f)=I(\bar{e})-I(\bar{e} \mid f)=0.193-2.322=-2.129 b i t
> $$
> 说明事件 “空中有乌云” 不利于事件 “无雨” 的出现。

参考文献：

1. Proakis, John G., et al. *Communication systems engineering*. Vol. 2. New Jersey: Prentice Hall, 1994.
2. Proakis, John G., et al. *SOLUTIONS MANUAL Communication Systems Engineering*. Vol. 2. New Jersey: Prentice Hall, 1994.
3. 周炯槃. 通信原理（第3版）[M\]. 北京：北京邮电大学出版社, 2008.
4. 樊昌信, 曹丽娜. 通信原理（第7版） [M\]. 北京：国防工业出版社, 2012.



[返回首页](https://github.com/timerring/information-theory)