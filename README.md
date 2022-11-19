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

**Example 1**: Show that $n<2^n$ for all $n\in\mathbb{N}$

*Proof*:<br>
Let $n=1$, then $1<2^1=2$.<br>
Assume $n<2^n$, show $(n+1)<2^{n+1}$.<br>
Since $n<2^n$, $n+1<2^n+1<2^n+2^n=2^{n+1}$, it concludes that $n+1<2^{n+1}$. <br>
Therefore, by induction, we prove that $n<2^n$.

**Example 2**: Let $(a_n)\_{n\in\mathbb{N}}$ be a sequence, satisfying $a_1=2, a_2=8$, and $a_n=4(a_{n-1}-a_{n-2}), n\ge 3$. Show that $a_n=n\cdot2^n$

*Proof*:<br>
Let $n=1$, then $a_1=2=1\cdot2^1$<br>
&ensp;&ensp;&ensp; $n=2$, then $a_2=8=2\cdot2^2$<br>
Assume $a_j=j\cdot2^j$ for all $1\le j\le k$. Show that $a_{k+1}=(k+1)\cdot2^{k+1}$<br>
Since $a_{k+1}=4(a_k-a_{k-1})$, by strong induction, $a_{k+1}=4(k2^k-(k-1)2^{k-1})=4(2^{k-1})(2k-k+1)=(k+1)2^{k+1}$<br>
Therefore, by strong induction, we prove that $a_n=n\cdot2^n$
