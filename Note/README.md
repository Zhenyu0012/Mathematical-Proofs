## $\mathrm{Text Book}$
INTRODUCTION TO REAL ANALYSIS, by Robert G. Bartle & Donald R. Sherbert, 4th edition

## $\S 1.2,1.3\ \mathrm{Principle\ of\ Induction}$ 

<p align="center"><b>Induction Definition</b></p>

Let $n\in\mathbb{N}$ (from 1) and $P(n)$ be a statement. Suppose that

1. $P(n_0)$ is true ( $n_0\in\mathbb{N}$ )
2. If $P(n_0)$ is true, then $P(n+1)$ is true

Then $P(n)$ is true for all $n\in\mathbb{N}, n\ge n_0$.

<p align="center"><b>Strong Induction Definition</b></p>

Let $n\in\mathbb{N}$ and $P(n)$ be a statement. Suppose that

1. $P(n_0)$ is true ( $n_0\in\mathbb{N}$ )
2. If $P(n_0), P(n_0+1), …, P(k)$ are true, then $P(k+1)$ is true

Then $P(n)$ is true for all $n\in\mathbb{N}, n\ge n_0$.

---

**Example 1**: Show that $n<2^n$ for all $n\in\mathbb{N}$

*Base step*: Let $n=1$, then $1<2^1=2$. Thus, we prove that $P(1)$ is true.

*Inductive step*: Assume $n<2^n$, show that $(n+1)<2^{n+1}$.<br>
&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&thinsp;Since $n<2^n$, $n+1<2^n+1<2^n+2^n=2^{n+1}$, it concludes that $n+1<2^{n+1}$.<br>

Therefore, by induction, we prove that $n<2^n$.

<br>
<br>

**Example 2**: Prove that $2n-3\leq 2^{n-2}$ for all $n \geq 5$, $n\in \mathbb{N}$.

*Base step*: Let $n=5$, then $7<2^{3}$. Thus, we prove that $P(1)$ is true.

*Inductive step*: Assume $2n-3\leq 2^{n-2}$, show that $2n-1\leq 2^{n-1}$, i.e., $2(n+1)-3\leq 2^{(n+1)-2}$.

$$\begin{aligned}
2n-3\leq 2^{n-2}&\Rightarrow 2n-3+2\leq 2^{n-2}+2\leq 2^{n-2}+2^{n-2} \\
&\Rightarrow 2n-1\leq 2^{n-2}+2\leq2^{n-1} \\
&\Rightarrow 2n-1\leq 2^{n-1}
\end{aligned}$$

Therefore, by induction, we prove that $2n-3\leq 2^{n-2}$ for all $n \geq 5$.

<br>
<br>

**Example 3**: Let $(a_n)\_{n\in\mathbb{N}}$ be a sequence, satisfying $a_1=2, a_2=8$, and $a_n=4(a_{n-1}-a_{n-2}), n\ge 3$. Show that $a_n=n\cdot2^n$

*Base step*: Let $n=1$, then $a_1=2=1\cdot2^1$.<br>
&emsp;&emsp;&emsp;&emsp;&emsp;&thinsp;Let $n=2$, then $a_2=8=2\cdot2^2$.<br>
&emsp;&emsp;&emsp;&emsp;&emsp;&thinsp;Thus, we prove that both $P(1)$ and $P(2)$ are true.

*Inductive step*: Assume $a_j=j\cdot2^j$ for all $1\le j\le k$. Show that $a_{k+1}=(k+1)\cdot2^{k+1}$<br>
&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&thinsp;Since $a_{k+1}=4(a_k-a_{k-1})$, by strong induction, $a_{k+1}=4(k2^k-(k-1)2^{k-1})=4(2^{k-1})(2k-k+1)=(k+1)2^{k+1}$

Therefore, by strong induction, we prove that $a_n=n\cdot2^n$

<br>
<br>

**Example 4**: Let the numbers $x_n$ be defined as follows: $x_1 \coloneqq1, x_2 \coloneqq2$, and $x_{n+2} \coloneqq\frac{1}{2}(x_{n+1} + x_n)$ for all $n\in N$. Use the Principle of Strong Induction to show that $1 \leq x_n\leq 2$ for all $n \in \mathbb{N}$.

*Base step*: Let $n=1, x_1=1, 1\le x_1\le2$<br>
&emsp;&emsp;&emsp;&emsp;&emsp;&thinsp;Let $n=2, x_2=2, 1\le x_2\le2$<br>
&emsp;&emsp;&emsp;&emsp;&emsp;&thinsp;Thus, we prove that both $P(1)$ and $P(2)$ are true.

*Inductive step*: Assume $x_j\coloneqq\frac{1}{2}(x_{j-1} + x_{j-2})$ for all $3\le j\le k$, s.t., $1\le x_j\le2$. Show that $x_{k+1}=\frac{1}{2}(x_{k}+x_{k-1})$.<br>
&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&thinsp;By strong induction, $1\le x_k\le2$ and $1\le x_{k-1}\le2$.

$$\begin{aligned}
1\le x_k\le 2&\Rightarrow2\le x_k+x_{k-1}\le 4 \\
&\Rightarrow1\le \frac{1}{2}(x_k+x_{k-1})\le 2 \\
&\Rightarrow 1\le x_{k+1} \le 2
\end{aligned}$$

Therefore, by strong induction, we prove that $1 \leq x_n\leq 2$ for all $n \in \mathbb{N}$.

## $\S 1.1\ \mathrm{Sets\ and\ Functions}$

<p align="center"><b>Injection, Surjection, and Bijection Definitions</b></p>

Let $S$ be a set. Let $f: A\to B$, i.e. $a\to f(a)$, be a function.
1. If $f(x_1)\ne f(x_2)$ whenever $x_1\ne x_2$, then $f$ is called one-to-one, or injective.
2. If any $b\in B$, there is $a\in A$, s.t., $f(a)=b$, then $f$ is called onto, or surjective.
3. If $A\to B$ is both injective and surjective, then $f$ is called bijective (from $A$ to $B$).

<p align="center"><b>Cardinality Definition</b></p>

Let $S$ be a set. We use cardinality to denote the number of elements in $S$.<br>
Let $A, B$ be sets. If there is bijection between $A$ and $B$, then we say $A$ and $B$ have the same cardinality.

<p align="center"><b>Denumerable Definition</b></p>

Let $S$ be a set. If $S$ and $\mathbb{N}$ have the same cardinality, then $S$ is called denumerable, or infinitely countable.

<p align="center"><b>Tricks for proving two infinite sets have the same cardinality</b></p>

- Defining a bijection directly if the case is trivial, i.e., two sets are finite.
- Cantor-Schröder-Bernstein Theorem<sup>[1]</sup>: Let $S$ and $T$ be sets. Suppose there are injective functions $f: S \to T$ and $g: T \to S$. Then $S$ and $T$ have the same cardinality.

---

**Example 1**: Show that $E=\\{2n|n\in\mathbb{N}\\}$ and $\mathrm{N}$ have the same cardinality.

Since $E\subset\mathbb{N}$, there exists a function $f:E\to\mathbb{N}$, namely the function $f(x)=x,\forall x\in E$. Suppose $f(a)=f(b)$, then $f(a)=f(b)\Rightarrow a=b$. Thus, $f$ is injective. Let $g(x) = 4x, \forall x\in\mathbb{N}$. If $g(a)=g(b)$, then $g(a)=g(b)\Rightarrow 4a=4b\Rightarrow a=b$. Thus, $g$ is injective. Thus, by Cantor-Schröder-Bernstein Theorem, $\mathbb{N}$ and $E$ have the same cardinality.

<p align="center">
  <img src="../pictures/1.1_example1.1.jpg" alt="1.1_example1" width="18%"/>
  &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;
  <img src="../pictures/1.1_example1.2.jpg" alt="1.1_example2" width="18%"/>
  <br>
  <br>
  $f:E\to \mathbb{N}$ &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; $g:\mathbb{N}\to S(E)$
</p>

<br>
<br>

**Example 2**: Show that $(0,1)$ and $[0,1]$ have the same cardinality.

Clearly, $(0,1)$ injects into $[0,1]$. Let $g(x) = \frac{1}{2}x+\frac{1}{10}, \forall x\in[0,1]$. If $g(a)=g(b)$, then $g(a)=g(b)\Rightarrow \frac{1}{2}a+\frac{1}{10}=\frac{1}{2}b+\frac{1}{10}\Rightarrow\frac{1}{2}a=\frac{1}{2}b\Rightarrow a=b$. Hence, $g$ is injective. Therefore, by Cantor-Schröder-Bernstein Theorem, $[0,1]$ and $(0,1)$ have the same cardinality.

<br>
<br>

**Example 3**: Show that $\[0,1)$ and $(2,4]$ have the same cardinality.

Let $f(x)=x+3,\forall x\in\[0,1)$. Suppose $f(a)=f(b)$, then $f(a)=f(b)\Rightarrow a+3=b+3\Rightarrow a=b$. Thus, $f$ is injective. Let $g(x)=\frac{1}{8}x,\forall x\in(2,4]$. Suppose $g(a)=g(b)$, then $g(a)=g(b)\Rightarrow\frac{1}{8}a=\frac{1}{8}b\Rightarrow a=b$. Hence, $g$ is injective. Therefore, by Cantor-Schröder-Bernstein Theorem, $\[0,1)$ and $(2,4]$ have the same cardinality.

<br>
<br>

**Example 4**: Show that $\mathbb{N}$ and $\mathbb{Z}$ have the same cardinality.

Clearly, $\mathbb{N}$ injects into $\mathbb{Z}$. Let $g:\mathbb{Z}\to\mathbb{N}$ be a pisewise function, s.t.,

$$
g(x)=\begin{cases}
2x+1&\mathrm{if\ }x\ge0\\
-2x&\mathrm{if\ }x<0\\
\end{cases}
$$

Suppose $a$ and $b$ are both non-negative and $g(a)=g(b)$, then $g(a)=g(b)\Rightarrow 2a+1=2b+1\Rightarrow 2a=2b\Rightarrow a=b$. Similarly, suppose $a$ and $b$ are both negative and $g(a)=g(b)$, then $g(a)=g(b)\Rightarrow -2a=-2b\Rightarrow a=b$. Hence, $g$ is injective. Thus, by Cantor-Schröder-Bernstein Theorem, $\mathbb{N}$ and $\mathbb{Z}$ have the same cardinality.

<br>
<br>

**Example 5**: Show that $\mathbb{N}$ and $\mathbb{Q}$ have the same cardinality.

---

<p align="center">Further Reading<p>

[1]: [Class Notes from Millersville University](https://sites.millersville.edu/bikenaga/math-proof/cardinality/cardinality.pdf)<br>
[2]: [Proof of Cantor-Schröder-Bernstein Theorem](http://www.cs.cornell.edu/courses/cs2800/2017fa/lectures/lec14-cantor.html)

