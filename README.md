## $\S 1.2,1.3\ \mathrm{Principle\ of\ Induction}$ 

<p align="center">INDUCTION</p>

Let $n\in\mathbb{N}$ (from 1) and $P(n)$ be a statement. Suppose that

1. $P(n_0)$ is true ( $n_0\in\mathbb{N}$ )
2. If $P(n_0)$ is true, then $P(n+1)$ is true

Then $P(n)$ is true for all $n\in\mathbb{N}, n\ge n_0$.

<p align="center">STRONG INDUCTION</p>

Let $n\in\mathbb{N}$ and $P(n)$ be a statement. Suppose that

1. $P(n_0)$ is true ( $n_0\in\mathbb{N}$ )
2. If $P(n_0), P(n_0+1), …, P(n)$ are true, then $P(n+1)$ is true

Then $P(n)$ is true for all $n\in\mathbb{N}, n\ge n_0$.

---

Example 1: Show that $n<2^n$ for all $n\in\mathbb{N}$

*Proof*:<br>
Let $n=1$, then $1<2^1=2$.<br>
Assume $n<2^n$, show $(n+1)<2^{n+1}$.<br>
Since $n<2^n$, $n+1<2^n+1<2^n+2^n=2^{n+1}$, it concludes that $n+1<2^{n+1}$. <br>
Therefore, by induction, we prove that $n<2^n$.


