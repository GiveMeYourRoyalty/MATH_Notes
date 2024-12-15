# MATH2023 Summary Multivariable Calculus

## Table of Contents

- [MATH2023 Summary Multivariable Calculus](#math2023-summary-multivariable-calculus)
  - [Table of Contents](#table-of-contents)
    - [Retangular Integral =\> Polar Integral](#retangular-integral--polar-integral)
    - [Surface area](#surface-area)
    - [Chapter 3: Multiple Integrals](#chapter-3-multiple-integrals)

### Retangular Integral => Polar Integral

Find slope of tangent line to a polar curve in polar coordinate

Suppose that $r = f(\theta)$. f is differentiable at $\theta=\theta_0$, then the slope of tangent line to the curve at point $(r_0, \theta_0)$ is given by

$$
\frac{dy}{dx} = \frac{f'(\theta_0) \sin\theta_0 + f(\theta_0) \cos\theta_0}{f'(\theta_0) \cos\theta_0 - f(\theta_0) \sin\theta_0}
$$

provided that the denominator is nonzero at the point. At angle $\theta_0$ for which $f(\theta_0)=0$ and$f'(\theta_0) \neq 0$, the tangent line has slope $tan \theta_0$.

\
$$
\\
\begin{aligned}
\textbf{Theorem: Changing Rectangular Integrals into Polar Integrals}
\end{aligned}
$$

$$
\begin{aligned}
\hspace{2em} \text{ If } z = f(x, y) \text{is a continuous function of 2 real variables over a region R, then we have the following}
\end{aligned}
$$

$$
\iint_{R} f(x, y)dA = \int^{\theta_{max}}_{\theta_{min}} \int ^{r_{max}}_{r_{min}} f(rcos\theta, rsin\theta)rdr d\theta
$$

$$
\begin{aligned}
\hspace{2em} \text{where G is the region of integration in polar coordinates. Besides, we have } dA = dxdy = rdrd\theta
\end{aligned}
$$


### Surface area

$$
\begin{aligned}
\text{ Suppose that a surface S is traced out by vector function } \vec{r}(u, v) = <x(u, v), y(u, v), z(u, v)> \text{ where } a \leq u \leq b and c \leq v \leq d.
\end{aligned}
$$

$$
\begin{aligned}
\Delta S_k = \left| \frac{\partial \vec r}{\partial u} \times \frac{\partial \vec r}{\partial v} \right| \cdot \Delta v_k \cdot \Delta u_k
\end{aligned}
$$

$$
\begin{aligned}
\text{ Then the surface area of S equals}
\end{aligned}
$$

$$
\begin{aligned}
S = \lim_{n \rightarrow \infty } \sum ^n _{k=1} \left| \frac{\partial \vec r}{\partial u} \times \frac{\partial \vec r}{\partial v} \right| \cdot \Delta v_k \cdot \Delta u_k = \iint _R 
\end{aligned} \left| \frac{\partial \vec r}{\partial u} \times \frac{\partial \vec r}{\partial v} \right|dvdu
$$

$$
\begin{aligned}
\text{ Similarly, volume could be computed in this way } \Delta V_k = \left| \frac{\partial \vec r}{\partial u} \cdot \left(\frac{\partial \vec r}{\partial v} \times \frac{\partial \vec r}{\partial w}\right) \right| \Delta u_k \Delta v_k \Delta w_k, \text{ where } \vec r(u, v, w) \text{ traces out a solid }
\end{aligned}
$$

$$
\begin{aligned}
V = \iiint _R \left| \frac{\partial \vec r}{\partial u} \cdot \left(\frac{\partial \vec r}{\partial v} \times \frac{\partial \vec r}{\partial w}\right) \right|dudvdw
\end{aligned}
$$

$$
\begin{aligned}
\\
\textbf{Theorem: finding surface area given by Rectangular Equation}
\end{aligned}\\
\text{Given that R is a planar region}
$$

To be continued

### Chapter 3: Multiple Integrals
Content...