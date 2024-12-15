# MATH2023 Summary Multivariable Calculus

## Table of Contents

- [MATH2023 Summary Multivariable Calculus](#math2023-summary-multivariable-calculus)
  - [Table of Contents](#table-of-contents)
    - [Retangular Integral =\> Polar Integral](#retangular-integral--polar-integral)
    - [Surface area](#surface-area)
    - [Chapter 3: Multiple Integrals](#chapter-3-multiple-integrals)

### Retangular Integral => Polar Integral

\
**Find slope of tangent line to a polar curve in polar coordinate**

Suppose that $r = f(\theta)$. f is differentiable at $\theta=\theta_0$, then the slope of tangent line to the curve at point $(r_0, \theta_0)$ is given by

$$
\frac{dy}{dx} = \frac{f'(\theta_0) \sin \theta_0 + f(\theta_0) \cos \theta_0}{f'(\theta_0) \cos \theta_0 - f(\theta_0) \sin \theta_0}
$$

provided that the denominator is nonzero at the point. At angle $\theta_0$ for which $f(\theta_0)=0$ and$f'(\theta_0) \neq 0$, the tangent line has slope $tan \theta_0$.

\
**Theorem: Changing Rectangular Integrals into Polar Integrals**

Keypoint: $dA = dy dx = r dr d\theta$

If $z = f(x, y)$ is a continuous function of 2 real variables over region R,

$$
\iint_{R} f(x, y)dA = \int^{\theta_{max}}_{\theta_{min}} \int ^{r_{max}}_{r_{min}} f(rcos\theta, rsin\theta)rdr d\theta
$$

Where G is the region of integration in polar coordinates.

### Surface area

\
Suppose that surface S is traced out by $\vec r(u, v) = <x(u, v), y(u, v), z(u, v)>$ where $a \leq u \leq b$ and $c \leq v \leq d$

$$
\Delta S_k = \left| \frac{\partial \vec r}{\partial u} \times \frac{\partial \vec r}{\partial v} \right| \cdot \Delta v_k \cdot \Delta u_k
$$

Then the surface area of S equals

$$
S = \lim_{n \rightarrow \infty } \sum ^n _{k=1} \left| \frac{\partial \vec r}{\partial u} \times \frac{\partial \vec r}{\partial v} \right| \cdot \Delta v_k \cdot \Delta u_k = \iint _R 
\left| \frac{\partial \vec r}{\partial u} \times \frac{\partial \vec r}{\partial v} \right|dvdu
$$

\
Similarly, the **volume** of a solid traced out by $\vec r(u, v, w) = <x(u, v, w), y(u, v, w), z(u, v, w)>$ could be computed in this way

$$
\Delta V_k = \left| \frac{\partial \vec r}{\partial u} \cdot \left(\frac{\partial \vec r}{\partial v} \times \frac{\partial \vec r}{\partial w}\right) \right| \Delta u_k \Delta v_k \Delta w_k
$$

$$
V = \iiint _R \left| \frac{\partial \vec r}{\partial u} \cdot \left(\frac{\partial \vec r}{\partial v} \times \frac{\partial \vec r}{\partial w}\right) \right|dudvdw
$$

\
**Theorem：finding area of a surface given by a Rectangular Equation**

Given that R is a planar region on xy-plane. Suppose $z = f(x, y)$ is a continuously differentiable function defined on the region R. Then S, traced out by $f(x, y)$

$$
S = \iint _R \sqrt{(\frac{\partial f}{\partial x})^2 + (\frac{\partial f}{\partial y})^2 + 1} dA, \text{ where } dA = dy dx = dx dy
$$

(Just use the rectangular equation to form a vector function $\vec{r}(x, y) = <x, y, f(x, y)>$)

To be continued

### Chapter 3: Multiple Integrals
Content...