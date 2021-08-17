---
title: 昂萨格倒异关系 Onsager reciprocal relations
date: 2021-05-21
---

# 昂萨格倒异关系

> 参考：https://www.weizmann.ac.il/complex/mukamel/sites/complex.mukamel/files/uploads/2013-onsager_reciprocity.pdf
## 基本简介
昂萨格倒异关系是描述近平衡态下的各种流之间的耦合关系，其本质是在近平衡态保持了一阶项，所以是线性响应理论的结果。

昂萨格关系的起源来自于近平衡态统计物理加上可逆过程的假设。

我们可以先写出化学势

$$
dU = TdS-PdV+\mu dM
$$


## 外界的驱动

这里我们考虑一个温度梯度的驱动。来自热传导的能量流动我们可以用傅里叶形式写出

$$
J_u = -k\nabla T=kT^2\nabla\frac{1}{T}
$$

如果这里还有一个质量流(mass transport), 其菲克扩散流写作

$$
J_\rho = -D\nabla \rho
$$

接下来使我们要引入物理假设的地方在。这里我们用到一个已接近似，认为化学势能正比于密度，那么我们就有了

$$
J_\rho = -D'\nabla (-\mu/T)
$$

## 从热力学开始

其实我们不是以具体过程开始，而是抽象的认为一个驱动力能导致在其他物理空间的流，那么我们可以写出一个最广义的经验公式

$$
\dot{x_i}=-\sum_j \lambda_{ij}x_j
$$

这里物理量$x_i$的时间演化和其他的宏观量均有耦合。这个耦合有什么关系呢？考虑到这个耦合由一个等效的力所导致的，那么这个力便是

$$
F_i \equiv - \partial_{x_i}G
$$

这里的$S$是自由能，但是我们也可以理解为一个“势能”。在平衡态，熵是一个极大值，在近平衡态我们展开这个熵便会有

$$
G=G_0 + \sum_{j,k}\beta_{jk}x_jx_k
$$

那这样这个“回复力”就好理解了，

$$
F_i = -\sum_j\beta_{ij}x_i
$$

我们认为这个回复力导致了$x_i$的时间演化，而这个时间演化是没有“惯性的”，于是要联系起来这些内容我们需要定义一个“耗散力”矩阵$\gamma$.

考虑到$\dot x = -\lambda x$,我们可以定义一个$\gamma$矩阵使得$\gamma^{-1}\beta=\lambda$, 那便有了

$$
\dot{\mathbf{x}} = \gamma^{-1}\mathbf{F}
$$

这里把$\gamma$写出来就是

$$
\gamma  =\beta \lambda^{-1}
$$

接下来我们想要发现的是这$\lambda$矩阵的结构性质，这里的结构性质来源于一个可逆过程的假设。

$$
\begin{aligned}
\langle F_ix_j\rangle
&=-\int d\mathbf{x}\  e^{-G[\mathbf{x}]}\partial_{x_i}G[\mathbf{x}]  x_j\\
&=\int d\mathbf{x}\  \partial_{x_i}e^{-G[\mathbf{x}]}x_j\\
&=\int d\mathbf{x}\  \partial_{x_i}(e^{-G[\mathbf{x}]}x_j)-\int d\mathbf{x}\ e^{-G[\mathbf{x}]} \partial_{x_i}x_j\\
&=-\delta_{ij}
\end{aligned}
$$

使用上面这个式子我们还可以发现

$$
\langle F_i F_j\rangle =\langle F_i\beta \mathbf{x}\rangle =\beta_{ij}
$$

$$
\langle x_i x_j\rangle = \left\langle x_i\beta^{-1}\mathbf{F}\right\rangle =(\beta^{-1})_{ij}
$$

根据这个我们有了力的对称性$\beta_{ij}=\beta_{ji}$, 接下来我们需要理解耗散系数$\gamma$的对称性，这个对称性的来源是时间可逆性

$$
\langle x_i(t+\tau)x_j(t)\rangle = \langle x_i(t-\tau)x_j(t)\rangle =\langle x_i(t)x_j(t+\tau)\rangle 
$$

这个时间可逆性给了我如下关系

$$
\langle \dot{x}_i(t)x_j(t)\rangle = \langle x_i(t)\dot{x}_j(t)\rangle 
$$

注意到

$$
\langle \dot{x}_i(t)x_j(t)\rangle =\langle \gamma_{ik}F_k(t)x_j(t)\rangle =\gamma_{ik}
$$


于是我们得到了耗散系数之间的对易关系

$$
\gamma_{ij}=\gamma_{ji}
$$

总结一下，昂萨格倒异关系告诉了我们，一对物理量对于微扰的相互影响是相同的。为什么会有这个相互响应呢？你把东西从平衡态拉开，各个量之间不是正交（相互独立）的话，就会有相互的影响。


## 对于一个稳态的流

接下来我们不考虑时间的一个稳态的流

假设我们有一个温度梯度，那么

$$
\dot{P_i}=\partial_{T_i} G
$$