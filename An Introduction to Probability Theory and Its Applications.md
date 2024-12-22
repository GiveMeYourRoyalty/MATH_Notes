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