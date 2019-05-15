<head>
    <script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript"></script>
    <script type="text/x-mathjax-config">
        MathJax.Hub.Config({
            tex2jax: {
            skipTags: ['script', 'noscript', 'style', 'textarea', 'pre'],
            inlineMath: [['$','$']]
            }
        });
    </script>
</head>

# 统计学基本知识梳理

## 二项分布

### 基本描述

二项分布（英语：Binomial distribution）是n个独立的是/非试验中成功的次数的离散概率分布，其中每次试验的成功概率为p。这样的单次成功/失败试验又称为伯努利试验。实际上，当n = 1时，二项分布就是伯努利分布。二项分布是显著性差异的二项试验的基础。

二项分布频繁地用于对以下描述的一种实验进行建模：从总数量大小为N的两个事物中进行n次放回抽样，以某一事物为基准，计算成功抽取这个事物的次数的概率。要注意的是必须进行的是放回抽样，对于不放回抽样我们一般用超几何分布来对这样的实验进行建模。

### 概率质量函数

　　　一般来说，如果一个随机变量X满足二项分布的话，那么它一定有一个参数n∈ ℕ且还有一个参数p∈ [0,1]。这样的话，我们可以把关于X的二项分布写成X ~ B(n, p)。对应的概率质量函数如下。

### 累积分布函数

$$
F(x;n,p) = \Pr(X \le x) = \sum_{i=0}^{\lfloor x \rfloor} {n\choose i}p^i(1-p)^{n-i}
$$

## 泊松分布

**Poisson分布**（法语：loi de Poisson，英语：Poisson distribution），译名有**泊松分布**、**普阿松分布**、**帕松分布**、**布瓦松分布**、**布阿松分布**、**波以松分布**、**卜氏分配**等，又称泊松小数法则（Poisson law of small numbers），是一种统计与概率学里常见到的离散概率分布

泊松分布适合于描述单位时间内随机事件发生的次数的概率分布。如某一服务设施在一定时间内受到的服务请求的次数，电话、交换机接到呼叫的次数、汽车站台的候客人数、机器出现的故障数、自然灾害发生的次数、DNA序列的变异数、放射性原子核的衰变数、激光的光子数分布等等。

泊松分布的概率质量函数为：
$$
P(X=k)=\frac{e^{-\lambda}\lambda^k}{k!}
$$


## 大数定律

### 示例

例如，抛掷一颗均匀的6面的骰子，1，2，3，4，5，6应等概率出现，所以每次扔出骰子后，出现点数的期望值是
$$
\frac{1+2+3+4+5+6}{6} = 3.5
$$


根据大数定理，如果多次抛掷骰子，随着抛掷次数的增加，平均值（样本平均值）应该接近3.5，根据大数定理，在多次伯努利实验中，实验概率最后收敛于理论推断的概率值，对于伯努利随机变量，理论推断的成功概率就是期望值，而若对n个相互独立的随机变量的平均值，频率越多则相对越精准。

例如硬币投掷即伯努利实验，当投掷一枚均匀的硬币，理论上得出的正面向上的概率应是1/2。因此，根据大数定理，正面朝上的比例在相对“大”的数字下，“理应”接近为1/2，尤其是正面朝上的概率在n次实验（n接近无限大时）后应几近收敛到1/2。

即使正面朝上（或背面朝上）的比例接近1/2，几乎很自然的正面与负面朝上的绝对差值（absolute difference差值范围）应该相应随着抛掷次数的增加而增加。换句话说，绝对差值的概率应该是会随着抛掷次数而接近于0。直观的来看，绝对差值的期望会增加，只是慢于抛掷次数增加的速度。

### 表现形式

大数定律主要有两种表现形式：'''弱大数定律'''和'''强大数定律'''。定律的两种形式都肯定无疑地表明，样本均值
$$
\overline{X}_n=\frac1n(X_1+\cdots+X_n)
$$
收敛于真值
$$
\overline{X}_n \to \mu \quad\textrm{as}\quad n \to \infty
$$
其中 $X_1$,$X_2$, ... 是独立同分布、期望值$\operatorname{E}(X_1)=\operatorname{E}(X_2)=\,\cdots\,=\mu$ 且皆[[勒贝格可积]]的随机变量构成的无穷序列。$X_j$的勒贝格可积性意味着期望值 $\operatorname{E}(X_j)$存在且有限。

#### 方差

$\operatorname{Var}(X_1)=\operatorname{Var}(X_2)=\,\cdots\,= \sigma^2 <\infty$有限的假设是''非必要''的。很大或者无穷大的方差会使其收敛得緩慢一些，但大数定律仍然成立。通常采用这个假设来使证明更加简洁。

### 弱大数定律

'''弱大数定律'''也称为辛钦定理，陈述为：样本均值依概率收敛于期望值。
$$
\overline{X}_n\ \xrightarrow{P}\ \mu \quad\textrm{as}\quad n \to \infty
$$
也就是说对于任意正数 ε,
$$
\lim_{n\to\infty}P\left(\,|\overline{X}_n-\mu| > \varepsilon\,\right) = 0
$$
即
$$
<math>P\left( \lim_{n\to\infty}\overline{X}_n=\mu\right) = 1<\math>
$$

### 切比雪夫定理的特殊情况

设$a_1,\ a_2,\ \dots\ ,\ a_n,\ \dots$ 为相互独立的随机变量，
数学期望：$ \operatorname{E}(a_i) = \mu \quad (i = 1,\ 2,\ \dots) $
方差：$ \operatorname{Var}(a_i) = \sigma^2 \quad (i=1,\ 2,\ \dots)$

则序列$\overline{a}= \frac{1}{n} \sum_{i=1}^n a_i$[[依概率收敛]]于$\mu$（即收敛于此数列的数学期望$E(a_i)$）。

换言之，在定理条件下，当$n$无限变大时，$n$个随机变量的[[算术平均]]将变成一个常数。

### 伯努利大数定律

设在$n$次独立重复伯努利试验中，
事件$X$发生的次数为$ n_x$。
事件$X$在每次试验中发生的母體機率为$p$。
$ \frac{n_x}{n}$代表样本发生事件$X$的频率。

大数定律可用概率极限值定义:
则对任意正数$\varepsilon >0 $，下式成立：
$ \lim_{n \to \infty}{P{\left\{ \left|\frac{n_x}{n} - p \right| < \varepsilon \right\}}} = 1 $

定理表明事件发生的频率依概率收敛于事件的总体概率。
定理以严格的数学形式表达了频率的稳定性。
就是说当$n$很大时，事件发生的频率于总体概率率有较大偏差的可能性很小。



## 正态分布

''正态分布''又名“高斯分布''，是一個非常常見的概率分布。正态分布在上十分重要，

若随机变量$X$服從一個位置參數為$\mu$、尺度參數為$\sigma$的正态分布，记为：
$ X \sim N(\mu,\sigma^2) $
則其機率密度函數為
$ f(x) = {1 \over \sigma\sqrt{2\pi} }\,e^{- {{(x-\mu )^2 \over 2\sigma^2}}} $

常態分布的[[數學期望]]值或[[期望值]]$\mu$等於位置參數，決定了分布的位置；其[[方差]]$\sigma^2$的開平方或[[標準差]]$\sigma$等於尺度參數，決定了分布的幅度。

常態分布的機率密度函數曲線呈鐘形，因此人們又經常稱之為'''鐘形曲線'''（类似于寺庙里的大钟，因此得名）。我們通常所說的'''標準常態分布'''是位置參數$\mu = 0$，尺度參數$\sigma^2 = 1$的正态分布。

## 置信区间

在统计学中，一个概率样本的**置信区间**（英语：Confidence interval，CI），是对产生这个样本的总体的参数分布（Parametric Distribution）中的某一个未知参数值，以区间形式给出的估计。相对于点估计（Point Estimation）用一个样本统计量来估计参数值，置信区间还蕴含了估计的精确度的信息。在现代机器学习中越来越常用的置信集合（Confidence Set）概念是置信区间在多维分析的推广[1]。

置信区间在频率学派中间使用，其在贝叶斯统计中的对应概念是可信区间（Credible Interval）。两者建立在不同的概念基础上的，贝叶斯统计将分布的位置参数视为随机变量，并对给定观测到的数据之后未知参数的后验分布进行描述，故无论对随机样本还是已观测数据，构造出来的可信区间，其可信水平都是一个合法的概率[2]；而置信区间的置信水平，只在考虑随机样本时可以被理解为一个概率。

### 定义

;对随机样本的定义
定义置信区间最清晰的方式是从一个'''随机样本'''出发。考虑一个一维随机变量<math>{\cal X}</math>服从分布<math>{\cal F}</math>，又假设<math>\theta</math>是<math>{\cal F}</math>的参数之一。假设我们的数据采集计划将要独立地抽样<math>n</math>次，得到一个随机样本<math>\{X_1,\ldots,X_n\}</math>，注意这里所有的<math>X_i</math>都是随机的，我们是在讨论一个尚未被观测的数据集。如果存在'''统计量'''(统计量定义为样本<math>X=\{X_1,\ldots,X_n\}</math>的一个函数，且不得依赖于任何未知参数)<math>u(X_1,\ldots,X_n),v(X_1,\ldots,X_n)</math>满足<math>u(X_1,\ldots,X_n)<v(X_1,\ldots,X_n)</math>使得：

: <math>\mathbb{P}\left(\theta\in\left(u(X_1,\ldots,X_n),v(X_1,\ldots,X_n)\right)\right)=1-\alpha</math>

则称<math>\left(u(X_1,\ldots,X_n),v(X_1,\ldots,X_n)\right)</math>为一个用于估计参数<math>\theta</math>的<math>1-\alpha</math>置信区间，其中的<math>1-\alpha</math>称为'''置信水平'''。

;对观测到的数据的定义
接续随机样本版本的定义，现在，对于随机变量<math>{\cal X}</math>的一个已经观测到的样本<math>\{x_1,\ldots,x_n\}</math>，注意这里用小写x表记的<math>x_i</math>都是已经观测到的数字，没有随机性了，定义基于数据的<math>1-\alpha</math>置信区间为：

: <math>\left(u(x_1,\ldots,x_n),v(x_1,\ldots,x_n)\right)</math>

注意，置信区间可以是单边或者双边的，单边的置信区间中设定<math>u=-\infty</math>或者<math>v=+\infty</math>，具体前者还是后者取决于所构造的置信区间的方向。

初学者常犯一个概念性错误，是将基于观测到的数据所同样构造的置信区间的置信水平，误认为是它包含真实未知参数的真实值的概率。正确的理解是：置信水平只有在描述这个同样构造置信区间的'''过程'''(或称'''方法''')的意义下才能被视为一个概率。一个基于已经观测到的数据所构造出来的置信区间，其两个端点已经不再具有随机性，因此，类似的构造的间隔将会包含真正的值的比例在所有值中，其包含未知参数的真实值的概率是'''0或者1'''，但我们'''不能知道'''是前者还是后者<ref>{{cite book |author1=Moore, D |author2=McCabe, George P |author3=Craig, B |title=Introduction to the Practice of Statistics |date=2012 |publisher=San Francisco, CA: Freeman}}</ref>。

### 例子

; 例1：正态分布，'''已知'''总体方差<math>\sigma^2</math>
<math>1-\alpha</math>水平的正态置信区间为：
: <math>\left( \bar{x}-z_{1-\alpha/2}\frac{\sigma}{\sqrt{n}}, \bar{x}+z_{1-\alpha/2}\frac{\sigma}{\sqrt{n}} \right)</math>  (双边)
: <math>\left( -\infty, \bar{x}+z_{1-\alpha}\frac{\sigma}{\sqrt{n}} \right)</math>  (单边)
: <math>\left( \bar{x}-z_{1-\alpha}\frac{\sigma}{\sqrt{n}}, +\infty \right)</math>  (单边)

以下为方便起见，只列出'''双边'''置信区间的例子，且区间中用"<math>\pm</math>"进行简记：

; 例2：正态分布，'''未知'''总体方差<math>\sigma^2</math>
<math>1-\alpha</math>水平的'''双边'''正态置信区间为：
: <math>\left( \bar{x}\pm t_{n-1;\alpha/2}\frac{s}{\sqrt{n}} \right)</math>

; 例3：两个独立正态样本<math>x</math>和<math>y</math>，样本大小为<math>m</math>和<math>n</math>，估计总体均值之差<math>\mu_1-\mu_2</math>，假设总体方差'''未知但相等：<math>\sigma_1=\sigma_2</math>'''(如果未知且不等就要应用{{tsl|en|Welch's t-test|Welch公式}}来确定t分布的自由度)
<math>1-\alpha</math>水平的'''双边'''正态置信区间为：
: <math>\left( \bar{x}-\bar{y}\pm t_{m+n-2;\alpha/2}\cdot s_p\cdot \sqrt{\frac1m+\frac1n} \right)</math>，其中<math>s_p=\sqrt{\frac{(m-1)s_x^2+(n-1)s_y^2}{m+n-2}}</math>且<math>s_x,s_y</math>分别表示<math>x</math>和<math>y</math>的样本标准差。

### 构造法
一般来说，置信区间的构造需要先找到一个'''枢轴变量'''（{{Lang|en|Pivotal quantity}}，或称{{Lang|en|Pivot}}），其表达式依赖于样本以及带估计的未知参数(但'''不能'''依赖于总体的其它未知参数)，其分布'''不依赖于'''任何未知参数。

下面以上述例2为例，说明如何利用枢轴变量构造置信区间。对于一个正态分布的随机样本<math>{X_1,\ldots,X_n}</math>，可以证明(此证明对初学者并不容易)如下统计量'''互相独立'''：
: <math>\bar{X}=\frac1n \sum_{i=1}^n X_i </math>  和   <math>S^2=\frac{\sum_{i=1}^n\left(X_i-\bar{X}\right)^2}{n-1}</math>
它们的分布是：
: <math>\frac{\bar{X}-\mu}{\sigma}\sim N(0,1)</math>  和  <math>(n-1)\frac{S^2}{\sigma^2} \sim \chi^2_{n-1}</math>
所以根据[[t分布]]的定义，有
:<math>t = \frac{\bar{X}-\mu}{S/\sqrt{n}}\sim t_{n-1}</math>
于是反解如下等式左边括号中的不等式
:<math>\mathbb{P}\left( -t_{n-1;\alpha/2}<t=\frac{\bar{X}-\mu}{S\sqrt{n}}<t_{n-1;\alpha/2} \right)=1-\alpha</math>
就得到了例2中双边置信区间的表达式。

### 与参数检验的联系
有时，置信区间可以用来进行参数检验。例如在上面的例1中构造的'''双边'''<math>1-\alpha</math>水平置信区间，可以用来检验具有相应的'''显著水平为<math>\alpha</math>'''的'''双边'''对立假设，具体地说是如下检验：
正态分布总体，知道总体方差<math>\sigma^2</math>，'''在<math>\alpha</math>显著水平下'''检验：
: <math>H_0: \mu=\mu_0</math> vs <math>H_1: \mu \neq\mu_0</math>
检验方法是：当且仅当相应的<math>1-\alpha</math>水平置信区间不包含<math>\mu_0</math>时拒绝零假设<math>H_0</math>

例1中构造的'''双边'''<math>1-\alpha</math>水平置信区间也可以用来检验如下两个显著水平为'''<math>\alpha/2</math>'''的'''单边'''对立假设：
: <math>H_0: \mu\leq \mu_0</math> vs <math>H_1: \mu >\mu_0</math>
和
: <math>H_0: \mu\geq \mu_0</math> vs <math>H_1: \mu <\mu_0</math>
检验方法是完全类似的，比如对于上述第一个单边检验<math>H_1: \mu >\mu_0</math>，当且仅当双边置信区间的左端点大于<math>\mu_0</math>时拒绝零假设。

