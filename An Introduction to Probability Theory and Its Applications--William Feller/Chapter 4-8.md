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
    - [5. The Poisson Approximation](#5-the-poisson-approximation)
    - [6. The Poisson Distribution](#6-the-poisson-distribution)
    - [8. Waiting Times. The Negative Binomial Distribution](#8-waiting-times-the-negative-binomial-distribution)
    - [9. The Multinomial Distribution](#9-the-multinomial-distribution)
  - [Chapter 8 The Normal Distribution to the Binomial Distribution](#chapter-8-the-normal-distribution-to-the-binomial-distribution)
    - [1. The Normal Distribution](#1-the-normal-distribution)
    - [2. Orientation: Symmetric Distributions](#2-orientation-symmetric-distributions)
    - [3. The Demoivre-Laplace Limit Theorem](#3-the-demoivre-laplace-limit-theorem)
    - [5. Relation to the Poisson Approximation](#5-relation-to-the-poisson-approximation)
    - [6. Large Deviations](#6-large-deviations)
  - [Chapter 8 Unlimited Sequences of Bernoulli Trials](#chapter-8-unlimited-sequences-of-bernoulli-trials)
    - [2. Systems of Gambling](#2-systems-of-gambling)
    - [3. The Borel-Cantelli Lemmas](#3-the-borel-cantelli-lemmas)
    - [4. The Strong Law of Large Numbers](#4-the-strong-law-of-large-numbers)

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

<br><br>

### 4. The Law of Large Numbers

<br>

If $S_n$ is the number of successes in $n$ trials, then $S_n/n$ is the average number of successes and should near $p$. Consider, the probability that $S_n/n$ exceeds $p + \epsilon$, where $\epsilon > 0$ is arbitrarily small but fixed. THe probability is the same as $\bold{P}\{S_n > n(p+\epsilon)\}$, and by (3.5) this is greater than $1/(n\epsilon ^2)$. It follows that as $n$ increases

$$
\bold{P}\{S_n > n(p+\epsilon)\} \rightarrow 0
$$

We see in the same way that $\bold{P}\{S_n <n(p-\epsilon)\} \rightarrow 0$, and thus

$$
(4.1) \hspace{4em} \bold{P}\{\left| \frac{S_n}{n} - p\right| < \epsilon\} \rightarrow 1
$$

In words: As $n$ increases, the probability that the average number of successes deviates from $p$ by more than any preassigned $\epsilon$ tends to zero. This is one form of the law of large numbers and serves as a basis ofr the intuitive notion of probability as a measure of relative frequencies.

The assertion (4.1) is the classical law of large numbers. It is of very limited interest and should be replaced by the more precise and more useful *strong law of large numbers*.

<br><br>

### 5. The Poisson Approximation

<br>

In many applications we deal with Bernoulli trials where, comparativelly speaking, $n$ is large and $p$ is small, whereas the product $\lambda = np$ is of moderate magnitude. In such cases it is convenient to use an approximation to $b(k;n,p)$ which is due to Poisson and which we proceed to derive. For $k=0$, we have

$$
(5.2) \hspace{4em} b(0;n,p)=(1-p)^n=(1-\frac{\lambda}{n})^n \approx e^{-\lambda}
$$

Furthermore, from (3.1) it is seen that for any fixed $k$ and sufficientlly large $n$

$$
(5.5) \hspace{4em} \frac{b(k;n,p)}{b(k-1;n,p)}=\frac{\lambda-(k-1)p}{kq}\approx \frac{\lambda}{k}
$$

Generally by induction

$$
(5.6) \hspace{4em} b(k;n,p) \approx \frac{\lambda ^k}{k!}e^{-\lambda}
$$

This is the classical *Poisson approximation to the binomial distribution*. In view of its great importance we introduce the notation

$$
(4.7) \hspace{4em} p(k;\lambda) = e^{-\lambda}\frac{\lambda ^k}{k!}
$$

<br><br>

### 6. The Poisson Distribution

\
The 3 principal distributions, with ramifcations throughout probaility theory, are the binomial distribution, the normal distribution (to be introduced in the following chapter), and the Poisson distribution

$$
(6.1) \hspace{4em} p(k;\lambda) = e^{-\lambda}\frac{\lambda ^k}{k!}
$$

The true nature of the Poisson distribution will become apparent only in connection with the theory of stochastic processes.

$$
(6.2) \hspace{4em} p(k;\lambda t) = e^{-\lambda t} \frac{(\lambda t)^k}{k!}
$$

as the probability of finding exactly $k$ points in a fixed interval of length $t$.

The parameter $\lambda$ is a physical constant which determines the density of points on the $t$-axis.

<br><br>

### 8. Waiting Times. The Negative Binomial Distribution

\
Consider a succession of $n$ Bernoullli trials and let us inquire how long it will take for the $r$th success to turn up. Here $r$ is a fixed positive integer. The total number of successes in $n$ trials may fall short of $r$, but the probability that the $r$th success occurs at the trial number $v \le n$ is clearly independent of $n$ and depends only on $v, r and p$. Since necessarily $v \ge r$, it is preferable to write $v = k + r$. The probability that the $r$th success occurs at the trial number $r + k$ (where $k = 0, 1,...$) will be denoted by $f(k;r,p)$. It equals the probabilty that exactly $k$ failures precede $r$th success.

$$
(8.1) \hspace{4em} f(k;r,p)=\binom{r+k-1}{k} \cdot p^r q^k
$$

Rewriting the binomial coefficient in accordance with Chapter 2, (12.4) $\displaystyle\binom{-a}{k} = (-1)^k \binom{a+k-1}{k}$, we find the alternative form

$$
(8.2) \hspace{4em} f(k;r,p)=\binom{-r}{k} p^r (-q)^k, \hspace{2em} k=0,1,2,...
$$

We must ask whether it is possible that the trial *never* end, that is, whether an infinite sequence eof trials may produce fewer than $r$ successes.
The probability of an infinite sequence with fewer than $r$ successes can be discounted if, and only if,

$$
(8.3) \hspace{4em} \sum ^\infty _{k=0} f(k;r,p)=1
$$

This is so because by the binomial theorem

$$
(8.4) \hspace{4em} \sum ^\infty _{k=0} \binom{-r}{k} (-q)^k = (1-q)^{-r} = p^{-r}
$$

Multiplying (8.4) by $p^r$ we get (8.3).

For arbitrary fixed real $r > 0$ and $0 < p < 1$ the sequence $\{f(k;r,p)\}$ is called **a negative binomial distribution**.

When $r$ is a positive integer $\{f(k;r,p)\}$ may be interpreted as the probability distribution for waiting time to the $r$th success.

<br><br>

### 9. The Multinomial Distribution

\
The binomial distribution can easily be generalized to the case of $n$ repeated independent trials where each trial can have one of several outcomes. Denote the possible outcomes of each trial by $E_1, ..., E_r$, and suppose that the probability of the realization of $E_i$ in each trial is $p_i\ (i=1,...r)$. In general, the numbers $p_i$ are subject only to the condition

$$
(9.1) \hspace{4em} p_1+ \cdots +p_r=1, \hspace{2em} p_i \ge 0
$$

The result of $n$ trials is a succession like $E_3 E_2 E_1 ...$. The probability that in $n$ trials $E_i$ occurs $k_i$ times, $E_2$ occurs $k_2$ times, etc., is

$$
(9.2) \hspace{4em} \frac{n!}{k_1! k_2! \cdots k_r!} p_1^{k_1} p_2^{k_2} \cdots p_r^{k_r}
$$

here the $k_i$ are arbitrary non-negative integers subject to the obvious condition

$$
(9.3) \hspace{4em} k_1+k_2+ \cdots +k_r = n
$$

<br><br><br>

## Chapter 8 The Normal Distribution to the Binomial Distribution

<br><br>

### 1. The Normal Distribution

**Definition.** The function defined by

$$
(1.1) \hspace{4em} \mathfrak{n}(x)=\frac{1}{\sqrt{2 \pi}} e^{-\frac{1}{2}x^2}
$$

is called the normal density function; its integral

$$
(1.2) \hspace{4em} \mathfrak{N} (x)=\frac{1}{\sqrt{2 \pi}} \int ^x _{-\infty} e^{-\frac{1}{2}y^2} dy
$$

is the normal distribution function.
[The notation $\mathfrak{n}$ and $\mathfrak{N}$ are not standard. $\phi$ and $\Phi$ are more customary. This is for consistency with volume 2]

\
**Lemma 1.** The domain bounded by the graph of $\mathfrak{n}(x)$ and the $x$-axis has unit area, that is,

$$
(1.3) \hspace{4em} \int ^{+\infty} _{-\infty} \mathfrak{n}(x) dx = 1
$$

**Proof.** We have

$$
\begin{align*}
(1.4) \hspace{4em} \{\int ^{+\infty}_{-\infty} \mathfrak{n}(x) dx\}^2 &= \int ^{+\infty}_{-\infty} \int ^{+\infty}_{-\infty} \mathfrak{n}(x) \mathfrak{n}(y)\ dx\ dy\\
&=\frac{1}{2\pi} \int ^{+\infty}_{-\infty} \int ^{+\infty}_{-\infty} e^{-\frac{1}{2}(x^2+y^2)}\ dx\ dy
\end{align*}
$$

This doulbe integral can be expressed in polar coordinates. The remaining calculations are omitted.

$$
(1.6) \hspace{4em} \mathfrak{N}(-x) = 1 - \mathfrak{N}(x)
$$

For many purposes it is convenient to have an elementary estimate of $1 - \mathfrak{N}(x)$, for large $x$. Such an estimate is given by

\
**Lemma 2.** As $x \rightarrow \infty$

$$
(1.7) \hspace{4em} 1 - \mathfrak{N}(x) \sim x^{-1} \mathfrak{n}(x)
$$

more precisely, the double inequality

$$
(1.8) \hspace{4em} [x^{-1} - x^{-3}] \mathfrak{n}(x) < 1 - \mathfrak{N}(x) < x^{-1}\mathfrak{n}(x)
$$

holds for every $x > 0$.

\
**Proof.** Obviously

$$
(1.9) \hspace{2em} [1 - 3x^{-4}]\mathfrak{n}(x) < \mathfrak{n}(x) < [1+x^{-2}]\mathfrak{n}(x)
$$

\
**Note on Terminology.**

The term *distribution function* is used in the mathematical literature for never-decreasing functions of $x$ which tend to $0$ as $x \rightarrow -\infty$, and to $1$ as $x \rightarrow \infty$. Statisticians currently prefer the term *cummulative distribution function*, but the adjective "cummulative"is redundant. A *density function* is a non-negative function $f(x)$ whose integral, extended over the entire $x$-axis, is unity. The older term *frequency function* is a synonym for density function.

The normal distribution function is often called the *Gaussian distribution*, but it was used in the probability theory earlier by DeMoivre and Laplace. If the origin and the unit of measurement are changed, then $\mathfrak{N}(x)$ is tranformed into $\mathfrak{N}((x-a)/b)$; this function is called the normal distribution function with mean $a$ and variance $b^2$ (or standard deviation $|b|$). The function $2\mathfrak{N}(x\sqrt{2})-1$ is often called *error function*.

<br><br>

### 2. Orientation: Symmetric Distributions

\
We proceed to explain the use of normal distribution as an approximation to the binomial with $p=\frac{1}{2}$.

For definiteness we take $n=2v$ even, and to simplify notations we put

$$
(2.1) \hspace{4em} a_k = b(v+k;2v,\frac{1}{2})
$$

$k$ runs from $-v$ to $v$. Since $a_{-k} = a_k$ we shall consider only $k \ge 0$.

To get an idea concerning the behaviour of the sequence $a_0, a_2, a_2, ...$ we shall compare its general term with $a_0$ using the relation

$$
(2.2) \hspace{4em} a_k = a_0 \cdot \frac{v(v-1)\cdots (v-k+1)}{(v+1)(v+2)\cdots(v+k)}
$$

which follows trivially from the definition.

[Some inferences are omitted here.]

\
If $v \rightarrow \infty$ and $k$ varies within a range $0 < k < K_v$ such that

$$
(2.4) \hspace{4em} K_v^3 /v^2 \rightarrow 0
$$

We have the approximation

$$
(2.5) \hspace{4em} a_k \sim a_0 e^{-k^2/v}
$$

Combining Stirling's formula

$$
(2.7) \hspace{4em} a_k \sim h \mathfrak{n}(kh) \hspace{2em} \text{where } h = \sqrt{2/v} = 2/\sqrt{n}
$$

\
**Approximation Theorem.** For fixed $z_1 < z_2$

$$
(2.10) \hspace{4em} \sum _{\frac{1}{2}z_1\sqrt{n} \le k \le \frac{1}{2}z_2 \sqrt{n}} a_k \rightarrow \mathfrak{N}(z_2) - \mathfrak{N}(z_1)
$$

<br><br>

### 3. The Demoivre-Laplace Limit Theorem

\
We proceed to show how our approximations can be extended to the general binomial distribution with $p \ne \frac{1}{2}$. The first complication arises in connection with the central term of the distribution. The index $m$ of the central term is the unique integer of the form

$$
(3.1) \hspace{4em} m = np + \delta \hspace{2em} \text{with } -q < \delta \le p
$$

The quantity $\delta$ will be ultimately neglected, but it occurs in the calculations.

\
Now we renumber the terms of the binomial distribution and write

$$
(3.2) \hspace{4em} a_k = b(m+k;n,p) = \binom{n}{m+k} p^{m+k} q^{n-m-k}
$$

For definiteness we consider $k > 0$, since the range $k < 0$ is covered by interchanging $p$ and $q$. We have now

$$
(3.3) \hspace{4em} a_k=a_0 \frac{(n-m)(n-m-1)\cdots(n-m-k+1)p^k}{(m+1)(m+2)\cdots(m+k)q^k}
$$

This can be rewritten in the form

$$
(3.4) \hspace{4em} a_k = a_0 \frac{(1-pt_0)(1-pt_1)\cdots (1-pt_{k-1})}{(1+qt_0)(1+qt_1)\cdots(1+qt_{k-1})}
$$

where we put for abbreviation

$$
(3.5) \hspace{4em} t_j = \frac{j + \delta + q}{(n+1)pq}
$$

We shall use (3.4) only for values of $k$ for which $t_k$ is small, say $t_k < \frac{1}{2}$. From the Taylor expansion (Chapter 2, (8.9)) for the logarithm it is then clear that

$$
(3.6) \hspace{4em} \frac{1-pt_j}{1+qt_j} = e^{-t_j+\cdots}
$$

Thus

$$
(3.7) \hspace{4em} a_k = a_0 e^{-(t_0+ \cdots +t_{k-1})+ \cdots}
$$

For simplicity we replace the right side by $k^2/(2npq)$ thereby committing an error less than $2k/(npq)$. Thus, if we write

$$
(3.9) \hspace{4em} a_k = a_0 e^{-k^2/(2npq)+\rho_k}
$$

the error term $\rho_k$ satisfies the inequality

$$
(3.10) \hspace{4em} |\rho_k| < \frac{k^3}{(npq)^2} + \frac{2k}{npq}
$$

[Some inferences are omitted]

\
**Theorem 1.** If $n \rightarrow \infty$ and $k$ is constrained to an interval $k < K_n$ such that $K_n^3/n^2 \rightarrow 0$, then for every $\epsilon > 0$ and $n$ is sufficiently large

$$
(3.14) \hspace{4em} 1-\epsilon < \frac{a_k}{k\mathfrak{n}(kh)} < 1 + \epsilon
$$

The main application of theorem 1 is to obtain approximations to probabilities of the form

$$
(3.15) \hspace{4em} \bold{P}\{\alpha \le S_n \le \beta\} = \sum ^\beta _{v=\alpha}b(v;n,p) = \sum ^{\beta-m} _{k=\alpha-m} a_k
$$

\
**Theorem 2.** *(DeMoivre-Laplace limit theorem.)* For fixed $z_1$ and $z_2$ as $n \rightarrow \infty$

$$
(3.17) \hspace{2em} \bold{P}\{np+z_1\sqrt{npq}\le S_n \le np+z_2\sqrt{npq}\} \rightarrow \mathfrak{N}(z_2) -\mathfrak{N}(z_1)
$$

The limit relation (3.17) takes on a more pleasing form is $S_n$ is replaced by the reduced number of successes $S_n^*$ defined by

$$
(3.18) \hspace{4em} S_n^* = \frac{S_n-np}{\sqrt{npq}}
$$

The inequality on the left side in (3.17) is the same as $z_1 \le S_n^* \le z_2$ and hence we can restate (3.17) in the form

$$
(3.19) \hspace{4em} \bold{P}\{z_1 \le S_n^* \le z_2\} \rightarrow \mathfrak{N}(z_2) -\mathfrak{N}(z_1)
$$

In most cases we shall refer to the limit theorem in this form. It shows, in particular, that for large $n$ the probability on the left is practically independent of $p$. This perits us to compare fluctuations in different series of Bernoulli trials simply by referring to our standard units.

<br><br>

### 5. Relation to the Poisson Approximation

\
For small $\lambda=np$ only the Poisson approximation can be used, but for large $\lambda$ we can use either the normal or the Poisson approximation. This implies that for large vales of $\lambda$ it must be possible to approximmate the Poisson distribution by the normal distribution.

<br>

### 6. Large Deviations

\
The Demoivre-Laplace theorem describess the asymptotic behavior of $\bold{P}\{z_1 < S_n^* < z_2\}$ for fixed $z_1$ and $z_2$. From its deviation it is clear that the theorem applies also when $z_1$ and $z_2$ are permitted to vary with $n$ in such a way that $z_1 \rightarrow \infty$, provided that the growth is sufficiently slow. In this case both sides in (3.17) tend to $0$, and the theorem is meaningful only if the *ratio* of the 2 sides tends to unity.

To simplify the formulation the double inequality $z_1 < S_n^* < z_2$ is replaced by $S_n^* > z_1$. This is justified by the following lemma, which shows that when $z_1 \rightarrow \infty$ the upper limit $z_2$ plays no role.

\
**Lemma.** If $x_n \rightarrow \infty$ then for every fixed $\eta > 0$

$$
(6.1) \hspace{4em} \frac{\bold{P}\{S_n^* > x_n + \eta\}}{\bold{P}\{S_n^* > x_n\}} \rightarrow 0
$$

that is

$$
(6.2) \hspace{4em} \bold{P}\{x_n < S_n^* \le x_n + \eta\} \sim \bold{P}\{S_n^* > x_n\}
$$

In other words: When $S_n^*$ exceeds $x_n$ it is likely to be very close to $x_n$, and larger values play no role in the limit.

[Related proof is omitted]

\
**Theorem.** If $x_n \rightarrow \infty$ in such a way that $x_n^3/\sqrt{n} \rightarrow 0$, then

$$
(6.6) \hspace{4em} \bold{P}\{S_n^* > x_n\} \sim 1 - \mathfrak{N}(x_n)
$$

In view of (1.7) the asymptotic relation (6.6) is fully equivalent to

$$
(6.7) \hspace{4em} bold{P}\{S_n^* > x_n\} \sim \frac{1}{\sqrt{2 \pi}} \cdot \frac{1}{x_n} e^{-\frac{1}{2}x_n^2}
$$

[Related proof is omitted]

<br><br><br>

## Chapter 8 Unlimited Sequences of Bernoulli Trials

\
In the present volume we are confined to the theory of discrete sample spaces, and this means a considerable loss of mathematical elegance. The general theory considers $n$ Bernoulli trials only as the beginning of an infinite sequence of trials. A sample point is then represented by an infinite sequence of letters $S$ and $F$, and the sample space is the aggregate of all such sequences. A finite sequence, like $SSFS$, stands for aggregate of all points with this beginning, that is, for compound event that in an infinite sequence fo tial s the first four result in $S, S, F, S$ respectively.

<br>

### 2. Systems of Gambling

\
We define a system as a set of fixed rules which for every trial uniquely determine whether or not the bettor is to bet; at the $k$th trial the decision may depend on the outcomes of the first $k-1$ trials, but not on the outcome of trials number $k, k+1, k+2,...$; finally the rules must be such as to ensure an indefinite continuation of the game.

Under any system the successive bets form a sequence of Bernoulli trials with unchanged probability for success.

For simplicity we assume that $p = \frac{1}{2}$. Let $A_k$ be the event "first bet occurs at the $k$th trial." Our definition of system requires that as $n \rightarrow \infty$ the probability that the first bet has occurred before the $n$th trial tends to $1$. This means

$$
(2.1) \hspace{4em} \sum \bold{P}\{A_k\} = 1
$$

\
Next, let $B_k$ be the event "head at $k$th trial" and $B$ the event "the trial of the first bet results in heads." Then $B=A_1B_1 + A_2B_2 + A_3B_3 + ...$ which are mutually exclusive. Now $A_k$ only depends on the outcome of the first $k - 1$ trials, and $B_k$ only on the trial number $k$. Hence $A_k$ and $B_k$ are independent and $\bold{P}\{A_k B_k\} = \bold{P}\{A_k\} \bold{P}\{B_k\} = \frac{1}{2} \bold{P}\{A_k\}$. Thus $\bold{P}\{B\} = \sum \bold{P}\{A_kB_k\}=\frac{1}{2}\sum \bold{P}\{A_k\} = \frac{1}{2}$. This shows that under this system the probability of heads at the first bet is $\frac{1}{2}$.

\
It remains to show that the bets are stochastically independent. To verify this statement let $A_k^*$ be the event that the second bet occurs at the $k$th trial. Let $E$ represent the event "heads at the first 2 bets"; it is the union of all events $A_jB_jA_k^*B_k$ where $j < k$ (if $j \ge k$, then $A_j$ and $A_k^*$ are mutually exclusive and $A_jA_k^* = 0$). Therefore

$$
(2.2) \hspace{4em} \bold{P}\{E\} = \sum _{j=1} ^\infty \sum _{k=j+1} ^\infty \bold{P}\{A_jB_jA_k^*B_k\}
$$

As before, we see that the event $B_k$ is independent of the event $A_jB_jA_k^*$ (which depends only on the outcomes of hte first $K-1$ trials). Hence

$$
\begin{align*}
  (2.3) \hspace{4em} \bold{P}\{E\} &= \frac{1}{2} \sum _{j=1} ^\infty \sum _{k=j+1} ^\infty \bold{P}\{A_jB_jA_k^*\}\\
  &= \frac{1}{2} \sum _{j=1} ^\infty \bold{P}\{A_jB_j\} \sum _{k=j+1} ^\infty \bold{P}\{A_k^*\ |\ A_jB_j\}
\end{align*}
$$

Now, whenever the first bet occurs and whatever its outcome, the game is sure to continue. The second series in (2.3) is unity, and we have already seen that $\sum \bold{P}\{A_jB_j\} = \frac{1}{2}$. Hence $\bold{p}\{E\} = \frac{1}{4}$ as contended.

\
Note that the situation is different when the player is permitted to vary his stakes. In this case there exist advantageous strategies, and the game depends on the strategy.

<br><br>

### 3. The Borel-Cantelli Lemmas

\
2 simple lemmas concerning infinite sequences of trials are used to frequently that they deserve special attention. We formulate them for Bernoulli trials, but they apply to more general cases.

Let $A_1, A_2, ...$ be an infinite sequence of events each of which depends only on a finite number of trials; in other words, we suppose that there exists an integer $n_k$ such that $A_k$ is an event in the sample space of the first $n_k$ Bernouli trials. Put

$$
(3.1) \hspace{4em} a_k = \bold{P}\{A_k\}
$$

We can speak of the event $U_r$, that an unen ding sequence of trials produces more than $r$ among the enents $\{A_k\}$, and also of the event $U_\infty$, that infinitely many among the $\{A_k\}$ occur. The event $U_r$ is defined only in the infinite sample space, and ite probability is the limit of $\bold{P}\{U_{n,r}\}$, the probability that $n$ trials produce more than $r$ among the events $\{A_k\}$. Finally, $\bold{P}\{U_\infty\} = \lim \bold{P}\{U_r\}$.

\
**Lemma 1.** If $\sum a_k$ converges, the with probability one only finitely many events $A_k$ occur. More precisely, it is claimed that for $r$ sufficiently large, $\bold{P}\{U_r\} < \epsilon$ or: to every $\epsilon > 0$ it is possible to find an integer $r$ such that the probability that $n$ trials produce one or more among the events $A_{r+1}, A_{r+2}, ...$ is less than $\epsilon$ for all $n$.

\
**Lemma 2.** If the events $A_k$ are mutually independent, ad if $\sum a_k$ diverges, then with probability one infinitely many $A_k$ occur. In other words, it is claimed that for every $r$ the probability that $n$ trials produce more than $r$ among the events $A_k$ tend to $1$ as $n \rightarrow \infty$.

<br><br>

### 4. The Strong Law of Large Numbers

\
We deal with a statement much stronger than the weak law of large numbers [Chapter 6, (4.1)]. THe latter says that for every sufficiently large fixed $n$ the average $S_n / n$ is likely to be near $p$, but it does not say that $S_n / n$ is bound to stay near $p$ if the number of trials is increased. We shall now prove that with probability one $S_n / n - p$ becomes adn remains small.

\
**Strong Law of Large Numbers.** For every $\epsilon > 0$ with probability one there occur only finitely many of the events

$$
(4.2) \hspace{4em} \left| \frac{S_n}{n} - p \right| > \epsilon
$$

[Proof is omitted]

\
The strong law of large numbers was first formulated by Cantelli after Borel and Hausdorff has discussed certain special cases. Like the weak law, it is only a very special case of a general theorem on random variables.

Following theory inferences of the chapter are skipped at first reading.