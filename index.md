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

**Poisson分布**（法语：loi de Poisson，英语：Poisson distribution），译名有**泊松分布**、**普阿松分布**、**帕松分布**、**布瓦松分布**、**布阿松分布**、**波以松分布**、**卜氏分配**等，又称泊松小数法则（Poisson law of small numbers），是一种[统计](https://zh.wikipedia.org/wiki/統計)与[概率](https://zh.wikipedia.org/wiki/概率)学里常见到的[离散概率分布](https://zh.wikipedia.org/wiki/機率分佈)，由[法国](https://zh.wikipedia.org/wiki/法國)[数学家](https://zh.wikipedia.org/wiki/數學家)[西莫恩·德尼·泊松](https://zh.wikipedia.org/wiki/西莫恩·丹尼·泊松)（Siméon-Denis Poisson）在1838年时发表。

泊松分布适合于描述单位时间内随机事件发生的次数的概率分布。如某一服务设施在一定时间内受到的服务请求的次数，[电话](https://zh.wikipedia.org/wiki/电话)[交换机](https://zh.wikipedia.org/wiki/交换机)接到呼叫的次数、汽车站台的候客人数、机器出现的故障数、[自然灾害](https://zh.wikipedia.org/wiki/自然灾害)发生的次数、DNA序列的变异数、放射性原子核的衰变数、[激光](https://zh.wikipedia.org/wiki/雷射)的光子数分布等等。

泊松分布的[概率质量函数](https://zh.wikipedia.org/wiki/概率质量函数)为：
$$
P(X=k)=\frac{e^{-\lambda}\lambda^k}{k!}
$$



