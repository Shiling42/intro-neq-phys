# Entropy Production, Information and Non-Equilibrium Free Energy

## Entropy production[^1]

For a thermodynamic consistent system described master equations
$$
\frac{dp_i}{dt} = \sum_{j}(k_{ij}p_j-k_{ji}p_i).
$$
One can show that the entropy production rate of the system has the form of
$$
\dot{S} = \frac{1}{2}\sum_{i,j}(k_{ij} p _j-k_{ji}p_i)\ln\left[\frac{k_{ij}p_j}{k_{ji}p_i}\right].
$$
And it can be decomposed into two terms
$$
\begin{aligned}
\dot{S}=
\underbrace{\frac{1}{2}\sum_{i,j}(k_{ij} p _j-k_{ji})\ln\left[\frac{k_{ij}}{k_{ji}}\right]}_{\dot{S}_{env}}\\
+\underbrace{\frac{1}{2}\sum_{i,j}(k_{ij} p _j-k_{ji}p_i)\ln\left[\frac{p_j}{p_i}\right]}_{\dot{S}_{sys}}.
\end{aligned}
$$
a) **To show the thermodynamic nature of the two entropy production terms**:
$$
\dot{S}_{sys} = \frac{d}{dt}(S_{sys}),\\
\dot{S}_{env} = \sum_i\dot{Q}_i/T_i.
$$
b) **What happen when system reach stationary state ($dp_i/dt=0$)? Discuss  both of equilibrium and non-equilibrium cases.**

## Information and entropy production[^2]

Now we define the Kullback-Leibler distance 
$$
D_{KL}(P||Q) = \sum_{p_i}p_i\ln\left[\frac{p_i}{q_i}\right],
$$
this distance characterizes the distance of a distribution $P$ to the reference distribution $Q$. For a system that can reach thermodynamic equilibrium, we can use $Q=P^{eq}=\{\pi_i^{eq}\}$ as the reference state. 

a) **Show that the entropy production rate is the negative of the time derivative of K-L distance** (Hint: the dynamics of the system is described by thermodynamically consistent master equations).
$$
\dot{S}(t)=-\frac{d}{dt}D_{KL}(P(t)||P^{eq})
$$
b) **Show that, when the system start from an arbitrary initial distribution $P(0)=\{p_i(0)\}$, the K-L divergence, $D_{KL}(P||\pi_i^{eq})$,  is an monotonically decreasing function of time.** 

c) **Try to interpret the above result in terms of information - understand the K-L distance as a measure of information**



## Non-equilibrium free energy [^3][^4]

For an out-of-equilibrium distribution $P=\{p_i\}$, we can define generalized free energy, or called non-equilibrium free energy
$$
\mathcal{F} = \langle E\rangle_P-k_BTS(P),
$$
where $\langle E\rangle_{P}=\sum_i E_ip_i$ and $S(P) = -\sum_i p_i\ln p_i$.  When system is at equilibrium the above definition reduced back to the equilibrium free energy we are familiar with. $\mathcal{F}(P^{eq})=F_{eq}=\langle E\rangle_{eq}-k_BTS$. 

a) **Show that the Kullback-Leibler distance equals to the excess of non-equilibrium free energy**
$$
\Delta \mathcal{F} = \mathcal{F}(P)-\mathcal{F}(P^{eq})=D_{KL}(P||P^{eq}).
$$
b) **Show that the maximal work can be extracted from a non-equilibrium distribution $P$ is bounded by the non-equilibrium free energy difference:**
$$
W_{extrat} \leq  \Delta\mathcal{F}.
$$

**Ref.**

[^1]: Schnakenberg, J., 1976. Network theory of microscopic and macroscopic behavior of master equation systems. *Reviews of Modern physics*, *48*(4), p.571.

[^2]: Horowitz, J.M., Zhou, K. and England, J.L., 2017. Minimum energetic cost to maintain a target nonequilibrium state. *Physical Review E*, *95*(4), p.042102.

[^3]: Parrondo, J.M., Horowitz, J.M. and Sagawa, T., 2015. Thermodynamics of information. *Nature physics*, *11*(2), pp.131-139.
[^4]: Esposito, M. and Van den Broeck, C., 2011. Second law and Landauer principle far from equilibrium. *EPL (Europhysics Letters)*, *95*(4), p.40004.