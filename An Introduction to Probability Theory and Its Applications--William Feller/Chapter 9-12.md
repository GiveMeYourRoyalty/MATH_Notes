# An Introduction to Probability Theory and Its Applications

**Arthur: William Feller**

- [An Introduction to Probability Theory and Its Applications](#an-introduction-to-probability-theory-and-its-applications)
  - [Chapter 9 Random Variables; Expectation](#chapter-9-random-variables-expectation)
    - [1. Random Variables](#1-random-variables)

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