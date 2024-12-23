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

**Refinement**. $\sqrt{2 \pi} n^{n + \frac{1}{2}} e^{-n} \cdot e^{(12n+1)^{-1}} < n! < \sqrt{2 \pi} n^{n + \frac{1}{2}} e^{-n} \cdot e^{(12n)^{-1}} $