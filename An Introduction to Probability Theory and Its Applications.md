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