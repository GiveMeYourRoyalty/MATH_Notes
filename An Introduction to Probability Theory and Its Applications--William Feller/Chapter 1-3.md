# An Introduction to Probability Theory and Its Applications

**Arthur: William Feller**

- [An Introduction to Probability Theory and Its Applications](#an-introduction-to-probability-theory-and-its-applications)
  - [Introduction: The Nature of Probability Theory](#introduction-the-nature-of-probability-theory)
    - [1. The Background](#1-the-background)
    - [2. Procedure](#2-procedure)
    - [3. "Statistical" Probability](#3-statistical-probability)
    - [4. Summary](#4-summary)
  - [Chapter 1 The Sample Space 样本空间](#chapter-1-the-sample-space-样本空间)
    - [1. The Empirical Background](#1-the-empirical-background)
    - [3. The Sample Space. Events](#3-the-sample-space-events)
    - [4. Relations among Events](#4-relations-among-events)
    - [5. Discrete Sample Spaces](#5-discrete-sample-spaces)
    - [7. The Basic Definitions and Rules](#7-the-basic-definitions-and-rules)
  - [Chapter 2 Elements of Combinatorial Analysis](#chapter-2-elements-of-combinatorial-analysis)
    - [\*5. Application to Occupancy Problems](#5-application-to-occupancy-problems)
    - [6. The Hypergeometric Distribution](#6-the-hypergeometric-distribution)
    - [7. Examples for Waiting Times](#7-examples-for-waiting-times)
    - [8. Binomial Coefficients](#8-binomial-coefficients)
    - [9. Stirling's Formula](#9-stirlings-formula)
    - [12. Problems and Identities involving Binomial Coefficients](#12-problems-and-identities-involving-binomial-coefficients)
  - [Chapter 3 Fluctuations in Coin Tossing and Random Walks](#chapter-3-fluctuations-in-coin-tossing-and-random-walks)
    - [1. General Orientation. The Reflection Principle](#1-general-orientation-the-reflection-principle)
    - [2. Random Walks: Basic Notions and Notations](#2-random-walks-basic-notions-and-notations)
    - [3. The Main Lemma](#3-the-main-lemma)
    - [4. Last Visit and Long Leads](#4-last-visit-and-long-leads)
    - [\*5. Changes of Sign](#5-changes-of-sign)
    - [7. Maxima and First Passages](#7-maxima-and-first-passages)
## Introduction: The Nature of Probability Theory

### 1. The Background

When learning in new field, we must carefully distinguish between 3 aspects of the theory: (1) the formal logical content, (2) the intuitive background, (3) the applications.

### 2. Procedure

Starting from intuition, like tossing a coin or throwing dice, then prove some theorems and show how to apply

### 3. "Statistical" Probability

Our probabilities do not refer to judgments but to possible outcomes of a *conceptual experiment*.

### 4. Summary

At any rate, even for applications freedom and flexibility are essential, and it would be pernicious to fetter the theory to fixed poles.

## Chapter 1 The Sample Space 样本空间

### 1. The Empirical Background

- **Events**: the results of experiments or observations
  - **compound/decomposable event**: an aggregate of certain simple events
  - **simple/indecomposable event**: also called sample points or points for short
- The aggregate of all sample points will be called the ***sample space***
- All events connected with a given (idealized) experiment can be described as aggregates of sample points

### 3. The Sample Space. Events

**Sample space** and **event** are **the primitive and undefined notions of the theory** precisely as the notions of "points" and "straight line" remains undefined in an axiomatic treatment of Euclidean geometry.

### 4. Relations among Events

- Suppose that an arbitrary, but fixed, sample space $\mathfrak{S}$ is given.
  - We use capitals to denote *events*
  - $x \in A$, a point $x$ is contained in the event A

  - **Definition 1**. the notation $A = 0$ means *the event A contains no sample points*. 0 is a symbol, not a number.
  - **Definition 2**. the event consisting of all points not contained in the event A wil be called *the complementary event (or negation) of A* and denoted by $A'$. In particular, $\mathfrak{S}' = 0$
  - **Definition 3**. To every collection $A, B, C...$ of events we define 2 new events as follows
    - The aggregate of the sample points which belongs to all the given sets, $ABC...$, called the *intersection/simultaneous realization* of $A, B, C...$
    - The aggregate of sample points belong to at least one of the given sets, $A \cup B \cup C...$, called the *union /realization of at least one* of the given events
    - The events $A, B, C...$ are mutually exclusive if no two have a point in common, that is, if $AB = 0,  AC = 0, ..., BC = 0, ...$
    - **Definition 4**. The symbols $A \subset B$ (A implies B) and $B \supset A$ (B is implied by A) are equivalent and signify that every point of A is contained in B. In this case, we shall write $B - A$ instead of $BA'$ to denote the event that $B$ but not $A$ occurs

### 5. Discrete Sample Spaces

**Definition**: A sample space is called *discrete* if it contains only finitely many points or infinitely many points which can be arranged into a simple sequence $E_1, E_2, ...$

The probabilities of events in discrete sample spaces are obtained by *mere addtions*, whereas in other spaces *integrations* are necessary.

### 7. The Basic Definitions and Rules

**Fundamental Convention**. Given a discrete sample space $\mathfrak{S}$ with sample points $E_1, E_2, \dots$, we shall assume that with each $E_j$ there is assoiated a non-negative number, called the *probability of $E_j$* and denoted by $P\{E_j\}$

$$
P\{E_1\} + P\{E_2\} + \cdots  = 1
$$

\
**Definition**. $P\{A\}$ of any event A is the sum of the probabilities of all sample points in it

\
**Theorem**. $P\{A_1 \cup A_2\} = P\{A_1\} + P\{A_2\} - P\{A_1 A_2\}$

## Chapter 2 Elements of Combinatorial Analysis

- **Notation**: $(n)_r = n(n-1) \cdots (n-r+1)$ [This notaions is not standard but will be used in this book, even when n is not an integer]
- **Binomial coefficient** $\binom{n}{r} = \frac{(n)_r}{r!} = \frac{n!}{r!(n-r)!} = \frac{n(n-1) \cdots (n-r+1)}{1 \cdot 2 \cdots (r-1)r}$
- We define $\binom{n}{0} = 1, 0! = 1 \text{ and } (n)_0 = 1$
- **Multinomial coefficient** $\binom{n}{r_1}\binom{n-r_1}{r_2}\binom{n-r_1-r_2}{r_3} \cdots \binom{n-r_1- \cdots -r_{k-2}}{r_{k-1}} = \frac{n!}{r_1! r_2! \cdots r_3!}$, where $r_1 + r_2 + \cdots r_k = n$

### *5. Application to Occupancy Problems

- **Model:** placing randomly **r** indistinguishable balls into n distinguishable cells.
  1. The number of distinguishale distributions

  $$
  A_{r, n} = \binom{n + r - 1}{r} = \binom{n + r - 1}{n - 1}
  $$

  2. The number of distinguishable distributions in which no cell remains empty

  $$
  \binom{r - 1}{n - 1}
  $$

- Model: placing randomly r indistinguishable balls into n indistinguishble cells [not easy to find formula, need further study]

- Examples [consider a random distribution of r indistinguishable particles in n distinguishable cells]
  - *Maxwell-Boltzmann statistics*, all $n^r \text{ arrangements have equal probabilities}$
  - *Bose-Einstein statistics*, only distinguishable arrangements are considered and that each is assigned probability $\frac{1}{A_{r, n}}$
  - *Fermi-Dirac statistics*, with 2 assumptions, (1) it's impossible for 2 or more particles to be in the same cell, and (2) all distinguishable arrangements satisfying the first condition have equal probabilities. $\binom{n}{r} equal possible arrangements$

### 6. The Hypergeometric Distribution

In a population of $n$ elements $n_1$ are red and $n_2 = n - n_1$ are black. A group of $r$ elements is chosen at random. The probability $q_k$ that the group so chosen will contains exactly k red elements, where $0 \leq k \leq min(n_1, r)$

$$
q_k = \frac{\binom{n_1}{k}\binom{n - n_1}{r - k}}{\binom{n}{r}} = \frac{\binom{r}{k} \binom{n - r}{n_1 - k}}{\binom{n}{n_1}}
$$

- **Identity:** $\binom{r}{0} \binom{n - r}{n_1} + \binom{r}{1} \binom{n - r}{n_1 - 1} + \cdots + \binom{r}{n_1} \binom{n - r}{0} = \binom{n}{n_1}$
  It holds true for both positive and negative numbers $n$ and $r$ (it's meaningless if $n_1$ is not a positive number)

### 7. Examples for Waiting Times

**Situation:** Don't fix in advance the number $r$ of balls
  1. The random placing of continues until for the first time a ball is placed into a cell already occupied.
  *The probability of the process terminating at the rth step is*
  $$
  q_r = \frac{(n)_{r - 1} \cdot (r - 1)}{n^r} = (1 - \frac{1}{n}) \cdots (1 - \frac{r - 2}{n}) \cdot \frac{r - 1}{n}\\
  \text{with } q_1 = 0 \text{ and } q_2 = 1/n
  $$
  *The probability that the process lasts for more than r steps is* $p_r = 1 - (q_1 + q_2 + \cdots + q_r)$ or $p_1 = 1$ and
  $$
  p_r = \frac{(n)_r}{n^r} = (1 - \frac{1}{n}) \cdots (1 - \frac{r - 1}{n})
  $$

  2. We fix a cell (say cell number 1) and continue the procedure of placing balls as long as this cell remains empty
  *The probability that the process terminates at the rth step*
  $$
  q^*_r = (\frac{n - 1}{n})^{r - 1} \cdot \frac{1}{n}
  $$

### 8. Binomial Coefficients

- **Binomial coefficients** for all values of $x \isin R$ and all positive integers $r$
  $$
  \binom{x}{r} = \frac{(x)_r}{r!} = \frac{x(x - 1) \cdots (x - r + 1)}{r!}\\
  \binom{x}{0} = 1 \text{ and } \binom{x}{r} = 0 \text{ for } r < 0
  $$
  *We shall never use the symbol $\binom{x}{r}$ if $r$ is not an integer*

- Some properties
  1. *For any positive integer $n$*
    $$
    \binom{n}{r} = 0 \hspace{2em} \text{if either } r > n \text{ or } r < 0
    $$
  2. *For any number $x$ and any integer $r$*
    $$
    \binom{x}{r - 1} + \binom{x}{r} = \binom{x + 1}{r}
    $$

### 9. Stirling's Formula

- **Stirling's formula/approximation:**
  $$
  n! \thicksim \sqrt{2 \pi} n^{n + \frac{1}{2}} e^{-n}\\
  \lim _{n \rightarrow + \infty} \frac{n!}{\sqrt{2 \pi} n^{n + \frac{1}{2}} e^{-n}} = 1
  $$

**Elementary proof of Stirling's formula**

First, derive some estimate for

$$
\log n! = \log 1 + \log 2 + \cdots + \log n
$$

Use some integration techniques,

$$
n \log n - n < \log n! < (n + 1) \log (n + 1) - n
$$

This double inequality suggests comparing $\log n!$ with some quantiy close to the arithmetic mean of the extreme members. The simpliest of such quantity is $(n + \frac{1}{2}) \log n - n$, so accordingly we proceed to estimate the difference

$$
d_n = \log n! - (n + \frac{1}{2}) \log n + n
$$

Note that

$$
d_n - d_{n + 1} = (n + \frac{1}{2}) \log (\frac{n + 1}{n}) - 1
$$

But

$$
\frac{n+1}{n} = \frac{1 + \frac{1}{1+2n}}{1-\frac{1}{2n+1}}
$$

and using the expansion $\frac{1}{2} \log \frac{1+t}{1-t} = t + \frac{1}{3}t^3 + \frac{1}{5}t^5 + \cdots$, we get

$$
d_n - d_{n+1} = \frac{1}{3(2n+1)^2} + \frac{1}{5(2n+1)^4} + \cdots
$$

By comparison of the right side with geometric series with ratio $(2n + 1)^{-2}$,

$$
0 < d_n - d_{n + 1} < \frac{1}{3[(2n+1)^2 -1]} = \frac{1}{12n} - \frac{1}{12(n+1)}
$$

From above, we can see that the sequence $\{d_n\}$ is decreasing and the sequence $\{d_n - (12n)^-1\}$ is increasing. So a finite limit $C = \lim d_n$ exists. This is equivalent to

$$
\lim \log n! - (n + \frac{1}{2}) \log n + n = C\\
n! \thicksim \sqrt{2 \pi} n^{n + \frac{1}{2}} e^{-n}\\
$$

Except that $e^C = \sqrt{2 \pi}$ hasn't been proved yet.

**Refinement**. $\sqrt{2 \pi} n^{n + \frac{1}{2}} e^{-n} \cdot e^{(12n+1)^{-1}} < n! < \sqrt{2 \pi} n^{n + \frac{1}{2}} e^{-n} \cdot e^{(12n)^{-1}}$

### 12. Problems and Identities involving Binomial Coefficients

1. For integer $n \ge 2$
  $$
  1 - \binom{n}{1} + \binom{n}{2} -+ \cdots = 0\\
  \binom{n}{1} + 2 \binom{n}{2} + 3 \binom{n}{3} + \cdots = n \cdot 2^{n-1}\\
  \binom{n}{1} - 2 \binom{n}{2} + 3 \binom{n}{3} -+ \cdots = 0\\
  2 \cdot 1 \binom{n}{2} + 3 \cdot 2 \binom{n}{3} + 4 \cdot 3 \binom{n}{4} + \cdots = n \cdot (n-1) \cdot 2^{n-2}
  $$

So many formulas, skip at first reading

## Chapter 3 Fluctuations in Coin Tossing and Random Walks

### 1. General Orientation. The Reflection Principle

Consider $n = p + q$ symbols $\epsilon_1, ..., \epsilon_n$, each standing for either +1 or -1; suppose there are $p$ +1s and $q$ -1s. The partial sum $s_k = \epsilon_1 + \cdots + \epsilon_n$ represents the difference between the number of pluses and minuses occurring at the first k places. Then
   $$
   s_k - s_{k-1} = \epsilon_k = \pm 1, \hspace{2em} s_0 = 0, \hspace{2em} s_n = p - q
   $$
Where $k = 1, 2, ..., n$

**Definition.** From a geometric view, let $n > 0 \text{ and } x$ be integers. A path $(s_1, s_2, ..., s_n)$ from the origin to the point $(n, x)$ is a polygonal line whose vertices have abscissas $0, 1, ..., n$ and ordinates $s_0, s_1, ..., s_n$ with $s_n = x$.

We refer to $n$ as the *length* of the path.

**Example.** The ballot theorem [With the assumption that all admissible paths are equally probable]

Suppose that, in a ballot,candidate **P** scores p votes and candidate **Q** scores q votes, where p > q. The probability that throughout the counting there are always more votes for **P** than for **Q** equals (p - q)/(p + q)

**Example.** Galton's rank order test

This test can be abstracted as, the resulting path of length $2r$ joins the origin to the point $(2r, 0)$. And the whole line is non-negative. It can be shown that the probability of this is 1/(r + 1) no matter how long the line is.

**Setup.** Let $A = (a, \alpha)$ and $B = (b, \beta)$ be integral points in the positive quadrant: $b > a \ge 0, \alpha > 0, \beta > 0$. Reflection of $A$ is defined as $A' = (a, -\alpha)$.

**Lemma.** (*Reflection principle*) The number of paths from $A$ to $B$ which touch or cross the x-axis equals the number of all paths from $A'$ to $B$.

**The ballot theorem.** Let $n$ and $x$ be positive integers. There are exactly $\displaystyle\frac{x}{n}N_{n, x} \text{ paths } (s_1, ..., s_n = x)$ from the origin to the point $(n, x)$ such that $s_1 > 0, ..., s_n > 0$, with $N_{n, x} = \displaystyle\binom{p + q}{q} = \displaystyle\binom{p + q}{p}, n = p + q, x = p - q$.

**Proof.** Clearly there exist exactly as many admissible paths as there are paths from the point $(1, 1)$ to $(n, x)$ which neither etouch or cross the x-axis. By the last lemma the number of such paths equals
  $$
  N_{n-1, x-1} - N_{n-1, x+1} = \binom{p+q-1}{p-1} - \binom{p+q-1}{p}
  $$

With $p$ and $q$ defined earlier. A trite calculation show that the right side equals $N_{n, x}(p-q)/(p+q)$ , as asserted.

### 2. Random Walks: Basic Notions and Notations

Each path of length $\rho$ can be interpreted as the outcome of a random walk experiment: there are $2^\rho$ such paths, and we attribute probability of $2^{-\rho}$ to each. (Such random walk is called *symmetric*).

We denote the individual steps generically by $\bold{X}_1, \bold{X}_2, ...$ and the positions of the particle by $\bold{S}_1, \bold{S}_2, ...$. Thus 

$$
S_n = X_1 + \cdots + X_n, \hspace{2em} S_0 = 0
$$

The event "at epoch $n$ the particle is at the point $r$" will be denoted by {$\bold{S}_n = r$}.
The probability of the event "a vist to $r$ at epoch $n$" is denoted by $p_{n, r}$.
The number $N_{n, r}$ of paths for the origin to the point $(n, r)$ is given before, and hence

$$
p_{n, r} = \bold{P}\{\bold{S}_n = r\} = \binom{n}{\displaystyle\frac{n + r}{2}}2^{-n},
$$

Where the binomial coefficient is to be interpreted as 0 unless (n + r)/2 is an integer between 0 and $n$, inclusive.

A *return to the origin* occurs at epoch $2v$ if $\bold{S}_{2v} = 0$. Because of he frequent occurerence of this probability we denote it by $u_{2v}$

$$
u_{2v} = \binom{2v}{v} 2^{-2v} \thicksim \frac{1}{\sqrt{\pi v}}  \text{ by Stirling's formula }
$$

A *First return* occurs at epoch $2v$ if

$$
\bold{S}_1 \ne 0, ..., \bold{S}_{2v-1} \ne 0, \text{ but } \bold{S}_{2v} = 0
$$

The probability for this event will be denoted by $f_{2v}$. By definition $f_0 = 0$.

The probabilies $f_{2n}$ and $u_{2n}$ are related in a noteworthy manner

$$
(2.6) \hspace{4em} u_{2n} = f_2 u_{2n - 2} + f_4 u_{2n - 4} + \cdots + f_{2n} u_0 \hspace{4em} n \ge 1
$$

### 3. The Main Lemma

**Lemma 1.** The probability that no return to the origin occurs up to and including epoch $2n$ is the same as the probability that a return occurs at epoch $2n$. In symbols,

$$
(3.1) \hspace{3em} \bold{P}\{S_1 \ne 0, ..., S_{2n} \ne 0 \} = \bold{P}\{S_{2n} = 0 \} = u_{2n}
$$

When the event on the left occurs either all $S_j$ are positive, or all are negative. The 2 contingencies being equally probable we can restate a previous formula as

$$
\bold{P}\{S_1 > 0, ..., S_{2n} > 0\} = \frac{1}{2} u_{2n}
$$

**Proof.** Considering all possible values of $\bold{S}_{2n}$, it is clear that
  $$
  \bold{P}\{S_1 > 0, ..., S_{2n} > 0\} = \sum _{r = 1} ^\infty \bold{P}\{S_1 > 0, ..., S_{2n-1} > 0, S_{2n} = 2r\}
  $$

(all terms with $r > n$ varnish). By the ballot theorem, the number of paths satisfying the condition on the right side equals $N_{2n-1, 2r -1} - N_{2n-1, 2r+1}$, and so the $r$th term of the sum equals

$$
\frac{1}{2} (p_{2n-1, 2r-1} - p_{2n-1, 2r+1})
$$

The result of the sum reduces to $\frac{1}{2} p_{2n-1, 1}$. It is easy to verify that $p_{2n-1, 1} =  u_{2n}$ and concludes the proof.

The lemma can be restated in several ways; for example

$$
\bold{P}\{S_1 \ge 0, ..., S_{2n} \ge 0\} = u_{2n}
$$

Because a path of length $2n$ with all vertices strictly above the x-axis passes the point $(1, 1)$. Taking $(1, 1)$ as new origin we obtain a path of length $2n - 1$ with all vertices non-negative with respect to the new x-axis, which can be written as

$$
\bold{P}\{S_1 > 0, ..., S_{2n} > 0\} = \frac{1}{2}\bold{P}\{S_1 \ge 0, ..., S_{2n - 1} \ge 0\}
$$

Looking at the right hand side of the above equation, since $S_{2n-1}$ is an odd number, $S_{2n-1} \ge 0$ would imply that also $S_{2n} \ge 0$. Hence RHS can also imply LHS.

Lemma 1 directly leads to an explicit expression for the probability distribution for ***first return to the origin***.First return occurs at epoch $2n$ means the conditions

$$
S_1 \ne 0, ..., S_{2k} \ne 0 \text{ are satisfied for } k = n - 1, \text{ but not for } k = n.
$$

In view of (3.1) this implies

$$
(3.6) \hspace{3em} f_{2n} = u_{2n-2} - u_{2n} \hspace{3em} n = 1, 2, ...
$$

A trite calculation reduces this expression to

$$
(3.7) \hspace{3em} f_{2n} = \frac{1}{2n - 1} u_{2n}
$$

**Lemma 2.** The probability that the first return to the origin occurs at epoch $2n$ is given by (3.6) or (3.7).

### 4. Last Visit and Long Leads

**Theorem 1.** (*Arc sine law for last visits*) The probability that up to and including epoch $2n$ the last visit to the origin occurs at epoch $2k$ is given by

$$
(4.1) \hspace{4em} \alpha_{2k, 2n} = u_{2k}u_{2n-2k}, \hspace{2em} k = 0, 1, ..., n
$$

**Proof.** The conditions are $S_{2n} = 0 \text{ and } S_{2k+1} \ne 0, ..., S_{2n} \ne 0$. The first $2k$ vertices can be chosen in $2^{2k}u_{2k}$ different ways. Taking the point $(2k, 0)$ as new origin and using $(3.1)$ we see that the next $(2n - 2k)$ vertices can be chosen in $2^{2n-2k}u_{2n-2k}$ ways. Finally dividing by $2^{2n}$.

It follows from the theorem that the numbers (4.1) add to unity. The probability distribution which attaches weight $\alpha _{2k, 2n}$ to the point $2k$ is called ***the discrete arc sine distribution of order n***, because the inverse sine function provides excellent numerical approximations. The distribution is symmetric in the sense that $\alpha _{2k, 2n} = \alpha _{2n-2k, 2n}$. And the central term is the smallest.

$$
(4.2) \hspace{4em} f(x) = \frac{1}{\pi \sqrt{x(1-x)}} \hspace{2em} 0 < x < 1
$$

Using Stirling's formula, $u_{2n}$ is close to $1/\sqrt{\pi n}$, except when n is very small. This yields the approximation

$$
\alpha _{2k, 2n} \approx \frac{1}{n} f(x_k) \hspace{2em} x_k = \frac{k}{n}
$$

the error committed is negligible except when $k$ is extremely close to $0$ or $n$. $(4.2)$ can be integrated explicitly and we conclude that for fixed $0 < x < 1$ and n sufficiently large

$$
(4.4) \hspace{4em} \sum _{k < xn} \alpha _{2k, 2n} \approx \frac{2}{\pi} \arcsin \sqrt{x}
$$

Contrary to popular notions, it is quite likely that in a long coin-tossing game one of the players remains practically the whole time on the winning side, the other on the losing side.

**Theorem 2.** (*Discrete arc sine law for sojourn times.*) The probability that in the time interval from $0$ to $2n$ the particle spends $2k$ time units on the positive side adn $2n - 2k$ time units on the negative side equals $\alpha_{2k, 2n}$.

**Corollary.** If $0 < x < 1$, the probability that $xn$ time units are spent on the positive side and $(1 - x)n$ on the negative sides tends to $\frac{2}{\pi} \arcsin \sqrt{x}$ as $n \rightarrow \infty$.

**Proof of Theorem 2.** Consider paths of the fixed length $2n$ and denote by $b_{2k, 2n}$ the probability that exactly $2k$ sides lie above the t-axis. We have to provat that

$$
(4.5) \hspace{4em} b_{2k, 2v} = \alpha_{2k, 2v}
$$

Recall that $(3.4)$ asserts that $b_{2v, 2v} = u_{2v}$ and for reasons of symmetry we have also $b_{0, 2v} = u_{2v}$. It suffices therefore to prove $(4.5)$ for $1 \le k \le v - 1$.
Then assume that exactly $2k$ out of the $2n$ time units are spent on the positive side, and $1 \le k \le v - 1$. In this case a first return to the origin must occur at some epoch $2r < 2n$, and 2 contingencies are possible. First, the $2r$ time units up to the first return may be spent on the positive side. In this case $r \le k \le n - 1$, and the section of the path beyond the vertex $(2r, 0)$ has exactly $2k - 2r$ sdies above the axis. The number of such paths equals $\frac{1}{2} \cdot 2^{2r} f_{2r} \cdot 2^{2n - 2r} b_{2k - 2r, 2n - 2r}$. The other possibility is that the $2r$ time units up to the first return are spent on the negative side. in this case the section beyond the vertex $(2r, 0)$ has exactly $2k$ sides above the axis, whence $n - k \ge k$. The number of such paths equals $\frac{1}{2} \cdot 2^{2r} f_{2r} \cdot 2^{2n - 2r} b_{2k, 2n - 2r}$. Accordingly, when $1 \le k \le n - 1$

$$
(4. 6) \hspace{4em} b_{2k, 2n} = \frac{1}{2} \sum ^k _{r=1}f_{2r} b_{2k - 2r, 2n - 2r} + \frac{1}{2} \sum ^{n - k} _{r = 1} f_{2r} b_{2k, 2n - 2r}
$$

Now we proceed by induciton. The assertion $(4.5)$ is trivially true for $v = 1$, and we assume it to be true for $v = n - 1$. Then $(4.6)$ reduces to

$$
(4.7) \hspace{4em} b_{2k, 2n} = \frac{1}{2} u_{2n - 2k} \sum ^k _{r=1}f_{2r} u_{2k-2r}+\frac{1}{2} u_{2k} \sum ^{n-k} _{r=1}f_{2r}u_{2n-2k-2r}
$$

In view of (2.6) the first sum equals to $u_{2k}$ while the second equals $u_{2n-2k}$. Hence (4.5) is true also for $v = n$.

### *5. Changes of Sign

We revert to random walk terminology. A ***change of sign*** is said to occur at epoch $n$ is $\bold{S}_{n-1}$ and $\bold{S}_{n+1}$ are of opposite signs, that is, if the path crosses the axis. In the case $\bold{S}_n = 0$, and hence $n$ is necessarily an even integer\dots

**Theorem 1.** The probability $\xi _{r, 2n+1}$ that up to epoch $2n + 1$ there occur exactlly $r$ changes of signs equals $2p_{2n+1, 2r+1}$ 

$$
(5.1) \hspace{4em} \xi _{r, 2n+1} = 2\bold{P}\{S_{2n+1} = 2r + 1\} \hspace{2em} r = 0, 1, ...
$$

(Proof is intentionally omitted due to complexity.)

An amazing consequence of the theorem is that the probability $\xi _{r, n}$ of $r$ changes of sign in $n$ trials decreases with $r$:

$$
(5.3) \hspace{4em} \xi _{0, n} \ge \xi _{1, n} > \xi _{2, n} > \cdots
$$

This means that regardless of the number of tosses, the event that the lead never changes is more probable than any preassigned number of changes.

### 7. Maxima and First Passages

We now turn our attention to other interesting consequences of this principle.

Consider paths that remain below the line $x = r$, that is, paths satisfying the condition

$$
(7.1) \hspace{4em} S_0 < r, S_1 < r, ..., S_n < r
$$

We say in this case the *maximum* of the path is $ < r$. Let $A = (n, k)$ be a point with ordinate $k \le r$. A path from $0$ to $A$ touches or crosses the line $x = r$ if it violates the condition $(7.1)$.

**Lemma 1.** Let $k \ge r$. The probability that a path of length $n$ leads to $A = (n, k)$ and has a maximum $\le r$ equals $p_{n, 2r-k} = \bold{P}\{S_n = 2n - k\}$. [I don't quite understand this lemma, maybe there is a typo in the book.]

**Theorem 1.** The probability tha the maximum of a path of length $n$ equals $r \ge 0$ coincides with the positive member of the pair $p_{n, r}$ and $p_{n, r+1}$.

For $r = 0$ and even epochs the assertion reduces to

$$
(7.2) \hspace{4em} \bold{P}\{S_1 \le 0, S_2 \le 0, ..., S_{2n} \le 0\} = u_{2n}
$$

The next notion plays an important role in the general theory of stochastic processes. A ***first passage through the point $r > 0$*** is said to take place at epoch $n$ if

$$
S_1 < r, ..., S_{n-1} < r, \hspace{1em} S_n = r
$$

**Theorem 2.** The probability $\varphi _{r, n}$ that the first passage through r occurs at epoch $n$ is given by

$$
(7.4) \hspace{4em} \varphi _{r, n} = \frac{1}{2} [p_{n-1, r-1} - p_{n-1, r+1}] = \frac{r}{n} \binom{n}{\displaystyle \frac{n+r}{2}} 2^{-n}
$$

[Follwing a few topics are skipped in this first reading]
