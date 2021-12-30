---
layout: default
title: High Dimensional Statistics
---



# High Dimensional Statistics

## Sub-Gaussian distribution

##### Def 1

A random variable $$X$$ with mean $$\mu=\mathbb{E}[X]$$ is $$\sigma$$-sub-Gaussian if 
$$
\mathbb{E}\left[e^{\lambda(X-\mu)}\right] \leq e^{\sigma^{2} \lambda^{2} / 2}
$$
for  $$\forall \lambda \in \mathbb{R}$$.

This is some theorem for high dimensional statistics.

$$
\mathbb{P}\left\{\sum_{i=1}^{N}\left(X_{i}-\mathbb{E} X_{i}\right) \geq t\right\} \leq \exp \left(-\frac{2 t^{2}}{\sum_{i=1}^{N}\left(M_{i}-m_{i}\right)^{2}}\right)
$$

##### Def 2
Another definition is introduced in Vershyin's book. It introduced sub-Gaussian norm and along side equivalent definitions.

A random variable $X$ satisfies any one of above properties is called ub- Gaussian random variable, the sub-Gaussian norm, denoted $$\|X\|_{\psi_{2}}$$ is:
$$
\|X\|_{\psi_{2}}=\inf \left\{t>0: \mathbb{E} \exp \left(X^{2} / t^{2}\right) \leq 2\right\}
$$

1. $$\mathbb{P}\{X \geq t\} \leq  \exp \left(-ct^{2} / \|X\|_{\psi_{2}}^{2}\right) \quad \text { for all } t \geq 0$$.
2. $$\|X\|_{L^{p}}=(\mathbb{E}| X |^{p})^{1 / p}$$ $$ \leq C \|X\|_{\psi_{2}} \sqrt{p} \quad \text { for all } p \geq 1$$.
3. $$\mathbb{E} \exp \left(\lambda^{2} X^{2}\right) \leq \exp \left(C \|X\|_{\psi_{2}}^{2} \lambda^{2}\right) \quad \text { for all } \lambda \text { such that }|\lambda| \leq \frac{1}{C\|X\|_{\psi_{2}}}$$.
4. The MGF of $$X^2$$ is bounded at some point (def of sub-Gaussian norm):$$\mathbb{E} \exp \left(X^{2} / \|X\|_{\psi_{2}}^{2}\right) \leq 2$$.
5. Moreover, if $$\mathbb{E} X=0$$, we have: $$
    \mathbb{E} \exp (\lambda X) \leq \exp \left(C\|X\|_{\psi_{2}}^{2} \lambda^{2}\right) \quad \text { for all } \lambda \in \mathbb{R}
    $$


