- [BCH码-循环码](#bch码-循环码)
- [RS码](#rs码)
- [总结](#总结)


## BCH码-循环码

特点: 它的生成多项式  g(x)  与最小码距之间有密切 的关系, 可以根据所要求的纠错能力  t , 很容易地构 造出 BCH码。

如果循环码的生成多项式具有如下形式:
$$
g(x)=\mathrm{LCM}\left[m_{1}(x), m_{2}(x), \ldots, m_{2 t-1}(x)\right]
$$
其中  t  为纠错个数,  $m_{i}(x) $ 既约 (素) 多项式,  $\mathrm{LCM}$  表示取最小公倍数, 则由此生成的循环码为  $\mathbf{B C H}$  码。码距  $\boldsymbol{d} \geq 2 \boldsymbol{t}+\mathbf{1}$ 。每个码字能纠  $\mathrm{t}$  个随机独立差错。

若  $\mathbf{B C H}$  码的码长  $n=2^{m}-1$ , 其中  $m \geq 3$, $t<\frac{m}{2}$, $n-k \leq m t$ , 则为本原  $\mathbf{B C H}$  码;

若  $\mathbf{B C H}$  码的码长是  $n=2^{m}-1$  的因子, 则为非本原  $\mathbf{B C H}$  码。

相关知识: 

**本原多项式的定义**: 一个  n  次的多项式  f(x) 

(1)  f(x)  为既约多项式 (不可因式分解) -GF（2）;

(2)  f(x)  是  $\left(x^{p+1}\right)$  因子, $ p^{2}=2^{n}-1$ 

(3)  f(x)  不是 $ \left(x^{q+1}\right)$  的因子, $ p>q$ 

 $\mathrm{BCH}$  码的编码: 生成多项式查表。

 $\mathrm{BCH}$  码的译码: 

 $\mathbf{B C H}$  的译码主要采用彼得森译码, 思路如下:

- 用生成多项式  g(x)  的各因式作为除式, 对接收到的码多项式求余, 得到  t  个余式, 称为部分伴随式;
- 用  t  个部分伴随式构造一个特定的译码多项式, 它以错误位置数为根;
- 求译码多项式的根, 得到错误位置;
- 纠正错误位置。



## RS码

q  进制  $\mathrm{BCH}$  码的一个特殊子类  (n=q-1) , 并且具有很强的纠错能力。

$\mathrm{RS}$  码的参数：码长  n=q-1 , 监督位数目  r=2t , 其中  t  是 能够纠正的错码数目, 最小码距  $\boldsymbol{d}=\mathbf{2 t}+\mathbf{1}$ ; 其生成多项式为
$$
g(x)=(x+\alpha)\left(x+\alpha^{2}\right) \ldots\left(x+\alpha^{2 t}\right)
$$
式中,  $\alpha^{i}$  为伽罗华域  $\mathbf{G F}\left(\alpha^{m}\right)$  中的一个元素。

RS码的主要优点:

+ 它是多进制纠错编码，所以特别适合用于多进制调制的场合;
+ 它能够纠正t个q位二进制错码，即能够纠正不超过q个连续的二进制错码，所以适合在衰落信道中纠正突发性错码。

## 总结

+ 循环码基本概念;
+ 循环码的生成多项式，以及用该多项式编译码
+ 由生成多项式构造系统型生成矩阵和监督矩阵
+ 循环码的编译码电路;
+ BCH、RS码。





参考文献：

1. Proakis, John G., et al. *Communication systems engineering*. Vol. 2. New Jersey: Prentice Hall, 1994.
2. Proakis, John G., et al. *SOLUTIONS MANUAL Communication Systems Engineering*. Vol. 2. New Jersey: Prentice Hall, 1994.
3. 周炯槃. 通信原理（第3版）[M\]. 北京：北京邮电大学出版社, 2008.
4. 樊昌信, 曹丽娜. 通信原理（第7版） [M\]. 北京：国防工业出版社, 2012.



[返回首页](https://github.com/timerring/information-theory)