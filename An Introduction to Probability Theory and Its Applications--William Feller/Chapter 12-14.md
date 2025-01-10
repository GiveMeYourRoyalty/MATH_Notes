# An Introduction to Probability Theory and Its Applications

**Arthur: William Feller**

- [An Introduction to Probability Theory and Its Applications](#an-introduction-to-probability-theory-and-its-applications)
  - [Chapter 12 Compound Distributions. Branching Processes](#chapter-12-compound-distributions-branching-processes)
    - [1. Sum of A Random Number of Variables](#1-sum-of-a-random-number-of-variables)
    - [2. The Compound Poisson Distribution](#2-the-compound-poisson-distribution)
    - [3. Examples for Branching Processes](#3-examples-for-branching-processes)
    - [4. Extinction Probabilities in Branching Processes](#4-extinction-probabilities-in-branching-processes)
  - [Chapter 13 Recurrent Events. Renewal Theory](#chapter-13-recurrent-events-renewal-theory)
    - [2. Definitions](#2-definitions)

<br><br>

## Chapter 12 Compound Distributions. Branching Processes

<br>

In many situations the number of terms in the sums off independent random variables is itself a random variable.

<br>

### 1. Sum of A Random Number of Variables

\
Let $\{\bold{X}_k\}$ be a sequence of mutually independent random variables with the common distribution $\bold{P}\{\bold{X}_k=k\}=f_j$ and the generating function $f(s)=\sum f_is^i$. We are often interested in sums

$$
\bold{S_N}=\bold{X}_1+\bold{X}_2+\cdots+\bold{X_N}
$$

where the number $\bold{N}$ of terms is arandom variable independent of the $\bold{X}_j$. Let $\bold{P}\{\bold{N}=n\}=g_n$ be the distribution of $\bold{N}$ and $g(s)=\sum g_ns^n$ its generating function. FOr the distribution $\{h_j\}$ of $\bold{S_N}$ we get from the fundamental formula for conditional probabilites

$$
(1.1) \hspace{4em} h_j=\bold{P}\{\bold{S_N}=j\}=\sum _{n=0}^\infty \bold{P}\{\bold{N}=n\}\bold{P}\{\bold{X}_1+\cdot+\bold{X}_j=j\}
$$

For a fixed $n$ the distribution of $\bold{X}_1+\bold{X}_2+\cdots+\bold{X}_n$ is given by the $n$-fold convolution of $\{f_i\}$ with itself, and therefore (1.1) can be written in the compact form

$$
(1.2) \hspace{4em} \{h_j\}=\sum _{n=0}^\infty g_n\{f_n\}^{n*}
$$

This formula can be simplified by the use of generating functions. The generating function of $\{f_j\}^{n*}$ is $f^n(s)$ and it is obvious from (1.2) that the generating function of the sum $\bold{S_N}$ is given by

$$
(1.3) \hspace{4em} h(s)=\sum _{j=0}^\infty h_js^j=\sum _{n=0}^\infty g_nf^n(s)
$$

The right side is the Taylor expansion of $g(s)$ with $s$ replaced by $f(s)$; hence it equals $g(f(s))$. This proves the

**Theorem.** The generating function of the sum $\bold{S_N}=\bold{X}_1+\cdots+\bold{X_N}$ is the compound function $g(f(s))$.

<br><br>

### 2. The Compound Poisson Distribution

\
**Definition.** A probability generating function $h$ is called infinitely divisible if for each positive integer $n$ the $n$th root $\sqrt[n]{h}$ is again a probability generating function.

\
**Theorem.** The only infinitely divisible probability generating functions are those of the form $h_t(s)=e^{-\lambda t}\sum _{n=0} \frac{(\lambda t)^n}{n!}\{f_i\}^{n*}$ with $\{f_i\}$ a probability distribution on $0,1,...$.

\
The theorem may be restated in the form of the

**Criterion.** A function $h$ is an infinitely divisible probability generating function if and only if, $h(1)=1$ and

$$
(2.6) \hspace{2em} \log \frac{h(s)}{h(0)}=\sum _{k=1}^\infty a_ks^k \hspace{1em} \text{where } a_k \ge 0, \hspace{1em} \sum a_k = \lambda < \infty
$$

<br><br>

### 3. Examples for Branching Processes

\
In words the process may be described as follows.

We consider particles which are able to produce new particles of like kind. A single particle forms the original, or zero generation. Every particle has probability $p_k (k=0,1,2,...)$ of creating exactly $k$ new particles; the direct descendants of the $n$th generation form the $(n+1)st generation. The particles of each generation act independently of each other. We are interested in the size of the successive generations.

\
A few examples
  1. Nuclear chain reactions
  2. Survival of family names
  3. Genes and mutations

<br><br>

### 4. Extinction Probabilities in Branching Processes

\
Denote by $\bold{Z}_n$ the size of the $n$th generation, and by $\bold{P}_n$ the generating function of its probability distribution. By assumption $\bold{Z}_0=1$ and

$$
(4.1) \hspace{4em} P_1(s)=P(s)=\sum _{k=0}^\infty p_ks^k
$$

The $n$th generation can be divided into $\bold{Z}_1$ clans according to the ancestor in the first generation. This means that $\bold{Z}_n$ is the sum of $\bold{Z}_1$ random variables $\bold{Z}_n^{(k)}$, each representing the size of the offspring of one member of the first generation. By assumption each $\bold{Z}_n^{(k)}$ has the same probability distribution as $\bold{Z}_{n-1}$ and (for fixed $n$) the variables $\bold{Z}_n^{(k)}$ are mutually independent. The generating function $P_n$ is therefore given by the compound function

$$
(4.2) \hspace{4em} P_n(s)=P(P_{n-1}(s))
$$

This result enables us to calculate recursively all the generating functions.

<br><br>

The first question concerning our branching process is whether is will continue forever or whether the progeny will die out after finitely many generations. Put

$$
(4.5) \hspace{4em} x_n=\bold{P}\{\bold{Z}_n=0\}=P_n(0)
$$

This is the probability that the process terminates at or before the $n$th generation. By definition $x_1=p_0$ and from (4.2) it is clear that

$$
(4.6) \hspace{4em} x_n=P(x_{n-1})
$$

\
$$
(4.8) \hspace{4em} \mu=P'(1)=\sum _{k=0}^\infty kp_k \le \infty
$$

is *the expected number of direct descendants*.

\
**Theorem.** If $\mu \le 1$ the process dies out with probability one. If, however, $\mu > 1$ the probability $x_n$ that the process terminates at or before the $n$th generation tends to the unique root $x < 1$ of the equation $x=P(x)$.

[Some contents are skipped at first reading.]

<br><br>

## Chapter 13 Recurrent Events. Renewal Theory

<br>

### 2. Definitions