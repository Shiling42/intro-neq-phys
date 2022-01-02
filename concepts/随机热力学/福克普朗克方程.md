# Fokker-Planck 方程

## 从牛顿方程到Langevin方程

牛顿方程是经典物理下最直观的方程，其描述了一个物体在力的作用下的运动。
$$
m\dot{v}=F
$$
在我们现实中接触的大部分场景来并不涉及接近光速的物理或者明显的量子效应，牛顿方程都可以视为最底层的理论。所以我们关心的东西便是如何找到这个力。不准求严谨性的来说，我们考虑水中悬浮的一个胶体颗粒，比如说一个花粉，其比周围的水分子大很多，于是会受到各个方向的水分子不断地碰撞。这些周围水分子不断碰撞的力我们只能用一个噪音项$\eta(t)$去刻画，那么这个花粉粒子的牛顿方程就写作

$$
m\dot v= \eta(t)
$$

这个噪音项由于是来自周围水分子的不断碰撞，而这个溶液环境是均匀的，那么这些碰撞平均值应该为零，于是有了$\langle \eta(t)\rangle=0$, 这里我们用$\langle \rangle$表示求平均。

## 从单个粒子到概率分布
广义的来说Fokker-Planck方程是随机微分方程（Stochastic differential equation）的积分形式。首先直接给出 Fokker-Planck 方程的形式

$$
\frac{\partial f(x,t)}{\partial t}=-\frac{\partial }{\partial x}(a(x,t)f(x,t)) + \frac{\partial^2}{\partial x^2}(b(x,t)f(x,t))
$$

这里的$f(x,t)$ 是一个概率分布，$a(x,t)$ 我们一般称为拖拽项(drag term)，$b(x,t)$一般称为扩散项(diffusion term)。