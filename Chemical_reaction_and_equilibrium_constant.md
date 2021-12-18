首先我们假设一个比较一般性的化学反应表达
$$
\sum _i \nu_{S_i} S_i \leftrightharpoons \sum_j \nu_{P_j}P_j
$$
这里用$S_i$​​表示反应物，$\nu_{S_i}$​​表示是化学计量数。对产物$\{P_j\}$​​​ 们同理。

举个例子，对于反应$2A+B\leftrightharpoons C$​ 的反应，我们便有
$$
s_1 = 2\quad S_1 = A,\\ s_2 = 1\quad S_2=B,\\p_1 = 1\quad P_1 = C
$$
如果这个系统是封闭的，那么这个的平衡态是对应最小自由能的态，这里的自由能有两个部分，能量的部分和熵的部分
$$
G = E-ST
$$
这里的能量是系统里面所有化学物质的能量之和
$$
E = \sum_i\mu_{S_i}N_{S_i}+\sum_j\mu_{P_j}N_{P_j}
$$
这里$\mu_{S_i}$表示的是反应物$S_i$的化学势能，也就是这重物质本身所具有的能量。$N_{S_i}$则表示这种反应物的浓度。对生成物们同理。

而熵的部分度量了系统的自由度，可以表示为
$$
S = \sum_jk_B N_{S_i}\mathrm{ln} \frac{N_{S_i}}{V}+\sum_jk_B\mathrm{ln} \frac{N_{P_j}}{V}
$$
那么整体的话这个系统的自由能就是
$$
G=\sum_i\left(\mu_{S_i}N_{S_i}- k_BT\mathrm{ln} N_{S_i}\right)+\sum_j\left(\mu_{P_j}N_{P_j}-k_BT\mathrm{ln} N_{P_j}\right)
$$
为了找到平衡态，我们要去最小化这个自由能。注意到这是一个封闭系统，这个化学反应 $\sum _i\nu_{S_i} S_i \leftrightharpoons \sum_j \nu_{P_j}P_j$​​​ 反映了一个偶尔动力学，让这个反应进行 $\delta$​​ 的量，反应物和生成物的改变是
$$
\Delta N_{P_j}=N_{P_j}-N_{P_j}' = \nu_{p_j}\xi\\
\Delta N_{S_i} = N_{S_j}-N_{S_j}' = -\nu_{s_i}\xi
$$
用这个东西我们能便能得到自由能对化学反应的响应
$$
\begin{aligned}
0=\frac{\partial G}{\partial \xi} 
&=\sum_i\left(-\nu_{S_i}\mu_{S_i}-\nu_{S_i} \frac{k_BT}{V}-\nu_{S_i}k_BT\ln \frac{N_{S_i}}{V}\right)-\sum_j\left(\nu_{P_j}\mu_{P_j}+\nu_{P_j}\frac{k_BT}{V}-\nu_{P_j}k_BT\ln \frac{N_{P_j}}{V}\right)\\
&=\underbrace{\left(\sum_j \left(\nu_{P_j}\mu_{P_j}-\frac{\nu_{S_i}k_BT}{V}\right)-\sum_i\left(\nu_{S_i}\mu_{S_i}-\frac{\nu_{P_j}k_BT}{V}\right)\right)}_{\Delta G_{\Theta}}-k_BT\ln\frac{\prod_i[S_i]^{\nu_{S_i}}}{\prod_j[P_j]^{\nu_{P_j}}}
\end{aligned}
$$
所以最后我们总结出一个化学反应常数：
$$
K_{eq} = \frac{\prod_i[S_i]^{\nu_{S_i}}}{\prod_j[P_j]^{\nu_{P_j}}}=e^{-\Delta G_\Theta/k_BT}
$$
