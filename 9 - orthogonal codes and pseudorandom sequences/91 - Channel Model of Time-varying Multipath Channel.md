- [时变多径信道的信道模型](#时变多径信道的信道模型)
  - [抽头延迟线信道模型](#抽头延迟线信道模型)


> 第一代移动通信系统的关键技术有 ABCD
>
> A. 蜂窝网
>
> B. FDMA
>
> C. 模拟调制
>
> D. 主要有AMPS和TACS两种制式
>
> 第二代移动通信系统的关键技术有 ABCD
>
> A. 数字调制(GMSK)
>
> B. TDMA/CDMA
>
> C. 开始支持数据业务(GPRS)
>
> D. 主要有GSM和CDMA1X (IS-95)两种制式
>
> 第三代移动通信系统的关键技术有 ABCD
>
> A. 直接序列扩频
>
> B. CDMA
>
> C. 全面支持数据业务，语音和数据分开
>
> D. 有WCDMA、CDMA2000和TD-SCDMA三种制式
>
> 第四代移动通信系统(LTE)的关键技术有  ABCD
>
> A. OFDMA
>
> B. MIMO
>
> C. 支持数据业务，语音加载在数据网上(VoLTE)
>
> D. 智能天线、软件定义的无线电(SDR)
>
> 第五代移动通信系统(NR)的主要技术 ABCD
>
> A. NOMA/FBMC
>
> B. Massive MIMO
>
> C. 波束分割多址技术（BDMA)
>
> D. D2D通信(D: device)

+ 复习多径信道模型;
+ 定义正交码，能够构造哈达马矩阵并写出沃尔什序列，并画出对应的沃尔什函数波形;
+ 定义伪随机码，给定移位寄存器的结构，能够写出其所产生的伪随机序列;
+ 识记m序列的定义;
+ 能够根据要求，设计m序列的产生器。

## 时变多径信道的信道模型

![](https://raw.githubusercontent.com/timerring/picgo/master/picbed/image-20230211095158250.png)

### 抽头延迟线信道模型

![](https://raw.githubusercontent.com/timerring/picgo/master/picbed/image-20230211095220493.png)

W信道传输信号带宽,  1 / W  为时间分辨率, 抽头  $\{c_{n}(t)\}$  为互不相关的高斯随机过程。延迟线长度与多径信道中的时间弥散量相对应。多径扩展可以表示为  $T_{\mathrm{m}}=\mathrm{L} / \mathrm{W}$ , 其中  $\mathrm{L}$  为多径信号分量的最大数目。

例：试确定一个适用于飞机间通信的信道模型, 其中包括一条直接信号传输路径和由周围地面地形对信号散射而引起的二次传输路径。 二次传输路径相对于直接路径有  $\tau=\mathbf{1 0} \mu \mathrm{s}$  的传输时延, 信号带宽为  $\mathrm{W}=\mathbf{1 0 0} \mathrm{kHz}$  。

解:  $100 \mathrm{kHz}$  信号可提供  $1 / \mathrm{W}=10 \mu \mathrm{s}$  的时间分辨率。因为 2 条路径的相对时延是  $10 \mu \mathrm{s}$ , 所以二次信号路径是可分辨的。信道为 2 抽头模型。

试确定一个适用于飞机间通信的信道模型, 其中包括一条直接信号传输路径和由周围地面地形对信号 散射而引起的二次传输路径。二次传输路径相对于直接路径有  $\tau=10 \mu \mathrm{s}$  的传输时延, 若传输信号带宽为  $10 \mathrm{kHz}$  ，信道模型如何?单径信道



参考文献：

1. Proakis, John G., et al. *Communication systems engineering*. Vol. 2. New Jersey: Prentice Hall, 1994.
2. Proakis, John G., et al. *SOLUTIONS MANUAL Communication Systems Engineering*. Vol. 2. New Jersey: Prentice Hall, 1994.
3. 周炯槃. 通信原理（第3版）[M\]. 北京：北京邮电大学出版社, 2008.
4. 樊昌信, 曹丽娜. 通信原理（第7版） [M\]. 北京：国防工业出版社, 2012.



[返回首页](https://github.com/timerring/information-theory)