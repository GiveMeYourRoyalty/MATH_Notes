# An Introduction to Probability Theory and Its Applications

**Arthur: William Feller**

- [An Introduction to Probability Theory and Its Applications](#an-introduction-to-probability-theory-and-its-applications)
  - [Chapter 4 Combination of Events](#chapter-4-combination-of-events)
    - [1. Union of Events](#1-union-of-events)
    - [2. Application to the Classical Occupancy Problem](#2-application-to-the-classical-occupancy-problem)
    - [3. The Realization of $m$ among $N$ events](#3-the-realization-of-m-among-n-events)
    - [4. Application to Matching and Guessing](#4-application-to-matching-and-guessing)
  - [Chapter 5 Conditional Probability. Stochastic Independece](#chapter-5-conditional-probability-stochastic-independece)
    - [1. Condtional Probability](#1-condtional-probability)
    - [2. Probabilities Defined by Conditional Probabilities. Urn Models](#2-probabilities-defined-by-conditional-probabilities-urn-models)
    - [3. Stochastic Independence](#3-stochastic-independence)
    - [4. Product Spaces. Independent Trials](#4-product-spaces-independent-trials)
  - [Chapter 6 The Binomial and the Poisson Distributions](#chapter-6-the-binomial-and-the-poisson-distributions)
    - [1. Bernoulli Trials](#1-bernoulli-trials)
    - [2. The Binomial Distribution](#2-the-binomial-distribution)
    - [3. The Central Term and the Tails](#3-the-central-term-and-the-tails)
    - [4. The Law of Large Numbers](#4-the-law-of-large-numbers)

## Chapter 4 Combination of Events

<br>

### 1. Union of Events

\
**Notation.** We shall denote the probabilities $A_i, A_j, \text{ and } A_k$, etc. occurring simultaneously by the letter $p$ with appropriate subscripts.

$$
(1.2) \hspace{4em} p_{ijk} = \bold{P}\{A_i A_j A_k\}, ...
$$

The order of the subscripts is irrelevant, but for uniqueness we shall always *write the subscripts in increasing order*. Two subscripts are never equal.

**Notation.** For the sum of all $p$'s with $r$ subscripts we shall write $S_r$ that is,

$$
(1.3) \hspace{4em} S_1 = \sum p_i, \hspace{1em} S_2 = \sum p_{ij}, \hspace{1em} S_3 = \sum p_{ijk}, ...
$$

Here $i < j < k < \cdots \le N$, so that in the sums each combination appears once and only once; hence $S_r$ has $\binom{N}{r}$ terms.

**Theorem.** The probability $P_1$ of the realization of at least one among the event $A_1, A_2, ..., A_N$ is given by

$$
(1.5) \hspace{4em} P_1 = S_1 - S_2 + S_3 - S_4 + - \cdots \pm S_N
$$

<br><br><br>

### 2. Application to the Classical Occupancy Problem

\
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

Now we proceed to consider the limit form of the formular (2.4). The relation between $r$ and $n$ is, in principle, arbitrary, but in practice, onlys the intermediate case of the ratio $\frac{r}{n}$ is of our interest.

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

<br><br><br>

### 3. The Realization of $m$ among $N$ events

\
The theorem of section 1 can be strengthened as follows

**Theorem.** For any integer $m$ with $1 \le m \le N$ the probability $p_{[m]}$ that exactly $m$ among the $N$ events $A_1, ..., A_N$ occur simultaneously is given by

$$
(3.1) \hspace{4em} P_{[m]} = S_m - \binom{m+1}{m}S_{m+1} +\binom{m+2}{m} S_{m+2} -+ \cdots \pm \binom{N}{m}S_N
$$

(3.1) gives the correct value for $m = 0$ provided we put $S_0 = 1$.

<br><br><br>

### 4. Application to Matching and Guessing

\
Recall that, from example (1.b), the matching of 2 decks of cards, $S_k = 1/k!$.

In a random matching of 2 equivalent decks of $N$ distinct cards the probability $P_{[m]}$ of having exactly $m$ matches is given by

$$
\begin{align*}
P_{[0]} &= 1-1+\frac{1}{2!}-\frac{1}{3!}+- \cdots \pm \frac{1}{(N-2)!} \mp \frac{1}{(N-1)!} \pm \frac{1}{N!}\\
P_{[1]} &= 1-1+\frac{1}{2!}-\frac{1}{3!}+- \cdots \pm \frac{1}{(N-2)!} \mp \frac{1}{(N-1)!}\\
p_{[2]} &= \frac{1}{2!}\{1-1+\frac{1}{2!}-\frac{1}{3!}+- \cdots \pm \frac{1}{(N-2)!}\}\\
p_{[3]} &= \frac{1}{3!}\{1-1+\frac{1}{2!}-\frac{1}{3!}+- \cdots \pm \frac{1}{(N-3)!}\}\\
\cdots\\
p_{[N-2]} &= \frac{1}{(N-2)!}\{1-1+\frac{1}{2!}\}\\
p_{[N-1]} &= \frac{1}{(N-1)!}\{1-1\} = 0 \hspace{1em} p_{[N]}=\frac{1}{N!}
\end{align*}
$$

For larger $N$ we have approximately

$$
(4.2) \hspace{4em} p_{[m]}\approx\frac{e^{-1}}{m!}
$$

THe limiting form

$$
(4.3) \hspace{4em} p_m=\frac{e^{-1}}{m!}
$$

Note that (4.3) represents the special case $\lambda = 1$ of the ***Poisson distribution*** (2.11).

<br><br><br>

## Chapter 5 Conditional Probability. Stochastic Independece

<br>

### 1. Condtional Probability

\
**Definition.** Let $H$ be an event with positive probability. For an arbitrary event $A$, we shall write

$$
(1.3) \hspace{4em} \bold{P}\{A\ |\ H\} = \frac{\bold{P}\{AH\}}{\bold{P}\{H\}}
$$

The quantity so defined is called the **conditional probability of $A$ on the hypothesis $H$** (or for given $H$).
Conditional probabilities remains undefined when the hypothesis has 0 probability.

The proportionality factor $\bold{P}\{H\}$ is necessary in order to reduce the probability of the new sample space to unity. The formulation shows that *all general theorems on probabilities are valid also for conditional probabilities with respect to any particular hypothesis $H$*, for example

$$
(1.4) \hspace{4em} \bold{P}\{A\cup B\ | H\} = \bold{P}\{A\ |\ H\}+\bold{P}\{B\ |\ H\}-\bold{P}\{AB\ |\ H\}
$$

Let $H_1, ..., H_n$ be a set of mutually-exclusivve events of which one necessarily occurs (that is, the union of $H_1, ..., H_n$ is the entire sample space). Then any event $A$ can occur only in conjunctoin with some $H_j$, or in symbols

$$
(1.7) \hspace{4em} A=AH_1\cup AH_2 \cup \cdots \cup AH_n\\
(1.8) \hspace{3em} \bold{P}\{A\}=\sum \bold{P}\{A\ |\ H_j\}\cdot \bold{P}\{H_j\}
$$

This formula is useful because an evaluation of the conditional probabilities $\bold{P}\{A\ |\ H_j\}$ is frequently esier than a direct calculation of $\bold{P}\{A\}$.

<br><br><br>

### 2. Probabilities Defined by Conditional Probabilities. Urn Models

\
**Urn model:** An urn contains $b$ black and $r$ red balls. A ball is drawn at random. It is replaced and moreover, $c$ balls of the color drawn and $d$ balls of the opposite color are added. A new random drawing is made from the urn (now containing $r+b+c+d$ balls), and this procedure is repeated. [Here $c$ and $d$ are arbitrary integers. They may be chosen negative, except that in the case the procedure may terminate after finitelly many drawings for lack of balls.]

Explicit expressions for the probabilities are not readily obtainable except in the most important and best-known special case, that of

**Polya's urn scheme**, which is characterized by $d=0, c>0$. [After each drawing, the number of balls of the color drawn increases, whereas the balls of opposite color remain unchanged in number.]

The probability that of $n=n_1+n_2$ drawings the first $n_1$ ones result in black balls and the remaining $n_2$ ones in red balls is given by

$$
(2.3) \hspace{2em} \frac{b(b+c)(b+2c)\cdots(b+n_1c-c)\cdot r(r+c) \cdots (r+n_2c-c)}{(b+r)(b+r+c)(b+r+2c)\cdots(b+r+nc-c)}
$$

All possible sequences of $n_1$ black and $n_2$ red balls have the same probability.

The use of general binomial coefficient permits us to rewrite the probability $p_{n_1, n}$ that $n$ drawings result in $n_1$ black adn $n_2$ red balls in any order in either of the following forms:

$$
(2.4) \hspace{2em} p_{n_1, n}=\frac{\displaystyle\binom{n_1-1+b/c}{n_1}\binom{n_2-1+r/c}{n_2}}{\displaystyle\binom{n-1+(b+c)/c}{n}} = \frac{\displaystyle\binom{-b/c}{n_1}\binom{-r/c}{n_2}}{\displaystyle\binom{-(b+r)/c}{n}}
$$

\
\
Another special case of interest, namely the
**Ehrenfest model of heat exchange** between 2 isolated bodies [There are 2 containers, suppose particles in container_1 red, the others black. Then at each drawing the drawn is replaced by a ball of the opposite color, that is, we have $c=-1, d=1$]

\
In the statistical literature, is has become customary to use the word *contagion* instead of *aftereffect*.

<br><br><br>

### 3. Stochastic Independence

\
$A$ is stochastically independent of $H$ if the following condition holds

$$
(3.1) \hspace{4em} \bold{P}\{AH\} = \bold{P}\{A\} \cdot \bold{P}\{H\}
$$

This equation symmetric in $A$ and $H$ and shows whenever $A$ is stochatically independent of $H$, so is $H$ of $A$.

**Definition 1.** 2 events $A$ and $H$ are said to be stochastically independent (or independent, for short) if equation (3.1) holds. This definition is accepted also if $\bold{P}\{H\} = 0$, in which case $\bold{P}\{A\ |\ H\}$ is not defined. The term *statistically* independent is synonymous with stochatically independent.

If $H$ occurs, the complementary event $H'$ does not occur, and vice versa. Stochastic independence implies that no inference can be drawn from the occurrence of $H$ to that of $A$; therefore stochastic independence of $A$ and $H$ should mean the same as independence of $A$ and $H'$ (and, because of symmetry, also of $A'$ and $H$, and of $A'$ and $H'$). This can be verified

$$
\begin{align*}
  (3.2) \hspace{4em} \bold{P}\{AH'\}&=\bold{P}\{A\}-\bold{P}\{AH\}\\
  &=\bold{P}\{A\}-\bold{P}\{A\}\cdot \bold{P}\{H\}=\bold{P}\{A\} \cdot \bold{P}\{H'\}
\end{align*}
$$

**Definition 2.** The events $A_1, A_2, ..., A_n$ are called **mutually independent** if for all combinations $1 \le i < j < k < \cdots \le n$ the multiplication rules

$$
\begin{align*}
  \bold{P}\{A_iA_j\}&=\bold{P}\{A_i\}\bold{P}\{A_j\}\\
  \bold{P}\{A_iA_jA_k\}&=\bold{P}\{A_i\}\bold{P}\{A_j\}\bold{P}\{A_k\}\\
  \cdots \ \cdots \ \cdots\\
  \bold{P}\{A_1A_2\cdots A_n\}&=\bold{P}\{A_1\}\bold{P}\{A_2\} \cdots \bold{P}\{A_n\}\\
  \text{apply}
\end{align*}
$$

The first line stands for $\binom{n}{2}$ equations, which suffices to insure *pairwise independence*.

<br><br><br>

### 4. Product Spaces. Independent Trials

\
The **combinatorial product** of 2 sets $A$ and $B$ is the set of all ordered pairs $(a, b)$ of their elements, denoted by $(A, B)$. [Another commonly used notation is $A \times B$. The terms combinatorial product and Cartesian product are synonymous.] The definition carries over triviallyy to triples $(A, B, C)$ and even to infinite sequences.

Infinite product spaces are the natural habitat of probability theory.

Suppose $\mathfrak{A}, \mathfrak{B}$ are 2 sample spaces with points $\alpha_1, \alpha_2, ...$ and $\beta_1, \beta_2, ...$ carrying probabilities $p_1, p_2, ...$ and $q_1, q_2, ...$, respectively. Succession of the 2 experiments are independent only if

$$
(4.1) \hspace{4em} \bold{P}\{(\alpha_i, \beta_k)\} = p_i q_k
$$

\
**Conventions.** 
  1. The phrase "2 independent experiments" refers to the combinatorial product of 2 sample spaces with probabilities defined by the product rule (4.1). This convention applies equally to the notion of $n$ successivve independent experiments
  2. We speak of repeated independent trials if the component sample spaces (and the probabilities in them) are identical.

\
An intuitively obvious property of independent experiments deserves mention. Let $A$ be an event in $\mathfrak{A}$ containing the points $\alpha_{s_1}, \alpha_{s_2}, ...$; let similarly $B$ be an event in $\mathfrak{B}$ containing the points $\beta_{t_1}, \beta_{t_2}, ...$. Then $(A, B)$ is the event in $(\mathfrak{A}, \mathfrak{B})$ which consists of all pairs $(\alpha_{s_i}, \beta_{t_k})$,

$$
(4.2)\ \bold{P}\{(A, B)\}=\sum \sum p_{s_i} q_{t_K} = \sum p_{s_i} \sum q_{t_k} = \bold{P}\{A\} \bold{P}\{B\}
$$

<br><br><br>

## Chapter 6 The Binomial and the Poisson Distributions

<br>

### 1. Bernoulli Trials

*Repeated independent trials are called **Bernoulli trials** if there are only 2 possible outcomes for each trials and their probabilities remain the same throughout the trials.* It is usual to denote the 2 probabilities by $p$ and $q$, and to refer to the outcome with probability $p$ as "success", S, and to the other as "failure", F.

<br>

### 2. The Binomial Distribution

Frequently we are only interested in the total number of successes produced in a succession of $n$ Bernoulli trials but not in their order.

\
**Theorem.** Let $b(k;n,p)$ be the probability that $n$ Bernoulli trials with probability $p$ for success and $q=1-p$ for failure result in $k$ successes and $n-k$ failures, Then

$$
(2.1) \hspace{2em} b(k;n,p)=\binom{n}{k}p^kq^{n-k}
$$

We shall treat $p$ as a constant and denote the number of successes in $n$ trials by $S_n$; the $b(k;n,p)=\bold{P}\{S_n=k\}$. In the general terminology $S_n$ is a ***random variable***; we shall refer to it as the **binomial distribution**.

<br>

### 3. The Central Term and the Tails

\
From (2.1) we see that 

$$
(3.1) \hspace{2em} \frac{b(k;n,p)}{b(k-1;n,p)}=\frac{(n-k+1)p}{kq}=1+\frac{(n+1_p-k)}{kq}
$$

There exists exactly one integer $m$ such that 

$$
(3.2) \hspace{2em} (n+1)p-1< m \le (n+1)p
$$

and we have the

**Theorem.** As $k$ goes from $0$ to $n$, the terms $b(n;k,p)$ first increase monotonically, then decrease monotonically, reaching their greatest value when $k = m$, except that $b(m-1;n,p) = b(n;k,p)$ when $m = (n+1)p$.

We shall call $b(m;n,p)$ the *central* term.

The probability of having exactly $r$ successes is less interesting than the probability of at least $r$ successes; that is

$$
(3.3) \hspace{2em} \bold{P}\{S_n \ge r\}=\sum ^\infty _{v=0} b(r+v;n,p)
$$

The series is only formally infinite since the term with $v > n -r$ vanish. An rough upper bound for this probability is given below (a more sophisticated estimates will be mentioned soon). It is obvious from (3.1) that the terms of the series in (3.3) decrease faster than the terms of a geometric series with ratio $1-\displaystyle\frac{r-np}{rq}$, and so

$$
(3.4) \hspace{4em} \bold{P}\{S_n \ge r\} \le b(r;n,p) \frac{rq}{r - np}
$$

On the other hand, there are more than $r-np$ integers $k$ such that $m \le k \le r$. The corresponding terms of the binomial distribution add to less than unity, and none is smaller than $b(r;n,p)$. [$b(r;n,p) \cdot (r-np) \le 1$] It follows that this quantity is at most $(r-np)^{-1}$, and hence

$$
(3.5) \hspace{4em} \bold{P}\{S_n \ge r\} \le \frac{rq}{(r-np)^2} \hspace{2em} \text{if } r > np
$$

The same argument could be applied to the left tail, but no calculations are necessary. In fact, saying that there are at most $r$ successes amounts to saying that there are at least $n-r$ failures; applying the equivalent of (3.5) failures we see that

$$
(3.6) \hspace{4em} \bold{P}\{S_n \le r\} \le \frac{(n-r)p}{(np-r)^2} \hspace{2em} \text{if } r < np
$$

<br><br><br>

### 4. The Law of Large Numbers

