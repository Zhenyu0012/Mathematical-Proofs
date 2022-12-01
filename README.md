## $\mathrm{Text Book}$
INTRODUCTION TO REAL ANALYSIS, by Robert G. Bartle & Donald R. Sherbert, 4th edition

## $\S 1.2,1.3\ \mathrm{Principle\ of\ Induction}$ 

<p align="center">Induction Definition</p>

Let $n\in\mathbb{N}$ (from 1) and $P(n)$ be a statement. Suppose that

1. $P(n_0)$ is true ( $n_0\in\mathbb{N}$ )
2. If $P(n_0)$ is true, then $P(n+1)$ is true

Then $P(n)$ is true for all $n\in\mathbb{N}, n\ge n_0$.

<br>

<p align="center">Strong Induction Definition</p>

Let $n\in\mathbb{N}$ and $P(n)$ be a statement. Suppose that

1. $P(n_0)$ is true ( $n_0\in\mathbb{N}$ )
2. If $P(n_0), P(n_0+1), …, P(k)$ are true, then $P(k+1)$ is true

Then $P(n)$ is true for all $n\in\mathbb{N}, n\ge n_0$.

---

**Example 1**: Show that $n<2^n$ for all $n\in\mathbb{N}$

*Proof*:<br>
Let $n=1$, then $1<2^1=2$.<br>
Assume $n<2^n$, show that $(n+1)<2^{n+1}$.<br>
Since $n<2^n$, $n+1<2^n+1<2^n+2^n=2^{n+1}$, it concludes that $n+1<2^{n+1}$. <br>
Therefore, by induction, we prove that $n<2^n$.

<br>
<br>

**Example 2**: Prove that $2n-3\leq 2^{n-2}$ for all $n \geq 5$, $n\in \mathbb{N}$.

*Proof*:<br>
Let $n=5$, then $7<2^{3}$.<br>
Assume $2n-3\leq 2^{n-2}$, show that $2n-1\leq 2^{n-1}$, i.e., $2(n+1)-3\leq 2^{(n+1)-2}$.<br>
Then,

$$\begin{aligned}
2n-3\leq 2^{n-2}&\Rightarrow 2n-3+2\leq 2^{n-2}+2\leq 2^{n-2}+2^{n-2} \\
&\Rightarrow 2n-1\leq 2^{n-2}+2\leq2^{n-1} \\
&\Rightarrow 2n-1\leq 2^{n-1}
\end{aligned}$$

Therefore, by induction, we prove that $2n-3\leq 2^{n-2}$ for all $n \geq 5$.

<br>
<br>

**Example 3**: Let $(a_n)\_{n\in\mathbb{N}}$ be a sequence, satisfying $a_1=2, a_2=8$, and $a_n=4(a_{n-1}-a_{n-2}), n\ge 3$. Show that $a_n=n\cdot2^n$

*Proof*:<br>
Let $n=1$, then $a_1=2=1\cdot2^1$<br>
&ensp;&ensp;&ensp; $n=2$, then $a_2=8=2\cdot2^2$<br>
Assume $a_j=j\cdot2^j$ for all $1\le j\le k$. Show that $a_{k+1}=(k+1)\cdot2^{k+1}$<br>
Since $a_{k+1}=4(a_k-a_{k-1})$, by strong induction, $a_{k+1}=4(k2^k-(k-1)2^{k-1})=4(2^{k-1})(2k-k+1)=(k+1)2^{k+1}$<br>
Therefore, by strong induction, we prove that $a_n=n\cdot2^n$

<br>
<br>

**Example 4**: Let the numbers $x_n$ be defined as follows: $x_1 \coloneqq1, x_2 \coloneqq2$, and $x_{n+2} \coloneqq\frac{1}{2}(x_{n+1} + x_n)$ for all $n\in N$. Use the Principle of Strong Induction to show that $1 \leq x_n\leq 2$ for all $n \in N$.

*Proof*:<br>
Let $n=1, x_1=1, 1\le x_1\le2$<br>
&ensp;&ensp;&ensp; $n=2, x_2=2, 1\le x_2\le2$<br>
Assume $x_j\coloneqq\frac{1}{2}(x_{j-1} + x_{j-2})$ for all $3\le j\le k$, s.t., $1\le x_j\le2$. Show that $x_{k+1}=\frac{1}{2}(x_{k}+x_{k-1})$.<br>
By strong induction, $1\le x_k\le2$ and $1\le x_{k-1}\le2$.<br>
Then,

$$\begin{aligned}
1\le x_k\le 2&\Rightarrow2\le x_k+x_{k-1}\le 4 \\
&\Rightarrow1\le \frac{1}{2}(x_k+x_{k-1})\le 2 \\
&\Rightarrow 1\le x_{k+1} \le 2
\end{aligned}$$

Therefore, by strong induction, we prove that $1 \leq x_n\leq 2$ for all $n \in N$.

## $\S 1.1\ \mathrm{Sets\ and\ Functions}$

<p align="center">Injection, Surjection, and Bijection Definitions</p>

Let $S$ be a set. Let $f: A\to B$, i.e. $a\to f(a)$, be a function.
1. If $f(x_1)\ne f(x_2)$ whenever $x_1\ne x_2$, then $f$ is called one-to-one, or injective.
2. If any $b\in B$, there is $a\in A$, s.t., $f(a)=b$, then $f$ is called onto, or surjective.
3. If $A\to B$ is both injective and surjective, then $f$ is called bijective (from $A$ to $B$).

<br>

<p align="center">Theorem 1</p>

Let $A, B$ be sets. If there is bijection between $A$ and $B$, then we say $A$ and $B$ have the same cardinality.

<br>

<p align="center">Tricks for proving two infinite sets have the same cardinality</p>

1. Cantor–Bernstein Theorem, i.e., if $|A|\le|B|$ and $|B|\le|A|$ then $|A|=|B|$
2. Hilbert's Hotel

---

**Example 1**: Show that $E=\\{2n|n\in\mathbb{N}\\}$ and $\mathrm{N}$ have the same cardinality.

*Proof*:<br>
Since $E = 2, 4, 6, 8, ..., 2n$<br>
&ensp;&ensp;&ensp;&ensp;&ensp; $N = 1, 2, 3, 4, ..., n$,<br>
we can define a function $f$, s.t., $f(n) = 2n, \forall n\in\mathbb{N}$.<br>
Therefore, $f$ is a bijection between $N$ and $E$, which implies that $N$ and $E$ have the same cardinality.

<br>
<br>

**Example 2**: Show that $(0,1)$ and $[0,1]$ have the same cardinality. ([Hilbert's Hotel](https://math.stackexchange.com/questions/1006445/proving-0-1-and-0-1-have-the-same-cardinality))

*Proof*:<br>
Let $S$ be a set, s.t., $S=\\{\frac{1}{n}, n\in\mathbb{N}\land n \ge 4\\}$.<br>
Then define $f:(0,1)\to[0,1]$ satisfying<br>

$$f(n)=\begin{cases}
0, &\mathrm{when\ }n=\frac{1}{2} \\
1, &\mathrm{when\ }n=\frac{1}{3} \\
\frac{1}{m-2}, &\mathrm{when\ }n=\frac{1}{m}, m\ge 4 \mathrm{\ and\ } m\in\mathbb{N} \\
n, &\mathrm{when\ }n\notin S
\end{cases}$$

Therefore, $f$ is a bijection between $(0,1)$ and $[0,1]$, which implies that $(0,1)$ and $[0,1]$ have the same cardinality.

<br>
<br>

**Example 3**: Show that $[0,1)$ and $(2,4]$ have the same cardinality.

**Example 4**: Show that $\mathbb{N}$ and $\mathbb{Q}$ have the same cardinality.

---

<p align="center">Further Reading<p>

[1]: [Why do the rationals, integers and naturals all have the same cardinality?](https://math.stackexchange.com/questions/182236/why-do-the-rationals-integers-and-naturals-all-have-the-same-cardinality)

