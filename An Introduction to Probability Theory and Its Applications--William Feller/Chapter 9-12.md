# An Introduction to Probability Theory and Its Applications

**Arthur: William Feller**

- [An Introduction to Probability Theory and Its Applications](#an-introduction-to-probability-theory-and-its-applications)
  - [Chapter 9 Random Variables; Expectation](#chapter-9-random-variables-expectation)
    - [1. Random Variables](#1-random-variables)
    - [2. Expectations](#2-expectations)
    - [3. Examples and Applications](#3-examples-and-applications)
    - [4. The Variance](#4-the-variance)
    - [5. Covariance; Variance of A Sum](#5-covariance-variance-of-a-sum)
    - [6. Chebyshev's Inequality](#6-chebyshevs-inequality)
    - [\*7. Kolmogorov's Inequality](#7-kolmogorovs-inequality)
    - [\*8. The Correlation Coefficient](#8-the-correlation-coefficient)
  - [Chapter 10 Law of Large Numbers](#chapter-10-law-of-large-numbers)
    - [1. Identically Distributed Variables](#1-identically-distributed-variables)

## Chapter 9 Random Variables; Expectation

<br>

### 1. Random Variables

\
A function defined on a sample space is called a **random variable**.

The term random variable is somewhat confusing; random function would be more appropriate.

Let $\bold{X}$ be a random variable and let $x_1, x_2, ...$ be values which it assumes (In the standard mathematical terminology the set of values $x_1, x_2, ...$ should be called *the range of* $\bold{X}$. unfortunately the statistical literature uses the term range for the difference between the maximum and minimum of $X$). in most of what follows the $x_j$ will be integers. The aggregate of all sample points on which $X$ assumes the fixed value $x_j$ form the event that $\bold{X} = x_j$. *The function*

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
Note tha tthe joint distirbution of $\bold{X}$ and $\bold{Y}$ determines the distributions of $\bold{X}$ and $\bold{Y}$, but that we cannot calculate the joint distribution of $\bold{X}$ and $\bold{Y}$ from their marginal distributions. If 2 variables $\bold{X}$ and $\bold{Y}$ have the same distribution, they may or may not be independent.

<br><br>

**Definition.** A random variable $\bold{X}$ is a function defined on a given sample space, that is, an assignment of a real number to each sample points. The probability distribution of $\bold{X}$ is the function defined in (1.1). If 2 random variables $\bold{X}$ and $\bold{Y}$ are defined on the same sample space, their joint distribution is given by (1.3) and assigns probabilities to all combinations$(x_j, y_k)$ of values assumed by $\bold{X}$ and $\bold{Y}$. This notion carries over, in an obvious manner, to any finite set of variables $\bold{X}, \bold{Y}, ..., \bold{W}$ defined on some sample space. These variables are called mutually independent if, for any cmobination of values $(x, y, ..., w)$ assumed by them

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

The condition expectation $\bold{E}\{Y\ |\ X\}$ is a new random variable. To calculate its expectation we have to multiply (2.8) by $f(x_j)$ and sum over $x_j$. The result is

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

### 5. Covariance; Variance of A Sum

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
