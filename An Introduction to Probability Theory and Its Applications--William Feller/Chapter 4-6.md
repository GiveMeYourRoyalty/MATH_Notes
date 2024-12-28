# An Introduction to Probability Theory and Its Applications

**Arthur: William Feller**

- [An Introduction to Probability Theory and Its Applications](#an-introduction-to-probability-theory-and-its-applications)
  - [Chapter 4 Combination of Events](#chapter-4-combination-of-events)
    - [1. Union of Events](#1-union-of-events)
    - [2. Application to the Classical Occupancy Problem](#2-application-to-the-classical-occupancy-problem)
    - [3. The Realization of $m$ among $N$ events](#3-the-realization-of-m-among-n-events)
    - [4. Application to Matching and Guessing](#4-application-to-matching-and-guessing)

## Chapter 4 Combination of Events

### 1. Union of Events

**Notation.** We shall denote the probabilities $A_i, A_j, \text{ and } A_k$, etc. occurring simultaneously by the letter $p$ with appropriate subscripts.

$$
(1.2) \hspace{4em} p_{ijk} = \bold{P}\{A_i A_j A_k\}, ...
$$

The order of the subscripts is irrelevant, but for uniqueness we shall always *write the subscripts in increasing order*. Two subscripts are never equal.

**Notation.** For the sum of all $p$'s with $r$ subscripts we shall write $S_r$ that is,

$$
(1.3) \hspace{4em} S_1 = \sum p_i, \hspace{1em} S_2 = \sum p_{ij}, \hspace{1em} S_3 = \sum p_{ijk}, ...
$$

Here $i < j < k < \cdots \le N$, so that in the usms each combination appears once and only once; hence $S_r$ has $\binom{N}{r}$ terms.

**Theorem.** The probability $P_1$ of the realization of at least one among the event $A_1, A_2, ..., A_N$ is given by

$$
(1.5) \hspace{4em} P_1 = S_1 - S_2 + S_3 - S_4 + - \cdots \pm S_N
$$

### 2. Application to the Classical Occupancy Problem

We now return to the problem of a random distribution of $r$ balls in $n$ cells, assuming that each arrangement has probability $n^{-r}$. We seek the probability $p_m(r,n)$ of finding exactly $m$ cells empty.

Let $A_k$ be the event that cell number $k$ is empty. The probabilities of leaving some preassigned cells empty

$$
p_i = (1 - \frac{1}{n})^r, p_{ij} = (1 - \frac{2}{n})^r, p_{ijk} = (1 - \frac{3}{n})^r \text{ and } S_v = \binom{n}{v} (1 - \frac{v}{n})^r
$$

The probability of at least one cell is empty is given by (1.5), and hence the probability tht all cells are occupied

$$
(2.3) \hspace{4em} p_0(r, n) = 1 - S_1 + S_2 - + \cdots = \sum ^n _{v = 0} (-1)^v \binom{n}{v} (1 - \frac{v}{n})^r
$$

Now consider the distribution in which exactly $m$ cells are empty. The $r$ balls are distributed among the remaining $n - m$ cells so that each of these cells is occupied, the number of such distributions is $(n - m)^r p_0(r, n - m)$.

$$
\begin{aligned}
(2.4) \hspace{4em} p_m(r,n) = \binom{n}{m} (1-\frac{m}{n})^r p_0(r, n-m)\\
= \binom{n}{m} \sum ^{n-m} _{v=0} (-1)^v \binom{n-m}{v} (1-\frac{m+v}{n})^r
\end{aligned}
$$

Now we proceed to consider the limiting form of the formular (2.4). The relation between $r$ and $n$ is, in principle, arbitrary, but only the intermediate case of the ratio $\frac{r}{n}$ is of our interest.

We begin by estimating the quantity $S_v$ of (2.2). Since

$$
(n-v)^v < (n)_v < n^r
$$

We have

$$
(2.5) \hspace{4em} n^v (1-\frac{v}{n})^{v+r} < v! S_v < n^v(1-\frac{v}{n})^r
$$

For $0 < t < 1, t < -\log(1-t) < \displaystyle\frac{t}{1-t}$. Therefore

$$
(2.6) \hspace{4em} \{ne^{-\frac{v+r}{n-v}}\} ^v < v! S_v < \{ne^{-\frac{r}{n}}\}^v.
$$

Now put for abbreviation $\hspace{4em} ne^{-\frac{r}{n}} = \lambda$
and suppose that $r$ and $n$ increase in such a way that $\lambda$ reminas constrained to a finite interval $0 < a < \lambda < b$.

[Omissions]

$$
(2.10) \hspace{4em} p_m(r, n) - e^{-\lambda}\frac{\lambda ^m}{m!} \rightarrow 0
$$

**Theorem.** If $n$ and $r$ tend to infinity so that $\lambda = ne^{-r/n}$ remains bounded, then (2.10) holds for each fixed $m$
The approximation expressions

$$
(2.11) \hspace{4em} p(m; \lambda) = e^{-\lambda} \frac{\lambda ^m}{m!}
$$

defines the so-called ***Poisson distribution***.

### 3. The Realization of $m$ among $N$ events

The theorem of section 1 can be strengthened as follows

**Theorem.** For any integer $m$ with $1 \le m \le N$ the probability $p_{[m]}$ that exactly $m$ among the $N$ events $A_1, ..., A_N$ occur simultaneously is given by

$$
(3.1) \hspace{4em} P_{[m]} = S_m - \binom{m+1}{m}S_{m+1} +\binom{m+2}{m} S_{m+2} -+ \cdots \pm \binom{N}{m}S_N
$$

(3.1) gives the correct value for $m = 0$ provided we put $S_0 = 1$.

### 4. Application to Matching and Guessing
