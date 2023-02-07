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
|                                      | chapter focus                                                | 信源模型:记忆离散无记忆信源的数学模型。 <br />自信息:会计算。 <br />信息熵、联合熵、条件熵: 会计算，能够分析并计算离散信源的信息速率。<br />列举信息熵、联合熵、条件熵直接的关系。 |
| &emsp;                               | &emsp;                                                       | &emsp;                                                       |
| 离散信源的无失真编码                 | [编码的基本概念](https://github.com/timerring/information-theory/blob/main/2%20-%20distortionless%20coding%20of%20discrete%20sources/21%20-%20basic%20concepts%20of%20coding.md) | 信源编码  \|  分类  \|  前缀条件                             |
|                                      | [无失真信源编码](https://github.com/timerring/information-theory/blob/main/2%20-%20distortionless%20coding%20of%20discrete%20sources/22%20-%20lossless%20source%20coding.md) | 无失真定长编码定理  \|  无失真变长编码定理  \|  无失真信源编码定理 |
|                                      | [霍夫曼编码](https://github.com/timerring/information-theory/blob/main/2%20-%20distortionless%20coding%20of%20discrete%20sources/23%20-%20huffman%20coding.md) | 最佳变长编码  \|  霍夫曼编码  \|  L-Z编码                    |
|                                      | chapter focus                                                | 阐述无失真信源编码的概念和条件;<br />区别并判断给定编码方案是否是无失真编码;<br />解释香农无失真信源编码定理;<br />给定信源数学模型，能够进行二进制霍夫曼编码; |
| &emsp;                               | &emsp;                                                       | &emsp;                                                       |
| 信源的限失真编码定理                 | [互信息](https://github.com/timerring/information-theory/blob/main/3%20-%20distortion-limited%20coding%20of%20sources/31%20-%20mutual%20information.md) | [有（限）失真信源编码](https://github.com/timerring/information-theory/blob/main/3%20-%20distortion-limited%20coding%20of%20sources/31%20-%20mutual%20information.md#有限失真信源编码)  \|  [互信息定义](https://github.com/timerring/information-theory/blob/main/3%20-%20distortion-limited%20coding%20of%20sources/31%20-%20mutual%20information.md#互信息定义)  \|  [互信息的性质](https://github.com/timerring/information-theory/blob/main/3%20-%20distortion-limited%20coding%20of%20sources/31%20-%20mutual%20information.md#互信息的性质) |
|                                      | [平均互信息](https://github.com/timerring/information-theory/blob/main/3%20-%20distortion-limited%20coding%20of%20sources/32%20-%20average%20mutual%20Information.md) | [平均互信息](https://github.com/timerring/information-theory/blob/main/3%20-%20distortion-limited%20coding%20of%20sources/32%20-%20average%20mutual%20Information.md#平均互信息)  \|  [平均互信息与各类熵的关系](https://github.com/timerring/information-theory/blob/main/3%20-%20distortion-limited%20coding%20of%20sources/32%20-%20average%20mutual%20Information.md#平均互信息与各类熵的关系)  \|  [维拉图](https://github.com/timerring/information-theory/blob/main/3%20-%20distortion-limited%20coding%20of%20sources/32%20-%20average%20mutual%20Information.md#维拉图)  \|  [条件熵](https://github.com/timerring/information-theory/blob/main/3%20-%20distortion-limited%20coding%20of%20sources/32%20-%20average%20mutual%20Information.md#条件熵)  \|  [平均互信息的性质](https://github.com/timerring/information-theory/blob/main/3%20-%20distortion-limited%20coding%20of%20sources/32%20-%20average%20mutual%20Information.md#平均互信息的性质) |
|                                      | [失真的概念和定义](https://github.com/timerring/information-theory/blob/main/3%20-%20distortion-limited%20coding%20of%20sources/33%20-%20concept%20and%20definition%20of%20distortion.md) | [信息率失真函数](https://github.com/timerring/information-theory/blob/main/3%20-%20distortion-limited%20coding%20of%20sources/33%20-%20concept%20and%20definition%20of%20distortion.md#信息率失真函数)  \|  [限失真信源编码的必要性](https://github.com/timerring/information-theory/blob/main/3%20-%20distortion-limited%20coding%20of%20sources/33%20-%20concept%20and%20definition%20of%20distortion.md#限失真信源编码的必要性)  \|  [失真度的定义](https://github.com/timerring/information-theory/blob/main/3%20-%20distortion-limited%20coding%20of%20sources/33%20-%20concept%20and%20definition%20of%20distortion.md#失真度的定义)  \|  [系统模型](https://github.com/timerring/information-theory/blob/main/3%20-%20distortion-limited%20coding%20of%20sources/33%20-%20concept%20and%20definition%20of%20distortion.md#系统模型) |
|                                      | [失真函数](https://github.com/timerring/information-theory/blob/main/3%20-%20distortion-limited%20coding%20of%20sources/34%20-%20distortion%20function.md) | [失真函数](https://github.com/timerring/information-theory/blob/main/3%20-%20distortion-limited%20coding%20of%20sources/34%20-%20distortion%20function.md#失真函数)  \|  [失真矩阵](https://github.com/timerring/information-theory/blob/main/3%20-%20distortion-limited%20coding%20of%20sources/34%20-%20distortion%20function.md#失真矩阵)  \|  [平均失真](https://github.com/timerring/information-theory/blob/main/3%20-%20distortion-limited%20coding%20of%20sources/34%20-%20distortion%20function.md#平均失真) |
|                                      | [信息率失真函数](https://github.com/timerring/information-theory/blob/main/3%20-%20distortion-limited%20coding%20of%20sources/35%20-%20information%20rate%20distortion%20function.md) | [信息率失真函数](https://github.com/timerring/information-theory/blob/main/3%20-%20distortion-limited%20coding%20of%20sources/35%20-%20information%20rate%20distortion%20function.md#信息率失真函数)  \|  [信道容量](https://github.com/timerring/information-theory/blob/main/3%20-%20distortion-limited%20coding%20of%20sources/35%20-%20information%20rate%20distortion%20function.md#信道容量)  \|  [平均互信息再讨论](https://github.com/timerring/information-theory/blob/main/3%20-%20distortion-limited%20coding%20of%20sources/35%20-%20information%20rate%20distortion%20function.md#平均互信息再讨论) |
|                                      | chapter focus                                                | 1. 解释互信息的概念及性质，计算两事件之间的互信息和集合之间的平均互信息;<br/>2. 解释限失真信源编码的概念;<br/>3. 说明信息率失真函数的物理含义; |
| 信息率失真函数与信源的限失真编码定理 | [R(D) 的定义域](https://github.com/timerring/information-theory/blob/main/4%20-%20information%20rate-distortion%20function%20and%20distortion-limited%20coding%20theorem%20of%20information%20source/41%20-%20the%20domain%20of%20R(D).md) | [连续信源的熵](https://github.com/timerring/information-theory/blob/main/4%20-%20information%20rate-distortion%20function%20and%20distortion-limited%20coding%20theorem%20of%20information%20source/41%20-%20the%20domain%20of%20R(D).md#连续信源的熵)  \|  [R(D) 的定义域](https://github.com/timerring/information-theory/blob/main/4%20-%20information%20rate-distortion%20function%20and%20distortion-limited%20coding%20theorem%20of%20information%20source/41%20-%20the%20domain%20of%20R(D).md#rd-的定义域) |
|                                      | [信息率失真函数的性质](https://github.com/timerring/information-theory/blob/main/4%20-%20information%20rate-distortion%20function%20and%20distortion-limited%20coding%20theorem%20of%20information%20source/42%20-%20properties%20of%20information%20rate%20distortion%20function.md) | [信息率失真函数的性质](https://github.com/timerring/information-theory/blob/main/4%20-%20information%20rate-distortion%20function%20and%20distortion-limited%20coding%20theorem%20of%20information%20source/42%20-%20properties%20of%20information%20rate%20distortion%20function.md#信息率失真函数的性质)  \|  [实现限失真信源编码的方式](https://github.com/timerring/information-theory/blob/main/4%20-%20information%20rate-distortion%20function%20and%20distortion-limited%20coding%20theorem%20of%20information%20source/42%20-%20properties%20of%20information%20rate%20distortion%20function.md#实现限失真信源编码的方式) |
|                                      | [离散信源 R(D)计算](https://github.com/timerring/information-theory/blob/main/4%20-%20information%20rate-distortion%20function%20and%20distortion-limited%20coding%20theorem%20of%20information%20source/43%20-%20discrete%20source%20R(D)%20calculation.md) | [离散信源 R(D)计算](https://github.com/timerring/information-theory/blob/main/4%20-%20information%20rate-distortion%20function%20and%20distortion-limited%20coding%20theorem%20of%20information%20source/43%20-%20discrete%20source%20R(D)%20calculation.md#离散信源-rd计算)  \|  [二元对称信源的 R(D) 函数](https://github.com/timerring/information-theory/blob/main/4%20-%20information%20rate-distortion%20function%20and%20distortion-limited%20coding%20theorem%20of%20information%20source/43%20-%20discrete%20source%20R(D)%20calculation.md#二元对称信源的--rd--函数)  \|  [高斯信源的 R(D)函数](https://github.com/timerring/information-theory/blob/main/4%20-%20information%20rate-distortion%20function%20and%20distortion-limited%20coding%20theorem%20of%20information%20source/43%20-%20discrete%20source%20R(D)%20calculation.md#高斯信源的-rd函数)  \|  [限失真信源编码定理](https://github.com/timerring/information-theory/blob/main/4%20-%20information%20rate-distortion%20function%20and%20distortion-limited%20coding%20theorem%20of%20information%20source/43%20-%20discrete%20source%20R(D)%20calculation.md#限失真信源编码定理) |
|                                      | chapter focus                                                | 1. 说明信息率失真函数的性质;<br/>2. 简单计算R(D)的定义域<br/>3. 运用二元对称信源与高斯信源的R(D)函数;<br/>4. 牢记并解释限失真信源编码定理 |

### ChangeLog

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