# information-theory

> The repository contains the core knowledge of Information Theory and Coding, organized by knowledge points and can be used as a reference for teaching or studying.

本项目包含**信息论与编码**的核心知识，按知识点组织，可作为教学或学习的参考。

## Content

| Chapter                              | section                                                      | content                                                      |
| ------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| 绪论                                 | [绪论](https://github.com/timerring/information-theory/blob/main/01_introduction.md) | 信息、消息和信号  \|  信息论研究的内容  \|  发展历程         |
| 信源                                 | [信源分类](https://github.com/timerring/information-theory/blob/main/1%20-%20source/11%20-%20source%20classification.md) | 输出的信号取值分类 \|  输出信号(符号间)的依赖关系            |
|                                      | [信源数学模型](https://github.com/timerring/information-theory/blob/main/1%20-%20source/12%20-%20source%20mathematical%20model.md) | 单符号离散无记忆信源  \|  多维离散无记忆信源  \|  离散无记忆信源的扩展源 |
|                                      | [自信息](https://github.com/timerring/information-theory/blob/main/1%20-%20source/13%20-%20self%20information.md) | 信息量  \|  自信息定义  \|  联合自信息   \|  条件自信息      |
|                                      | [信息熵](https://github.com/timerring/information-theory/blob/main/1%20-%20source/14%20-%20information%20entropy.md) | 信息熵的物理含义                                             |
|                                      | [联合熵和条件熵](https://github.com/timerring/information-theory/blob/main/1%20-%20source/15%20-%20Joint%20Entropy%20and%20Conditional%20Entropy.md) | 联合熵  \|  条件熵                                           |
|                                      | [熵速率](https://github.com/timerring/information-theory/blob/main/1%20-%20source/16%20-%20entropy%20rate.md) | 熵速率  \| 各类熵的关系                                      |
|                                      | [序列熵](https://github.com/timerring/information-theory/blob/main/1%20-%20source/17%20-%20sequence%20entropy.md) | 离散无记忆信源的序列熵  \|  离散有记忆信源的序列熵           |
|                                      | [极限熵和冗余度]()                                           | 极限熵  \|  冗余度                                           |
| &emsp;                               | &emsp;                                                       | &emsp;                                                       |
| 离散信源的无失真编码                 | [编码的基本概念](https://github.com/timerring/information-theory/blob/main/2%20-%20distortionless%20coding%20of%20discrete%20sources/21%20-%20basic%20concepts%20of%20coding.md) | 信源编码  \|  分类  \|  前缀条件                             |
|                                      | [无失真信源编码](https://github.com/timerring/information-theory/blob/main/2%20-%20distortionless%20coding%20of%20discrete%20sources/22%20-%20lossless%20source%20coding.md) | 无失真定长编码定理  \|  无失真变长编码定理  \|  无失真信源编码定理 |
|                                      | [霍夫曼编码](https://github.com/timerring/information-theory/blob/main/2%20-%20distortionless%20coding%20of%20discrete%20sources/23%20-%20huffman%20coding.md) | 最佳变长编码  \|  霍夫曼编码  \|  L-Z编码                    |
| &emsp;                               | &emsp;                                                       | &emsp;                                                       |
| 信源的限失真编码定理                 | [互信息](https://github.com/timerring/information-theory/blob/main/3%20-%20distortion-limited%20coding%20of%20sources/31%20-%20mutual%20information.md) | [有（限）失真信源编码](https://github.com/timerring/information-theory/blob/main/3%20-%20distortion-limited%20coding%20of%20sources/31%20-%20mutual%20information.md#有限失真信源编码)  \|  [互信息定义](https://github.com/timerring/information-theory/blob/main/3%20-%20distortion-limited%20coding%20of%20sources/31%20-%20mutual%20information.md#互信息定义)  \|  [互信息的性质](https://github.com/timerring/information-theory/blob/main/3%20-%20distortion-limited%20coding%20of%20sources/31%20-%20mutual%20information.md#互信息的性质) |
|                                      | [平均互信息](https://github.com/timerring/information-theory/blob/main/3%20-%20distortion-limited%20coding%20of%20sources/32%20-%20average%20mutual%20Information.md) | [平均互信息](https://github.com/timerring/information-theory/blob/main/3%20-%20distortion-limited%20coding%20of%20sources/32%20-%20average%20mutual%20Information.md#平均互信息)  \|  [平均互信息与各类熵的关系](https://github.com/timerring/information-theory/blob/main/3%20-%20distortion-limited%20coding%20of%20sources/32%20-%20average%20mutual%20Information.md#平均互信息与各类熵的关系)  \|  [维拉图](https://github.com/timerring/information-theory/blob/main/3%20-%20distortion-limited%20coding%20of%20sources/32%20-%20average%20mutual%20Information.md#维拉图)  \|  [条件熵](https://github.com/timerring/information-theory/blob/main/3%20-%20distortion-limited%20coding%20of%20sources/32%20-%20average%20mutual%20Information.md#条件熵)  \|  [平均互信息的性质](https://github.com/timerring/information-theory/blob/main/3%20-%20distortion-limited%20coding%20of%20sources/32%20-%20average%20mutual%20Information.md#平均互信息的性质) |
|                                      | [失真的概念和定义](https://github.com/timerring/information-theory/blob/main/3%20-%20distortion-limited%20coding%20of%20sources/33%20-%20concept%20and%20definition%20of%20distortion.md) | [信息率失真函数](https://github.com/timerring/information-theory/blob/main/3%20-%20distortion-limited%20coding%20of%20sources/33%20-%20concept%20and%20definition%20of%20distortion.md#信息率失真函数)  \|  [限失真信源编码的必要性](https://github.com/timerring/information-theory/blob/main/3%20-%20distortion-limited%20coding%20of%20sources/33%20-%20concept%20and%20definition%20of%20distortion.md#限失真信源编码的必要性)  \|  [失真度的定义](https://github.com/timerring/information-theory/blob/main/3%20-%20distortion-limited%20coding%20of%20sources/33%20-%20concept%20and%20definition%20of%20distortion.md#失真度的定义)  \|  [系统模型](https://github.com/timerring/information-theory/blob/main/3%20-%20distortion-limited%20coding%20of%20sources/33%20-%20concept%20and%20definition%20of%20distortion.md#系统模型) |
|                                      | [失真函数](https://github.com/timerring/information-theory/blob/main/3%20-%20distortion-limited%20coding%20of%20sources/34%20-%20distortion%20function.md) | [失真函数](https://github.com/timerring/information-theory/blob/main/3%20-%20distortion-limited%20coding%20of%20sources/34%20-%20distortion%20function.md#失真函数)  \|  [失真矩阵](https://github.com/timerring/information-theory/blob/main/3%20-%20distortion-limited%20coding%20of%20sources/34%20-%20distortion%20function.md#失真矩阵)  \|  [平均失真](https://github.com/timerring/information-theory/blob/main/3%20-%20distortion-limited%20coding%20of%20sources/34%20-%20distortion%20function.md#平均失真) |
|                                      | [信息率失真函数](https://github.com/timerring/information-theory/blob/main/3%20-%20distortion-limited%20coding%20of%20sources/35%20-%20information%20rate%20distortion%20function.md) | [信息率失真函数](https://github.com/timerring/information-theory/blob/main/3%20-%20distortion-limited%20coding%20of%20sources/35%20-%20information%20rate%20distortion%20function.md#信息率失真函数)  \|  [信道容量](https://github.com/timerring/information-theory/blob/main/3%20-%20distortion-limited%20coding%20of%20sources/35%20-%20information%20rate%20distortion%20function.md#信道容量)  \|  [平均互信息再讨论](https://github.com/timerring/information-theory/blob/main/3%20-%20distortion-limited%20coding%20of%20sources/35%20-%20information%20rate%20distortion%20function.md#平均互信息再讨论) |
|                                      |                                                              | &emsp;&emsp;                                                 |
| 信息率失真函数与信源的限失真编码定理 | [R(D) 的定义域](https://github.com/timerring/information-theory/blob/main/4%20-%20information%20rate-distortion%20function%20and%20distortion-limited%20coding%20theorem%20of%20information%20source/41%20-%20the%20domain%20of%20R(D).md) | [连续信源的熵](https://github.com/timerring/information-theory/blob/main/4%20-%20information%20rate-distortion%20function%20and%20distortion-limited%20coding%20theorem%20of%20information%20source/41%20-%20the%20domain%20of%20R(D).md#连续信源的熵)  \|  [R(D) 的定义域](https://github.com/timerring/information-theory/blob/main/4%20-%20information%20rate-distortion%20function%20and%20distortion-limited%20coding%20theorem%20of%20information%20source/41%20-%20the%20domain%20of%20R(D).md#rd-的定义域) |
|                                      | [信息率失真函数的性质](https://github.com/timerring/information-theory/blob/main/4%20-%20information%20rate-distortion%20function%20and%20distortion-limited%20coding%20theorem%20of%20information%20source/42%20-%20properties%20of%20information%20rate%20distortion%20function.md) | [信息率失真函数的性质](https://github.com/timerring/information-theory/blob/main/4%20-%20information%20rate-distortion%20function%20and%20distortion-limited%20coding%20theorem%20of%20information%20source/42%20-%20properties%20of%20information%20rate%20distortion%20function.md#信息率失真函数的性质)  \|  [实现限失真信源编码的方式](https://github.com/timerring/information-theory/blob/main/4%20-%20information%20rate-distortion%20function%20and%20distortion-limited%20coding%20theorem%20of%20information%20source/42%20-%20properties%20of%20information%20rate%20distortion%20function.md#实现限失真信源编码的方式) |
|                                      | [离散信源 R(D)计算](https://github.com/timerring/information-theory/blob/main/4%20-%20information%20rate-distortion%20function%20and%20distortion-limited%20coding%20theorem%20of%20information%20source/43%20-%20discrete%20source%20R(D)%20calculation.md) | [离散信源 R(D)计算](https://github.com/timerring/information-theory/blob/main/4%20-%20information%20rate-distortion%20function%20and%20distortion-limited%20coding%20theorem%20of%20information%20source/43%20-%20discrete%20source%20R(D)%20calculation.md#离散信源-rd计算)  \|  [二元对称信源的 R(D) 函数](https://github.com/timerring/information-theory/blob/main/4%20-%20information%20rate-distortion%20function%20and%20distortion-limited%20coding%20theorem%20of%20information%20source/43%20-%20discrete%20source%20R(D)%20calculation.md#二元对称信源的--rd--函数)  \|  [高斯信源的 R(D)函数](https://github.com/timerring/information-theory/blob/main/4%20-%20information%20rate-distortion%20function%20and%20distortion-limited%20coding%20theorem%20of%20information%20source/43%20-%20discrete%20source%20R(D)%20calculation.md#高斯信源的-rd函数)  \|  [限失真信源编码定理](https://github.com/timerring/information-theory/blob/main/4%20-%20information%20rate-distortion%20function%20and%20distortion-limited%20coding%20theorem%20of%20information%20source/43%20-%20discrete%20source%20R(D)%20calculation.md#限失真信源编码定理) |
|                                      |                                                              | &emsp;                                                       |
| 信道                                 | [信道的定义和分类](https://github.com/timerring/information-theory/blob/main/5%20-%20channel/51%20-%20channel%20definition%20and%20classification.md) | [狭义信道](https://github.com/timerring/information-theory/blob/main/5%20-%20channel/51%20-%20channel%20definition%20and%20classification.md#狭义信道)  \|  [广义信道](https://github.com/timerring/information-theory/blob/main/5%20-%20channel/51%20-%20channel%20definition%20and%20classification.md#广义信道) |
|                                      | [信道的数学模型](https://github.com/timerring/information-theory/blob/main/5%20-%20channel/52%20-%20channel%20mathematical%20model.md#信道的数学模型) | [广义信道的数学模型](https://github.com/timerring/information-theory/blob/main/5%20-%20channel/52%20-%20channel%20mathematical%20model.md#广义信道的数学模型)  \|  [连续信道的数学模型](https://github.com/timerring/information-theory/blob/main/5%20-%20channel/52%20-%20channel%20mathematical%20model.md#连续信道的数学模型)  \|  [离散信道数学模型](https://github.com/timerring/information-theory/blob/main/5%20-%20channel/52%20-%20channel%20mathematical%20model.md#离散信道数学模型)  \|  [半连续信道](https://github.com/timerring/information-theory/blob/main/5%20-%20channel/52%20-%20channel%20mathematical%20model.md#半连续信道) |
|                                      | [恒参信道特性及其对信号传输的影响](https://github.com/timerring/information-theory/blob/main/5%20-%20channel/53%20-%20constant%20parameter%20channel%20characteristics.md#恒参信道特性及其对信号传输的影响) | [无失真信道满足的条件](https://github.com/timerring/information-theory/blob/main/5%20-%20channel/53%20-%20constant%20parameter%20channel%20characteristics.md#无失真信道满足的条件)  \|  [时延特性](https://github.com/timerring/information-theory/blob/main/5%20-%20channel/53%20-%20constant%20parameter%20channel%20characteristics.md#时延特性)  \|  [群时延特性](https://github.com/timerring/information-theory/blob/main/5%20-%20channel/53%20-%20constant%20parameter%20channel%20characteristics.md#群时延特性)  \|  [带通信号的复包络无失真](https://github.com/timerring/information-theory/blob/main/5%20-%20channel/53%20-%20constant%20parameter%20channel%20characteristics.md#带通信号的复包络无失真)  \|  [信道不理想对输出信号的影响](https://github.com/timerring/information-theory/blob/main/5%20-%20channel/53%20-%20constant%20parameter%20channel%20characteristics.md#信道不理想对输出信号的影响) |
|                                      | [随参信道特性](https://github.com/timerring/information-theory/blob/main/5%20-%20channel/54%20-%20dependent%20channel%20characteristics.md#随参信道特性) | [随参信道数学模型的建立](https://github.com/timerring/information-theory/blob/main/5%20-%20channel/54%20-%20dependent%20channel%20characteristics.md#随参信道数学模型的建立)  \|  [随参信道对信号传输的影响](https://github.com/timerring/information-theory/blob/main/5%20-%20channel/54%20-%20dependent%20channel%20characteristics.md#随参信道对信号传输的影响)  \|  [多径随参信道的时延扩展与相干带宽](https://github.com/timerring/information-theory/blob/main/5%20-%20channel/54%20-%20dependent%20channel%20characteristics.md#多径随参信道的时延扩展与相干带宽)  \|  [总结](https://github.com/timerring/information-theory/blob/main/5%20-%20channel/54%20-%20dependent%20channel%20characteristics.md#总结) |
|                                      | [移动信道的多普勒扩展及相干时间](https://github.com/timerring/information-theory/blob/main/5%20-%20channel/55%20-%20doppler%20spread%20and%20coherence%20time%20of%20mobile%20channels.md#移动信道的多普勒扩展及相干时间) | [多普勒扩展](https://github.com/timerring/information-theory/blob/main/5%20-%20channel/55%20-%20doppler%20spread%20and%20coherence%20time%20of%20mobile%20channels.md#1多普勒扩展)  \|  [信道的相干时间 Tc 和多普勒频率扩展](https://github.com/timerring/information-theory/blob/main/5%20-%20channel/55%20-%20doppler%20spread%20and%20coherence%20time%20of%20mobile%20channels.md#2信道的相干时间-tc-和多普勒频率扩展)  \|  [多普勒扩展对衰落的影响](https://github.com/timerring/information-theory/blob/main/5%20-%20channel/55%20-%20doppler%20spread%20and%20coherence%20time%20of%20mobile%20channels.md#3多普勒扩展对衰落的影响)  \|  [同时考虑随参信道的多径时延扩展及多普勒扩展对衰落的影响](https://github.com/timerring/information-theory/blob/main/5%20-%20channel/55%20-%20doppler%20spread%20and%20coherence%20time%20of%20mobile%20channels.md#4同时考虑随参信道的多径时延扩展及多普勒扩展对衰落的影响)  \|  [抗衰落的方案](https://github.com/timerring/information-theory/blob/main/5%20-%20channel/55%20-%20doppler%20spread%20and%20coherence%20time%20of%20mobile%20channels.md#5抗衰落的方案)  \|  [总结](https://github.com/timerring/information-theory/blob/main/5%20-%20channel/55%20-%20doppler%20spread%20and%20coherence%20time%20of%20mobile%20channels.md#总结) |
|                                      | [分集](https://github.com/timerring/information-theory/blob/main/5%20-%20channel/56%20-%20separation.md#分集) | [分集的概念](https://github.com/timerring/information-theory/blob/main/5%20-%20channel/56%20-%20separation.md#分集的概念)  \|  [分集的方法](https://github.com/timerring/information-theory/blob/main/5%20-%20channel/56%20-%20separation.md#分集的方法)  \|  [路径合并方式](https://github.com/timerring/information-theory/blob/main/5%20-%20channel/56%20-%20separation.md#路径合并方式)  \|  [Alamouti空时分组码(STBC)简介](https://github.com/timerring/information-theory/blob/main/5%20-%20channel/56%20-%20separation.md#alamouti空时分组码stbc简介) |
|                                      | [信道容量](https://github.com/timerring/information-theory/blob/main/5%20-%20channel/57%20-%20channel%20capacity.md#信道容量) | [信道容量的定义](https://github.com/timerring/information-theory/blob/main/5%20-%20channel/57%20-%20channel%20capacity.md#信道容量的定义)  \|  [三种特殊信道的容量](https://github.com/timerring/information-theory/blob/main/5%20-%20channel/57%20-%20channel%20capacity.md#三种特殊信道的容量)  \|  [典型信道的信道容量](https://github.com/timerring/information-theory/blob/main/5%20-%20channel/57%20-%20channel%20capacity.md#典型信道的信道容量)  \|  [信源与信道的匹配](https://github.com/timerring/information-theory/blob/main/5%20-%20channel/57%20-%20channel%20capacity.md#信源与信道的匹配) |
|                                      | &emsp;                                                       | &emsp;                                                       |
| 信道编码                             | [信道编码](https://github.com/timerring/information-theory/blob/main/6%20-%20channel%20coding/61%20-%20channel%20coding.md#信道编码) | [信道编码的基本概念](https://github.com/timerring/information-theory/blob/main/6%20-%20channel%20coding/61%20-%20channel%20coding.md#信道编码的基本概念) |
|                                      | [基本线性分组码与性能参数](https://github.com/timerring/information-theory/blob/main/6%20-%20channel%20coding/62%20-%20Basic%20Linear%20Block%20Codes%20and%20Performance%20Parameters.md#基本线性分组码与性能参数) | [线性分组码(n,k)定义](https://github.com/timerring/information-theory/blob/main/6%20-%20channel%20coding/62%20-%20Basic%20Linear%20Block%20Codes%20and%20Performance%20Parameters.md#线性分组码nk定义)  \|  [信道编码性能参数](https://github.com/timerring/information-theory/blob/main/6%20-%20channel%20coding/62%20-%20Basic%20Linear%20Block%20Codes%20and%20Performance%20Parameters.md#信道编码性能参数)  \|  [基本线性分组码](https://github.com/timerring/information-theory/blob/main/6%20-%20channel%20coding/62%20-%20Basic%20Linear%20Block%20Codes%20and%20Performance%20Parameters.md#基本线性分组码)  \|  [差错控制类型对信道编码的要求](https://github.com/timerring/information-theory/blob/main/6%20-%20channel%20coding/62%20-%20Basic%20Linear%20Block%20Codes%20and%20Performance%20Parameters.md#差错控制类型对信道编码的要求)  \|  [有限域运算、矩阵运算](https://github.com/timerring/information-theory/blob/main/6%20-%20channel%20coding/62%20-%20Basic%20Linear%20Block%20Codes%20and%20Performance%20Parameters.md#信道编码主要涉及的数学知识有限域运算矩阵运算) |
|                                      | [线性分组码](https://github.com/timerring/information-theory/blob/main/6%20-%20channel%20coding/63%20-%20linear%20block%20code.md#线性分组码) | [基本概念](https://github.com/timerring/information-theory/blob/main/6%20-%20channel%20coding/63%20-%20linear%20block%20code.md#基本概念)  \|  [编码-生成矩阵](https://github.com/timerring/information-theory/blob/main/6%20-%20channel%20coding/63%20-%20linear%20block%20code.md#编码-生成矩阵)  \|  [检错-监督矩阵](https://github.com/timerring/information-theory/blob/main/6%20-%20channel%20coding/63%20-%20linear%20block%20code.md#检错-监督矩阵) |
|                                      | [系统码的编译码](https://github.com/timerring/information-theory/blob/main/6%20-%20channel%20coding/64%20-%20Coding%20and%20Decoding%20of%20Systematic%20Codes%20and%20Hamming%20Codes.md#系统码的编译码) | [线性分组码的编码器](https://github.com/timerring/information-theory/blob/main/6%20-%20channel%20coding/64%20-%20Coding%20and%20Decoding%20of%20Systematic%20Codes%20and%20Hamming%20Codes.md#线性分组码的编码器)  \|  [线性分组码的译码器](https://github.com/timerring/information-theory/blob/main/6%20-%20channel%20coding/64%20-%20Coding%20and%20Decoding%20of%20Systematic%20Codes%20and%20Hamming%20Codes.md#线性分组码的译码器)  \|  [汉明码](https://github.com/timerring/information-theory/blob/main/6%20-%20channel%20coding/64%20-%20Coding%20and%20Decoding%20of%20Systematic%20Codes%20and%20Hamming%20Codes.md#汉明码)  \|  [总结](https://github.com/timerring/information-theory/blob/main/6%20-%20channel%20coding/64%20-%20Coding%20and%20Decoding%20of%20Systematic%20Codes%20and%20Hamming%20Codes.md#总结) |
|                                      | &emsp;                                                       | &emsp;                                                       |
| 循环码                               | [循环码](https://github.com/timerring/information-theory/blob/main/7%20-%20cyclic%20code/71%20-%20cyclic%20code.md#循环码) | [循环码的特点](https://github.com/timerring/information-theory/blob/main/7%20-%20cyclic%20code/71%20-%20cyclic%20code.md#循环码的特点)  \|  [基本概念](https://github.com/timerring/information-theory/blob/main/7%20-%20cyclic%20code/71%20-%20cyclic%20code.md#基本概念)  \|  [循环码的多项式描述](https://github.com/timerring/information-theory/blob/main/7%20-%20cyclic%20code/71%20-%20cyclic%20code.md#循环码的多项式描述) |
|                                      | [循环码的编码](https://github.com/timerring/information-theory/blob/main/7%20-%20cyclic%20code/72%20-%20Cyclic%20code%20encoding.md#循环码的编码) | [循环码的编码](https://github.com/timerring/information-theory/blob/main/7%20-%20cyclic%20code/72%20-%20Cyclic%20code%20encoding.md#循环码的编码)  \|  [循环码的伴随多项式译码](https://github.com/timerring/information-theory/blob/main/7%20-%20cyclic%20code/72%20-%20Cyclic%20code%20encoding.md#循环码的伴随多项式译码)  \|  [循环冗余校验 (Cyclic Redundancy Check, CRC)](https://github.com/timerring/information-theory/blob/main/7%20-%20cyclic%20code/72%20-%20Cyclic%20code%20encoding.md#循环冗余校验-cyclic-redundancy-check-crc) |
|                                      | [循环码生成多项式与生成矩阵](https://github.com/timerring/information-theory/blob/main/7%20-%20cyclic%20code/73%20-%20Cyclic%20code%20generator%20polynomial%20and%20generator%20matrix.md#循环码生成多项式与生成矩阵) | [循环码生成多项式与生成矩阵](https://github.com/timerring/information-theory/blob/main/7%20-%20cyclic%20code/73%20-%20Cyclic%20code%20generator%20polynomial%20and%20generator%20matrix.md#循环码生成多项式与生成矩阵)  \|  [循环码的监督 (校验) 矩阵](https://github.com/timerring/information-theory/blob/main/7%20-%20cyclic%20code/73%20-%20Cyclic%20code%20generator%20polynomial%20and%20generator%20matrix.md#循环码的监督-校验--矩阵) |
|                                      | [BCH 码和RS 码](https://github.com/timerring/information-theory/blob/main/7%20-%20cyclic%20code/74%20-%20BCH%20code%20and%20RS%20code.md) | [BCH码-循环码](https://github.com/timerring/information-theory/blob/main/7%20-%20cyclic%20code/74%20-%20BCH%20code%20and%20RS%20code.md#bch码-循环码)  \|  [RS码](https://github.com/timerring/information-theory/blob/main/7%20-%20cyclic%20code/74%20-%20BCH%20code%20and%20RS%20code.md#rs码)  \|  [总结](https://github.com/timerring/information-theory/blob/main/7%20-%20cyclic%20code/74%20-%20BCH%20code%20and%20RS%20code.md#总结) |
|                                      | &emsp;                                                       | &emsp;                                                       |
| 卷积码                               | [卷积码基础](https://github.com/timerring/information-theory/blob/main/8%20-%20convolutional%20code/81%20-%20Convolutional%20Code%20Basics.md#卷积码基础) | [卷积码的概念](https://github.com/timerring/information-theory/blob/main/8%20-%20convolutional%20code/81%20-%20Convolutional%20Code%20Basics.md#卷积码的概念)  \|  [卷积码编码器的结构](https://github.com/timerring/information-theory/blob/main/8%20-%20convolutional%20code/81%20-%20Convolutional%20Code%20Basics.md#卷积码编码器的结构)  \|  [卷积编码器表示](https://github.com/timerring/information-theory/blob/main/8%20-%20convolutional%20code/81%20-%20Convolutional%20Code%20Basics.md#卷积编码器表示) |
|                                      | [卷积译码](https://github.com/timerring/information-theory/blob/main/8%20-%20convolutional%20code/82%20-%20convolutional%20decoding.md#卷积译码) | [最大似然译码](https://github.com/timerring/information-theory/blob/main/8%20-%20convolutional%20code/82%20-%20convolutional%20decoding.md#最大似然译码)  \|  [卷积译码-维特比卷积译码算法](https://github.com/timerring/information-theory/blob/main/8%20-%20convolutional%20code/82%20-%20convolutional%20decoding.md#卷积译码-维特比卷积译码算法) |
|                                      | [交织技术](https://github.com/timerring/information-theory/blob/main/8%20-%20convolutional%20code/83%20-%20interleaving%20technology.md#交织技术) | [突发错误](https://github.com/timerring/information-theory/blob/main/8%20-%20convolutional%20code/83%20-%20interleaving%20technology.md#1突发错误)  \|  [抗突发错的有效手段——交织](https://github.com/timerring/information-theory/blob/main/8%20-%20convolutional%20code/83%20-%20interleaving%20technology.md#2抗突发错的有效手段交织)  \|  [交织器的三个重要参数](https://github.com/timerring/information-theory/blob/main/8%20-%20convolutional%20code/83%20-%20interleaving%20technology.md#3交织器的三个重要参数) |
|                                      | &emsp;                                                       | &emsp;                                                       |
| 正交码和伪随机序列                   | [时变多径信道的信道模型](https://github.com/timerring/information-theory/blob/main/9%20-%20orthogonal%20codes%20and%20pseudorandom%20sequences/91%20-%20Channel%20Model%20of%20Time-varying%20Multipath%20Channel.md#时变多径信道的信道模型) | [时变多径信道的信道模型](https://github.com/timerring/information-theory/blob/main/9%20-%20orthogonal%20codes%20and%20pseudorandom%20sequences/91%20-%20Channel%20Model%20of%20Time-varying%20Multipath%20Channel.md#时变多径信道的信道模型)  \|  [抽头延迟线信道模型](https://github.com/timerring/information-theory/blob/main/9%20-%20orthogonal%20codes%20and%20pseudorandom%20sequences/91%20-%20Channel%20Model%20of%20Time-varying%20Multipath%20Channel.md#抽头延迟线信道模型) |
|                                      | [正交编码](https://github.com/timerring/information-theory/blob/main/9%20-%20orthogonal%20codes%20and%20pseudorandom%20sequences/92%20-%20Orthogonal%20code.md#正交编码) | [正交编码的基本概念](https://github.com/timerring/information-theory/blob/main/9%20-%20orthogonal%20codes%20and%20pseudorandom%20sequences/92%20-%20Orthogonal%20code.md#正交编码的基本概念)  \|  [正交沃尔什函数](https://github.com/timerring/information-theory/blob/main/9%20-%20orthogonal%20codes%20and%20pseudorandom%20sequences/92%20-%20Orthogonal%20code.md#正交沃尔什函数) |
|                                      | [伪随机码](https://github.com/timerring/information-theory/blob/main/9 - orthogonal codes and pseudorandom sequences/93 - pseudo-random code.md#伪随机码) | [伪随机序列的概念](https://github.com/timerring/information-theory/blob/main/9 - orthogonal codes and pseudorandom sequences/93 - pseudo-random code.md#伪随机序列的概念)  \|  [伪随机序列的产生](https://github.com/timerring/information-theory/blob/main/9 - orthogonal codes and pseudorandom sequences/93 - pseudo-random code.md#伪随机序列的产生) |
|                                      | [m 序列](https://github.com/timerring/information-theory/blob/main/9 - orthogonal codes and pseudorandom sequences/94 - m sequence.md#m-序列-最长线性反馈移位寄存器序列) |                                                              |

### ChangeLog

+ v1.8 Completed chapter 8 update 230219

+ v1.7 Completed chapter 7 update 230218

+ v1.6 Completed chapter 6 update 230216

+ v1.5 Completed chapter 5 update 230214

+ v1.4 Completed chapter 4 update 230207
+ v1.3 Completed chapter 3 update 230207
+ v1.2 Completed distortionless coding of discrete sources chapter update 230205

- v1.1 Completed source chapter update 230204
- v1.0 Completed introduction chapter update 230201

## Reference

[1] [Proakis, John G., et al. *Communication systems engineering*. Vol. 2. New Jersey: Prentice Hall, 1994.](https://github.com/timerring/information-theory/blob/main/reference/communication-systems-engineering.pdf)

[2] [Proakis, John G., et al. *SOLUTIONS MANUAL Communication Systems Engineering*. Vol. 2. New Jersey: Prentice Hall, 1994.](https://github.com/timerring/information-theory/blob/main/reference/communication-systems-engineering-solutions-manual.pdf)

[3] [周炯槃.  通信原理（第3版）[M]. 北京：北京邮电大学出版社,  2008.](https://github.com/timerring/information-theory/blob/main/reference/Principles-of-Communication-Zhou.pdf)

[4] [樊昌信, 曹丽娜.  通信原理（第7版） [M]. 北京：国防工业出版社,  2012.](https://github.com/timerring/information-theory/blob/main/reference/Principles-of-Communication-Fan.pdf)

## Tips

1. 如果存在疑问或发现错误，欢迎提Issues交流订正。
2. 如果遇到图片无法加载的情况，可以考虑使用代理，或者访问[博客网站](https://blog.csdn.net/m0_52316372/category_12102819.html) 。
2. 如果发现Tex数学公式展示异常，可以安装插件[GitHub Math Display](https://chrome.google.com/webstore/detail/github-math-display/cgolaobglebjonjiblcjagnpmdmlgmda?hl=zh-CN)，安装后启用插件，刷新网页即可。也可以下载后本地软件打开。

## More

<div align=center>
<p>扫描下方二维码关注公众号：AIShareLab</p>
<img src="resources/qrcode.jpg" width = "180" height = "180">
</div>


&emsp;&emsp;AIShareLab，一个关注CV、AI、区块链、Web开发、硬件开发、5G通信等领域的热“AI”分享的社群，微信搜索公众号 AIShareLab 一起交流更多相关知识，前沿算法，Paper解读，项目源码，面经总结。﻿

## LICENSE

<a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="知识共享许可协议" style="border-width:0" src="https://img.shields.io/badge/license-CC BY--NC--SA 4.0-lightgrey" /></a><br />本作品采用<a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/">知识共享署名-非商业性使用-相同方式共享 4.0 国际许可协议</a>进行许可。