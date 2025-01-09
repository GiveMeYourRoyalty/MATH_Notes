# An Introduction to Probability Theory and Its Applications

**Arthur: William Feller**

- [An Introduction to Probability Theory and Its Applications](#an-introduction-to-probability-theory-and-its-applications)
  - [Chapter 9 Random Variables; Expectation](#chapter-9-random-variables-expectation)
    - [1. Random Variables](#1-random-variables)
    - [2. Expectations](#2-expectations)
    - [3. Examples and Applications](#3-examples-and-applications)
    - [4. The Variance](#4-the-variance)
    - [5. Covariance; Variance of a Sum](#5-covariance-variance-of-a-sum)
    - [6. Chebyshev's Inequality](#6-chebyshevs-inequality)
    - [\*7. Kolmogorov's Inequality](#7-kolmogorovs-inequality)
    - [\*8. The Correlation Coefficient](#8-the-correlation-coefficient)
  - [Chapter 10 Law of Large Numbers](#chapter-10-law-of-large-numbers)
    - [1. Identically Distributed Variables](#1-identically-distributed-variables)
    - [3. The Theory of "Fair" Games](#3-the-theory-of-fair-games)
    - [5. Variable Distributions](#5-variable-distributions)
  - [Chapter 11 Integral-Valued Variables. Generating Functions](#chapter-11-integral-valued-variables-generating-functions)
    - [1. Generalities](#1-generalities)
    - [2. Convolutions](#2-convolutions)
    - [3. Equalizations and Waiting Times in Bernoulli Trials](#3-equalizations-and-waiting-times-in-bernoulli-trials)
    - [4. Partial Fraction Expansions](#4-partial-fraction-expansions)
    - [5. Bivariate Generating Functions](#5-bivariate-generating-functions)
    - [\*6. The Continuity Theorem](#6-the-continuity-theorem)

## Chapter 9 Random Variables; Expectation

<br>

### 1. Random Variables

\
A function defined on a sample space is called a **random variable**.

The term random variable is somewhat confusing; random function would be more appropriate.

Let $\bold{X}$ be a random variable and let $x_1, x_2, ...$ be values which it assumes (In the standard mathematical terminology the set of values $x_1, x_2, ...$ should be called *the range of* $\bold{X}$. Unfortunately the statistical literature uses the term range for the difference between the maximum and minimum of $\bold{X}$). In most of what follows the $x_j$ will be integers. The aggregate of all sample points on which $\bold{X}$ assumes the fixed value $x_j$ form the event that $\bold{X} = x_j$. *The function*

$$
(1.1) \hspace{4em} \bold{P}\{\bold{X}=x_j\}=f(x_j) \hspace{2em} (j=1,2,...)
$$

is called the **(probability) distribution of the random variable $\bold{X}$**. Clearly

$$
(1.2) \hspace{4em} f(x_j) \ge 0, \hspace{2em} \sum f(x_j)=1
$$

\
Consider now 2 random variables $\bold{X}$ and $\bold{Y}$ defined on the same sample space, and denotes the values which they assume, respectively, by $x_1, x_2, ...$ and $y_1, y_2, ...$. The aggregate of points in which the 2 conditions $\bold{X}=x_j, \bold{Y}=y_k$ are satisfied forms an event whose probability will be denote by $\bold{P}\{\bold{X}=x_j, \bold{Y}=y_k\}$. *The function*

$$
(1.3) \hspace{4em} \bold{P}\{\bold{X}=x_j, \bold{Y}=y_k\}=p(x_j, y_k) \hspace{2em} (j, k=1,2,...)
$$

is called **the joint probability distribution of $\bold{X}$ and $\bold{Y}$**. Clearly

$$
(1.4) \hspace{4em} p(x_j, y_k) \ge 0, \hspace{1em} \sum _{j, k} p(x_j, y_k) = 1
$$

\
Let the corresponding probability distributions of $\bold{X}, \bold{Y}$ be $\{f(x_j)\}, \{g(y_k)\}$.
For every fixed $j$

$$
(1.5) \hspace{4em} p(x_j, y_1)+p(x_j, y_2)+p(x_j, y_3)+\cdots = \bold{P}\{\bold{X}=x_j\}=f(x_j)
$$

and for every fixed $k$

$$
(1.6) \hspace{4em} p(x_1, y_k)+p(x_2, y_k)+p(x_3, y_k)+\cdots = \bold{P}\{\bold{Y}=y_k\}=g(y_k)
$$

\
The notion of joint distribution carries over to *systems of more than 2 random variables*.

\
With the notation (1.3) the conditional probability of the event $\bold{Y}=y_k$, given that $\bold{X}=x_j$ [with $f(x_j) > 0$], becomes

$$
(1.12) \hspace{4em} \bold{P}\{\bold{Y}=y_k\ |\ \bold{X}=x_j\} = \frac{p(x_j, y_k)}{f(x_j)}
$$

In this way a number is associated with every value of $\bold{X}$, and so (1.12) defines a function of $\bold{X}$. It is called the *conditional distribution of $\bold{Y}$ for given $\bold{X}$*.

\
Note tha the joint distirbution of $\bold{X}$ and $\bold{Y}$ determines the distributions of $\bold{X}$ and $\bold{Y}$, but that we cannot calculate the joint distribution of $\bold{X}$ and $\bold{Y}$ from their marginal distributions. If 2 variables $\bold{X}$ and $\bold{Y}$ have the same distribution, they may or may not be independent.

<br><br>

**Definition.** A random variable $\bold{X}$ is a function defined on a given sample space, that is, an assignment of a real number to each sample points. The probability distribution of $\bold{X}$ is the function defined in (1.1). If 2 random variables $\bold{X}$ and $\bold{Y}$ are defined on the same sample space, their joint distribution is given by (1.3) and assigns probabilities to all combinations$(x_j, y_k)$ of values assumed by $\bold{X}$ and $\bold{Y}$. This notion carries over, in an obvious manner, to any finite set of variables $\bold{X}, \bold{Y}, ..., \bold{W}$ defined on some sample space. These variables are called mutually independent if, for any combination of values $(x, y, ..., w)$ assumed by them

$$
(1.13) \hspace{2em} \bold{P}\{\bold{X}=x,\bold{Y}=y,...,\bold{W}=w\}=\bold{P}\{\bold{X}=x\}\bold{P}\{\bold{Y}=y\}\cdots \bold{P}\{\bold{W}=w\}
$$

<br><br>

### 2. Expectations

\
**Definition.** Let $\bold{X}$ be a random variable assuming the values $x_1, x_2, ...$ with corresponding probabilities $f(x_1), f(x_2), ...$. The mean or expected value of $\bold{X}$ is defined by

$$
(2.1) \hspace{4em} \bold{E(X)}=\sum x_kf(x_k)
$$

provided that the series converges absolutely. In this case we say that $\bold{X}$ has a finite expectation. If $\sum |x_k|f(x_k)$ diverges, then we say that $\bold{X}$ has no finite expectation.

\
**Theorem 1.** Any function $\phi (x)$ defines a new random variable $\phi (\bold{X})$. If $\phi (\bold{X})$ has finite expectation, then

$$
(2.3) \hspace{4em} \bold{E}(\phi (\bold{X}))=\sum \phi (x_k)f(x_k)
$$

the series converes absolutely, if and only if, $\bold{E}(\phi (\bold{X}))$ exists. For any constant $a$ we have $\bold{E}(a\bold{X})=a\bold{E(X)}$.

\
**Theorem 2.** If $\bold{X_1}, \bold{X_2}, ..., \bold{X_n}$ are random variables with expectations, then the expectation of their sum exists and is the sum of their expectations

$$
(2.4) \hspace{4em} \bold{E}(\bold{X_1}+\cdots +\bold{X_n})=\bold{E(X_1)}+\cdots + \bold{E(X_n)}
$$

\
**Theorem 3.** If $\bold{X}$ and $\bold{Y}$ are mutually independent random variables with finite expectations, then their product is a random variable with finite expectation and

$$
(2.6) \hspace{4em} \bold{E(XY)}=\bold{E(X)E(Y)}
$$

By induction, the same multiplication rule holds for any number of mutually independent random variables.

\
It is convenient to have a notation also for the expectation of a conditional probability distribution. If $\bold{X}$ and $\bold{Y}$ are 2 random variables with the joint distribution (1.3), the conditional expectation $\bold{E(Y\ |\ X)}$ of $\bold{Y}$ for given $\bold{X}$ is the function which at the place $x_j$ assumes the value

$$
(2.8) \hspace{4em} \sum _k \bold{P}\{\bold{Y}=y_k\ |\ \bold{X}=x_j\}=\frac{\displaystyle\sum _k y_ p(x_j, y_k)}{f(x_j)}
$$

this definition is meaningful only if the series converges absolutely and $f(x_j) > 0$ for all $j$.

The conditional expectation $\bold{E}\{\bold{Y}\ |\ \bold{X}\}$ is a new random variable. To calculate its expectation we have to multiply (2.8) by $f(x_j)$ and sum over $x_j$. The result is

$$
(2.9) \hspace{4em} \bold{E(E(Y\ |\ X))}=\bold{E(Y)}
$$

<br><br><br>

### 3. Examples and Applications

\
The mean of the binomial distribution is

$$
(3.1) \hspace{4em} \bold{E(S_n)}=np
$$

\
The mean of Poisson distribution

$$
(3.2) \hspace{4em} \bold{E(X)}=\sum kp(k;\lambda)=\lambda \sum p(k-1;\lambda)=\lambda
$$

<br><br>

### 4. The Variance

\
Let $\bold{X}$ be a random variable with distribution $\{f(x_j)\}$, and let $r \ge 0$ be an integer. If the expectation of the random variable $\bold{X}^r$, that is

$$
(4.1) \hspace{4em} \bold{E}(\bold{X}^r)=\sum x_j^rf(x_j)
$$

exists, then it is called the $r$th moment of $\bold{X}$ about the origin. If the series does not converge absolutely, we say that the $r$th moment does not exist. Since $|\bold{X}|^{r-1} \le |\bold{X}|^r+1$, it follows that whenever the $r$th moment exists so does the $(r-1)$st, and hence all preceding moments.

\
**Definition.** Let $\bold{X}$ be a random vairable with second moment $\bold{E}(\bold{X}^2)$ and let $\mu=\bold{E(X)}$ be its mean. We define a number called the variance of $\bold{X}$ by

$$
(4.4) \hspace{4em} \text{Var}(\bold{X})=\bold{E}((\bold{X}-\mu)^2)=\bold{E}(\bold{X}^2)-\mu ^2
$$

Its positive square root (or zero) is called the standard deviation of $\bold{X}$.

\
$$
(4.5) \hspace{4em} \text{Var}(a\bold{X}+b)=a^2\text{Var}(\bold{X})
$$

\
In general, if $\bold{X}$ has mean $\mu$ and variance $\sigma ^2$, then $\bold{X}-\mu$ has mean zero and variance $\sigma ^2$, and hence the vairable

$$
(4.6) \hspace{4em} \bold{X}^*=(\bold{X}-\mu)/\sigma
$$

has mean 0 and variance 1. It is called **the normalized variable corresponding to $\bold{X}$**.

<br><br>

### 5. Covariance; Variance of a Sum

\
**Definition.** The covariance of $\bold{X}$ and $\bold{Y}$ is defined by

$$
(5.4.) \hspace{4em} \text{Cov}(\bold{X}, \bold{Y})=\bold{E}((\bold{X}-\mu _x)(\bold{Y}-\mu _y))=\bold{E(XY)}-\mu _x \mu _y
$$

This definition is meaningful whenever $\bold{X}$ and $\bold{Y}$ have finite variances.

\
**Theorem 1.** If $\bold{X}$ and $\bold{Y}$ are independent, then $\text{Cov}(\bold{X,Y})=0$.

Note that *the converse is not true*.

\
**Theorem 2.** If $\bold{X}_1, ..., \bold{X}_n$ are random variables with finite variances $\sigma _1^2, ..., \sigma _n^2$, and $\bold{S}_n=\bold{X}_1+\cdots+\bold{X}_n$, then

$$
(5.5) \hspace{4em} \text{Var}(\bold{S}_n)=\sum _{k=1} ^n \sigma _k ^2 + 2\sum_{j,k} \text{Cov}(\bold{X}_i, \bold{X}_k)
$$

the last sum extending over each of the $\displaystyle\binom{n}{2}$ pairs $(\bold{X}_j,\bold{X}_k)$ with $j < k$.

In particular, if the $\bold{X}_j$ are mutually independent,

$$
(5.6) \hspace{4em} \text{Var}(\bold{S}_n)=\sum _{k=1} ^n \sigma _k ^2
$$

\
**Example.** *Sampling without replacement*
Suppose that a population consists of $b$ black and $g$ green elements, and that a random sample of size $r$ is taken (without repetitions). The number $S_k$ of black elements in the sample is a random vairable with the *hypergeometric distribution* from which the mean and variance can be obtained by direct computation. However, the following method is preferable. Define the random variable $\bold{X}_k$ to assume the values $1$ or $0$ according as the $k$th element in the sample is or is not black $(k \le r)$. For reasons of symmetry the probability that $\bold{X}_k = 1$ is $b/(b+g)$. and hence

$$
(5.12) \hspace{4em} \bold{E}(\bold{X}_k)=\frac{b}{b+g}, \hspace{1em} \text{Var}(\bold{X}_k)=\frac{bg}{(b+g)^2}
$$

Next, if $j \ne k$, then $\bold{X}_j \bold{X}_k=1$ if the $j$th and $k$th elements of the sample are black, and otherwise $\bold{X}_j \bold{X}_k=0$. The probability of $\bold{X}_j \bold{X}_k=1$ is $b(b-1)/(b+g)(b+g-1)$, and therefore

$$
\begin{align*}
  (5.13) \hspace{4em} \bold{E}(\bold{X}_j \bold{X}_k)&=\frac{b(b-1)}{(b+g)(b+g-1)}\\
  \text{Cov}(\bold{X}_j \bold{X}_k)&=\frac{-bg}{(b+g)^2 (b+g-1)}
\end{align*}
$$

Thus

$$
(5.14) \hspace{4em} \bold{E}(\bold{S}_r)=\frac{rb}{b+g}, \hspace{1em} \text{Var}(\bold{S}_r)=\frac{rbg}{(b+g)^2}\left\{1-\frac{r-1}{b+g-1}\right\}
$$

In sampling with replacement we would have the same mean, but the variance would be slightly larger, namely, $rgb/(b+g)^2$.

<br><br>

### 6. Chebyshev's Inequality

\
We see that a small variance indicates that large deviations from the mean are imporbable. This statement is made more precisely by Chebyshev's inequality, which is an exceedingly useful tool. It presupposes the existence of a second moment.

\
**Theorem.** For any $t > 0$

$$
(6.1) \hspace{4em} \bold{P}\{|\bold{X}| \ge t\} \le t^{-2}\bold{E}(\bold{X}^2)
$$

In particular, if $\bold{E(X)}=\mu$ then

$$
(6.2) \hspace{4em} \bold{P}\{|\bold{X}-\mu| \ge t\} < t_{-2}\text{Var}(\bold{X})
$$

\
**Proof.** The second inequality is obtained by applying the first to the variable $\bold{X}-\mu$. Using the notations of section 4 we have

$$
(6.3) \hspace{4em} \bold{P}\{|\bold{X}| \ge t\}=\sum _{|x_j|\ge t} f(x_j) \le t^{-2}\sum _{|x_j| \ge t} x_j^2 f(x_j)
$$

the sums extending over those $x_j$ that exceed $t$ in absolute value. The last sum is $\le \bold{E}(\bold{X}^2)$, and so (6.1) is true.

\
Chebyshev's inequality must be regarded as a theoooretical tool rather than a practical method of estimation. Its importance is due to its universality, but no statement of great generality can be expected to yield sharp results in individual cases.

<br><br>

### *7. Kolmogorov's Inequality

\
Let $\bold{X}_1, ..., \bold{X}_n$ be mutually independent variables with expectations $\mu _k=\bold{E}(\bold{X}_k)$ and variances $\sigma _k^2$. Put

$$
\begin{align*}
  (7.1) \hspace{8em} \bold{S}_k&=\bold{X}_1+\cdots +\bold{X}_k\\
  (7.2) \hspace{4em} m_k=\bold{E}(\bold{S}_k)&=\mu_1+\cdots+\mu_k\\
  s_k^2=\text{Var}(\bold{S}_k)&=\sigma_1^2+\cdots+\sigma_k^2
\end{align*}
$$

For every $t > 0$ the probability of the simultaneous realization of the n inequalities

$$
(7.3) \hspace{4em} |\bold{S}_k-m_k| < ts_n, \hspace{2em} k=1,2,..n
$$
is at least $1-t^{-2}$.

For $n=1$, this theorem reduces to Chebyshev's inequality. For $n > 1$ Chebyshev's inequality gives the same bound for the probability of the single relation $|\bold{S}_n-m_n| < ts_n$, so that Kolmogorov's inequality is considerably stronger.

[Proof is omitted]

<br><br>

### *8. The Correlation Coefficient

\
Let $\bold{X}$ and $\bold{Y}$ be any 2 random variables with means $\mu_x$ and $\mu_y$ and positive variances $\sigma_x^2$ and $\sigma_y^2$. We introduce the corresponding normalized vairables $\bold{X}^*$ and $\bold{Y}^*$ defined by (4.6). Their covariance is called **the correlation coefficient of $\bold{X}$ and $\bold{Y}$** and is denoted by $\rho(\bold{X}, \bold{Y})$. Thus

$$
(8.1) \hspace{4em} \rho(\bold{X}, \bold{Y})=\text{Cov}(\bold{X}^*, \bold{Y}^*)=\frac{\text{Cov}(\bold{X}^*, \bold{Y}^*)}{\sigma_x\sigma_y}
$$

Clearly this correlation coefficient is independent of the origins and units of measurements, that is, for any constants $a_1, a_2, b_1, b_2$, with $a_1 > 0, a_2 > 0$, we have $\rho(a_1\bold{X}+b_1, a_2\bold{Y}+b_2)=\rho(\bold{X}, \bold{Y})$

\
**Theorem.** We have always $|\rho(\bold{X}, \bold{Y})| \le 1$; furthermore, $\rho(\bold{X}, \bold{Y})=\pm 1$ only if there exist constants $a$ and $b$ such that $\bold{Y}=a\bold{X}+b$, except, perhaps, for values of $\bold{X}$ with zero probability.\

<br><br><br>

## Chapter 10 Law of Large Numbers

<br>

### 1. Identically Distributed Variables

\
Here we discuss at least some cases of the law off large numbers in order to reveal a new aspect of the expectation of a random variable, but the general limit theorems for Bernoulli trials cannot be treated in this volume.

\
The connection between Bernoulli trials and the theory of random variables becomes clearer when we consider the dependence of the number $\bold{S}_n$ of successes on the number $n$ of trials. With each trial, $\bold{S}_n$ increases by $1$ or $0$

$$
(1.1) \hskip{4em} \bold{S}_n=\bold{X}_1+\cdots+\bold{X}_n
$$

where the random variable $\bold{X}_k$ equals $1$ if the $k$th trial results in success and zero otherwise (assumes the values $1$ and $0$ with probabilities $p$ and $q$).

<br><br>

**Law of Large Numbers.** Let $\{\bold{X}_k\}$ be a sequence of mutually independent random variables with a common distribution. If the expectation $\mu=\bold{E(\bold{X}_k)}$ exists, then for every $\epsilon > 0$ as $n \rightarrow \infty$

$$
(1.2) \hspace{4em} \mathbf{P}\left\{ \left| \frac{\bold{X}_1+\cdots+\bold{X}_n}{n} - \mu \right| > \epsilon \right\} \rightarrow 0
$$

in words, the probability that the average $\mathbf{S}_n/n$ will differ from the expectation by less than an arbitrarily prescribed $\epsilon$ tends to one.

<br><br>

There exists a much more precise result which generalizes the DeMoivre-Laplace limit theorem for Bernoulli trials, (but has to introduce the restriction that the variance $\text{Var}(\mathbf{X}_k)$ should be finite), namely

<br>

**Central Limit Theorem.** Let $\{\mathbf{X}_k\}$ be a sequence of mutually independent random variables with a common distribution. Suppose that $\mu=\bold{E}(\bold{X}_k)$ and $\sigma^2=\text{Var}(\bold{X}_k)$ exist and let $\mathbf{S}_n=\mathbf{X}_1+\cdots+\mathbf{X_n}$. Then for every fixed $\beta$

$$
(1.3) \hspace{4em} \bold{P}\left\{\frac{\mathbf{S}_n-n\mu}{\sigma \sqrt{n}} < \beta \right\}\rightarrow \mathfrak{N}(\beta)
$$

where $\mathfrak{N}(x)$ is the normal distribution.The theorem is only a special case of a much more general theorem whose formulation and proof are deferred to the second volumee. Here we note that (1.3) is stronger thatn (1.2), since it gives an estimate for the probability that the discrepancy $|n^{-1}\mathbf{S}_n-\mu|$ is larger than $\sigma/\sqrt{n}$. On the other hand, the law of large numbers (1.2) holds even when the random variables $\mathbf{X}_k$ have no finite variance so that it is more general than the central limit theorem.

<br><br>

### 3. The Theory of "Fair" Games

\
First, we shall assume that our gambler possesses an *unlimited capital* so that no loss can force a termination of the game. (Dropping this assumption leads to the problem of the gambler's ruin. It is of importance of Wald's sequential analysis andd in the theory of stochastic processes.) Second, we shall assume that the gambler *does not have the privilege of optional stopping; the number $n$ of trials must be fixed in advance* independently of the development of the game.

The random variable $\bold{X}_k$ will be interpreted as the (positive or negative) gain at the $k$th trial of a player who keeps playing the same type of game of chance. The sum $\bold{S}_n=\bold{X}_1+\cdots+\bold{X}_n$ is the accumulated gain in $n$ independent trials. If the player pays for each trial an entrance fee $\mu'$ (not necessariliy positive), then $n\mu'$ represents the accumulated entrance fees, and $\bold{S}_n-n\mu'$ the *accumulaated net gain*. The law of large numbers applies when $\mu=\bold{E}(\bold{X}_k)$ exists. It says roughly for sufficiently large $n$ the difference $\bold{S}_n-n\mu$ is likely to be small in comparison to $n$. Therefore, if the entrance fee $\mu'$ is smaller thatn $\mu$, then, for large $n$, the player is likely to have a positive gain of the order of magnitude $n(\mu-\mu')$.

<br><br>

### 5. Variable Distributions

\
Up to now, we hvae considered only variable $\bold{X}_k$ having the same distribution. This situation corresponds to a repetition of the same game of chance, but it is more interesting to see what happens if the type of game changes at each step.

Imagine that an infinite sequence of probability distributions is given so that for each $n$ we have $n$ mutually independent variables $\bold{X}_1, ..., \bold{X}_n$ with the prescribed distributions. We assume that the means and variances exist and put

$$
(5.1) \hspace{4em} \mu_k=\bold{E}(\bold{X}_k), \hspace{1em} \sigma_k^2=\text{Var}(\bold{X}_k)
$$

The sum $\bold{S}_n$ has mean $m_n$ and variance $s_n^2$ given by

$$
(5.2) \hspace{4em} m_n=\mu_1+\cdots+\mu_n, \hspace{1em} s_n^2=\sigma_1^2+\cdots+\sigma_n^2
$$

*The (weak) law of large numbers is said to hold for the sequence* $\{\bold{X}_k\}$ *if for every* $\epsilon > 0$

$$
(5.3) \hspace{4em} \bold{P}\left\{\frac{|\bold{S}_n-m_n|}{n}>\epsilon\right\}\rightarrow0
$$

*The sequence* $\{\bold{X}_k\}$ *is said to obey the central limit theorem if for every fixed* $\alpha < \beta$

$$
(5.4) \hspace{4em} \bold{P}\left\{\alpha<\frac{\bold{S}_n-m_n}{s_n}<\beta\right\}\rightarrow\mathfrak{N}(\beta)-\mathfrak{N}(\alpha)
$$

[Following contents are omitted at first reading]

<br><br>

## Chapter 11 Integral-Valued Variables. Generating Functions

<br>

### 1. Generalities

<br>

**Definition.** Let $a_0, a_1, a_2, ...$ be asequence of real numbers. If

$$
(1.1) \hspace{4em} A(s)=a_0+a_1s+a_2s^2+\cdots
$$

converges in some interval $-s_0<s<s_0$, then $A(s)$ is called the generating function of the sequence $\{a_j\}$

\
Let $\bold{X}$ be a random variable assuming the values $0,1,2,...$. It will be convenient to have a notation both for the distribution of $\bold{X}$ and for its tails, and we shall write

$$
(1.2) \hspace{4em} \bold{P}(\bold{X}=j)=p_j, \hspace{1em} \bold{P}{\bold{X}>j}=q_j
$$

Then

$$
(1.3) \hspace{4em} q_k=p_{k+1}+p_{k+2}+\cdots \hspace{2em} k\ge0
$$

The generating functions of the sequences $\{p_j\}$ and $\{q_j\}$ are

$$
(1.4) \hspace{4em} P(s)=p_0+p_1s+p_2s^2+p_3s^3+\cdots\\
(1.5) \hspace{4em} Q(S)=q_0+q_1s+q_2s^2+q_3s^3+\cdots
$$

\
**Theorem 1.** For $-1<s<1$

$$
(1.6) \hspace{4em} Q(s)=\frac{1-P(s)}{1-s}
$$

**Proof.** (It is not easy to derive the RHS from $Q(s)$ directly.) The coefficient of $s^n$ in $(1-s)\cdot Q(s)$ equals $q_n-q_{n-1}=-p_n$ when $n\ge1$, and equals $q_0=p_1+p_2+\cdots=1-p_0$ when $n=0$. Therefore LHS = RHS.

\
Next we examine the derivative

$$
(1.7) \hspace{4em} P'(s)=\sum _{k=1}^\infty kp_ks^{k-1}
$$

The series converges at least for $1 < s < 1$. For $s=1$, RHS reduces formally to $\sum kp_k=\bold{E}(\bold{X})$. Whenever this expectation exists, the derivative $P'(s)$ will be continuous in the closed interval $-1 \le s \le 1$. If $\sum k p_k$ diverges, then $P'(x)\rightarrow \infty$ as $s\rightarrow 1$. In this case we say that $\bold{X}$ *has an infinite expectation* and write $P'(1)=\bold{E}(\bold{X})=\infty$. (All quantities being positive, there is no danger in the use of the symbol $\infty$.) Applying the mean value theorem to the numerator in (1.6), we see that $Q(s)=P'(\sigma)$ where $\sigma$ is a point lying between $s$ and $1$. Since both functions are monotone this implies that $P(s)$ and $Q(s)$ have the same finite or infinite limit which we denote by $P(1)$ or $Q(1)$. This proves

\
**Theorem 2.** The expectation $\bold{E}(\bold{X})$ satisfies the relations

$$
(1.8) \hspace{4em} \bold{E}(\bold{X})=\sum _{j=1}^\infty jp_j=\sum _{k=0}^\infty q_k
$$

or in terms of generating functions

$$
(1.9) \hspace{4em} \bold{E}(\bold{X})=P'(1)=Q(1)
$$

By differentiation of (1.7) and of the relation $P'(s)=Q(s)-(1-s)Q'(s)$, we find in the same way

$$
(1.10) \hspace{4em} \bold{E}(\bold{X}(\bold{X}-1))=\sum k(k-1)p_k=P''(1)=2Q'(1)
$$

To obtain the variance of $\bold{X}$ we have to add $\bold{E(X)}-\bold{E^2(X)}$ which leads us to

\
**Theorem 3.** We have

$$
\begin{align*}
  (1.11) \hspace{4em} \text{Var}(\bold{X})&=P''(1)+P'(1)-P'^2(1)\\
  &=2Q'(1)+Q(1)-Q^2(1)
\end{align*}
$$

In the case of an infinite variance $P''(s) \rightarrow \infty$ as $s\rightarrow 1$.

<br><br>

### 2. Convolutions

\
If a random variable $\bold{X}$ assumes only non-negative integral valuess, then $s^\bold{X}$ is a well-defined new random variable, and the generating function of the distribution of $\bold{X}$ can be written in the compact form $\bold{S}(s^\bold{X})$. If $\bold{X}$ and $\bold{Y}$ are independent, so are $s^\bold{X}$ and $s^\bold{Y}$, and hence $\bold{E}(s^{\bold{X}+\bold{Y}})=\bold{E}(s^\bold{X})\bold{E}(s^\bold{Y})$. We proceed to give a different proof for this important result because it will lead us to a useful generalization.

\
$$
(2.1) \hspace{4em} c_r=a_0b_r+a_1b_{r-1}+a_2b_{r-2}+\cdots+a_{r-1}b_1+a_rb_0
$$

\
**Definition.** Let $\{a_k\}$ and $\{b_k\}$ be any 2 numerical sequences (not necessariliy probability distribution). The new sequencee $\{c_r\}$ defined by (2.1) is called the convolution of $\{a_k\}$ and $\{b_k\}$ and will be denoted by

$$
(2.2) \hspace{4em} \{c_k\}=\{a_k\}*\{b_k\}
$$

\
**Theorem.** If $\{a_k\}$ and $\{b_k\}$ are sequences with generating functions $A(s)$ and $B(s)$, and $\{c_k\}$ is their convolution, then the generating function $C(s)=\sum c_ks^k$ is the product

$$
(2.3) \hspace{4em} C(s)=A(s)B(s)
$$

If $\bold{X}$ and $\bold{Y}$ are non-negative integral-valued mutually independent random variables with generating functions $A(s)$ and $B(s)$, then their sum $\bold{X+Y}$ has the generating function $A(s)B(s)$.

\
**Property.** The convolution is an associative and commutative operation (exactly as the summation of random variables). The order in which the convolution are performed is immaterial ($\{a_k\}*\{b_k\}*\{c_k\}=\{c_k\}*\{b_k\}*\{a_k\}$, etc.).

\
$$
(2.5) \hspace{4em} \{a_j\}^{n*}=\{a_j\}^{(n-1)*}*\{a_j\}
$$

In words, $\{a_j\}^{n*}$ is the sequence of numbers whose generarting funtion is $A^n(s)$. $\{a_j\}^{0*}$ is defined as the sequence whose generating function is $A^0(s)=1$, that is, the sequence $(1,0,0,0,...)$.

<br><br>

### 3. Equalizations and Waiting Times in Bernoulli Trials

\
In the following we consider Bernoulli trials with probability $p$ for success. We put $\bold{X}_k= +1$ if the $k$th resulits in success, and $\bold{X}_k=-1$ otherwise.

As usual we put

$$
(3.1) \hspace{4em} \bold{S}_n=\bold{X}_1+\cdots+\bold{X_n}, \hspace{1em} \bold{S}_0=0
$$

**(a) Waiting Time for a Gain.** The event

$$
(3.2) \hspace{4em} \bold{S}_1 \le 0, ..., \bold{S}_{n-1} \le 0, \hspace{1em} \bold{S}_n=1
$$

signifies in gambling terminology that the $n$th trial is the first to render Peter's (the player) accumulated gain positive.

[Following contents are skipped.]

<br><br>

### 4. Partial Fraction Expansions

\
Given a generating function $P(s)=\sum p_ks^k$ the coefficients $p_k$ can be obtained by differentiations from the obvious formula $p_k=P^{(k)}(0)/k!$. However, in practice it may be impossible to obtain explicit expression and, anyhow, such expressions are frequently so complicated that reasonable approximations are preferable. The most common method for obtaining such approximatiosn is based on partial fraction expansions. We shall limit our exposition to teh simple case of *rational functions*.

\
Suppose that the generating function is of the form

$$
(4.1) \hspace{4em} P(s)=\frac{U(s)}{V(s)}
$$

where $U$ and $V$ are polynomials without common roots. For simplicity let us first assume that the degree of $U$ is lower than the degree of $V$, say $m$. Then the equation $V(s)=0$ has $m$ distinct (real or imaginary) roots $s_1, s_2, ..., s_m$. Then

$$
(4.2) \hspace{4em} V(s)=(s-s_1)(s-s_2)\cdots(s-s_m)
$$

and it is known form algebra that $P(s)$ can be decomposed into *partial fractions*

$$
(4.3) \hspace{4em} P(s)=\frac{\rho_1}{s_1-s}+\frac{\rho_2}{s_2-s}+\cdots+\frac{\rho_m}{s_m-s}
$$

where $\rho_1, \rho_2, ..., \rho_m$ are constants. To find $\rho_1$ multiply (4.3) by $s_1-s$; as $s\rightarrow s_1$ the product $(s_1-s)P(s)$ tends to $\rho_1$. From (4.1) and (4.2) we get

$$
(4.4) \hspace{4em} (s_1-s)P(s)=\frac{-U(s)}{(s-s_2)(s-s_3)\cdots(s-s_m)}
$$

As $s \rightarrow s_1$ the numerator tends to $-U(s_1)$ and the denominator is the same as $V'(s_1)$. Thus $\rho_1=-U(s_1)/V'(s_1)$. The same argument applies to all roots, so that for $k \le m$

$$
(4.5) \hspace{4em} \rho_k=\frac{-U(s_k)}{V'(s_k)}
$$

Given the $\rho_k$, we can easiliy derive an exact expression for the expression for the coefficient of $s^n$ in $P(s)$. Write

$$
(4.6) \hspace{4em} \frac{1}{s_k-s}=\frac{1}{s_k}\cdot\frac{1}{1-s/s_k}
$$

For $|s|<|s_k|$ we expand the last fraction into a geometric series

$$
(4.7) \hspace{4em} \frac{1}{1-s/s_k}=1+\frac{s}{s_k}+\left(\frac{s}{s_k}\right)^2+\left(\frac{s}{s_k}\right)^3+\cdots
$$

Introducing these expressions into (4.3), we find for the *coefficient $p_n$ of $s^n$*

$$
(4.8) \hspace{4em} p_n=\frac{\rho_1}{s_1^{n+1}}+\frac{\rho_2}{s_2^{n+1}}+\cdots+\frac{\rho_m}{s_m^{n+1}}
$$

Thus to get $p_n$ we have first to find the roots $s_1, ..., s_m$ of the denominator and then to determine the coefficients $\rho_1, ..., \rho_m$ from (4.5).

However, the labor involved in calculating all $m$ roots is usually prohibitive, and therefore formula (4.8) is primarily of theoretcal interest. Fortunately, if $s_1$ is a root which is *smaller*  in absolute value than all other roots, then the first term in (4.8) almost provides a satisfactory approximation.

In other words, *if $s_1$ is a root of $V(s)=0$ which is smaller in absolute value than all other roots, then, as $n \rightarrow \infty$*,

$$
(4.9) \hspace{4em} p_n \sim \frac{\rho_1}{s_1^{n+1}}
$$

The main advantage of (4.9) lies in the fact that it requires the computation of only one root of an algebraic equation.

<br>

**Theorem.** If $P(s)$ is a rational function with a simple root $s_1$ of the senominator whhich is smaller in absolute value than all other roots, then the coefficient $p_n$ of $s^n$ is given asymptotically by $p_n \sim \rho_1s_1^{-(n+1)}$, where $\rho_1$ is defined in (4.5).

[S similiar asymptotic expansion exists also in the case where $s_1$ is a multiple root.]

<br><br>

### 5. Bivariate Generating Functions

\
For a pair of integral-valued random variables $\bold{X, Y}$ with joint distributions of the form

$$
(5.1) \hspace{4em} \bold{P}\{\bold{X}=j, \bold{Y}=k\}=p_{jk}, \hspace{1em} j, k=0,1,...
$$

we define a generating function depending on 2 variables

$$
(5.2) \hspace{4em} P(s_1, s_2)=\sum _{j,k} p_{jk}s_1^js_2^k
$$

Such generating functions will be called bivariate for short.

\
The considerations of the first 2 sections apply without essential modifications, and it will suffice to point out 3 properties evident from (5.2):
  1. The generating function of the marginal distributions $\bold{P}\{\bold{X}=j\}$ and $\bold{P}\{\bold{Y}=k\}$ are $A(s)=P(s,1)$ and $B(s)=P(1,s)$.
  2. The generating function of $\bold{X+Y}$ is $p(s,s)$.
  3. The variables $\bold{X}$ and $\bold{Y}$ are independent if, and only if, $P(s_1, s_2)=A(s_1)B(s_2)$ for all $s_1, s_2$.

<br><br>

### *6. The Continuity Theorem

