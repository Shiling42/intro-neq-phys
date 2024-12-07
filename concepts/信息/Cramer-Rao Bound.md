---
date: 07-12-2024
---

我们考虑一个系统的概率取决于一个外部控制参数 $\theta$, 由此可以将概率分布写为 $p_\theta(x)\equiv p(x|\theta)$.

我们想通过这个概率分布测量出这个控制量 $\theta$, 我们假设有一个完美的观测量, $\hat{\theta}(x)$, 我们可以得出无偏的估计
$$
\theta = \langle \hat{\theta}\rangle
$$
有一个很直接的关系是
$$
\partial_\theta \theta = 1 \Rightarrow \int \hat{\theta}(x)\partial_\theta p_\theta(x) dx = 1
$$
现在我们希望可以把这个等式转化为correlation的形式, 可以有一点小技巧
$$
\begin{aligned}
	1 &= \int \hat{\theta}(x)\partial_\theta p_\theta(x)dx\\
	&=\int(\hat{\theta}(x)\partial_\theta\ln p_\theta(x) )p_\theta(x)dx\\
	&=\langle \hat{\theta}(x)\partial_\theta\ln p_\theta(x)\rangle
\end{aligned}
$$
这里 $\partial_\theta\ln p_\theta(x)=U(x)$ 就是我们的分数函数 (score function). 这里我们还可以再利用一个分数函数的性质
$$
\langle \partial_\theta\ln p_\theta(x)\rangle = 0
$$
那我们就可以把上面那个correlation的等式改写一下

$$
1 = \langle (\hat{\theta}(x)-\theta) U(x)\rangle
$$

然后用一下柯西不等式 (Cauchy–Schwarz inequality)

$$
1\leq \mathrm{Var}[\theta] \langle U(x)^2\rangle
$$
我们定义[[费希尔信息]] (Fisher information)

$$
I(\theta) =\langle U(x)^2\rangle= \int (\partial_\theta \ln p_\theta(x))^2 p_\theta(x) dx
$$
就可以得直接的Cramer-Rao Bound

$$
\boxed{\mathrm{Var}[\theta]\geq \frac{1}{I(\theta)}}
$$
也就是任何通过 $x$ 对 $\theta$ 进行的无偏估计的准确度都有一个下届, 由概率分布对这个控制参量的响应灵敏度所决定.

