# MATH2023 Summary Multivariable Calculus

## Table of Contents

- [MATH2023 Summary Multivariable Calculus](#math2023-summary-multivariable-calculus)
  - [Table of Contents](#table-of-contents)
    - [Notation about Order of Partial Differentiation](#notation-about-order-of-partial-differentiation)
    - [Differentiability and Implicit Differentiation](#differentiability-and-implicit-differentiation)
    - [Gradients](#gradients)
    - [Directional Derivatives](#directional-derivatives)
    - [Linear Approximation, Total Differential](#linear-approximation-total-differential)
    - [Local Extremes](#local-extremes)
    - [Lagrange Multiplier](#lagrange-multiplier)
    - [Fubini's Theorem (First Form)](#fubinis-theorem-first-form)
    - [Rectangular Integral =\> Polar Integral](#rectangular-integral--polar-integral)
    - [Surface area](#surface-area)
    - [Triple Integral in Cylindrical Coordinates](#triple-integral-in-cylindrical-coordinates)
    - [Triple Integral in Spherical Coordinates](#triple-integral-in-spherical-coordinates)
    - [Line Integral](#line-integral)
    - [Vector Fields, Work Done, Flux](#vector-fields-work-done-flux)
    - [Conservative Vector Field](#conservative-vector-field)
    - [Green's Theorem in Curl Form](#greens-theorem-in-curl-form)
    - [Divergence Theorem](#divergence-theorem)
    - [Stokes' Theorem](#stokes-theorem)

### Notation about Order of Partial Differentiation
[Table of Contents](#table-of-contents)

Let $z = f(x, y)$. When differentiating $f$ twice, we produce second order derivatives by the following notation

$$
\frac{\partial ^2 f}{\partial x^2} \stackrel{def}{=} \frac{\partial}{\partial x} (\frac{\partial f}{\partial x}) \stackrel{def}{=} f_{xx}\\
\frac{\partial ^2 f}{\partial y^2} \stackrel{def}{=} \frac{\partial}{\partial y} (\frac{\partial f}{\partial y}) \stackrel{def}{=} f_{yy}\\
\frac{\partial ^2 f}{\partial x \partial y} \stackrel{def}{=} \frac{\partial}{\partial x} (\frac{\partial f}{\partial y}) \stackrel{def}{=} f_{yx}\\
\frac{\partial ^2 f}{\partial y \partial x} \stackrel{def}{=} \frac{\partial}{\partial y} (\frac{\partial f}{\partial x}) \stackrel{def}{=} f_{yx}
$$

### Differentiability and Implicit Differentiation
[Table of Contents](#table-of-contents)

Given that $z = f(x, y)$, $f$ is **differentiable at point $(x_0, y_0)$** if $f_x, f_y$ both exist and

$$
f(x, y) - [f(x_0, y_0) + f_x(x_0, y_0)(x - x_0) + f_y(x_0, y_0)(y-y_0)] = (x - x_0)\ \varepsilon _1(x, y) + (y - y_0)\ \varepsilon _2(x, y),
$$

where $\varepsilon _1(x, y)$ -> 0 and $\varepsilon _2(x, y)$ -> 0 at point $(x, y) \text{ approaches } (x_0, y_0)$

\
**Theorem: Implicit Differentiation**
Suppose that $w = F(x, y)$ is differentiable and assume that $F(x, y) = 0$ defines $y$ as a differentiable function of $x$. Then at any point where $\frac{\partial F}{\partial y} \neq 0$, we must have

$$
\frac{dy}{dx} = -\frac{\frac{\partial F}{\partial x}}{\frac{\partial F}{\partial y}}
$$

### Gradients
[Table of Contents](#table-of-contents)

**Typical Algebraic Properties of Gradients**:

$$
\nabla (fg) = (\nabla f) g + f (\nabla g)\\
\nabla (\frac{f}{g}) = \frac{(\nabla f) g - f (\nabla g)}{g^2}
$$

Notice that they have the same form as the corresponding rules for derivatives of single-variable functions

### Directional Derivatives
[Table of Contents](#table-of-contents)

**Definition of Directional Derivative**
Suppose that $z = f(x, y)$ is a real-value function, $\vec u = <u_1, u_2>$ is a unit vector

$$
(D_{\vec u} f)(a, b) \stackrel{def}{=} \lim _{h \rightarrow 0} \frac{f(a + h u_1, b + hu_2)- f(a, b)}{h - 0} = \frac{d}{dt} [f(a + h u_1, b + hu_2)] |_{t = 0}
$$

\
**Theorem: using Gradients to find Directional Derivatives**

$$
(D _{\vec u} f) (a, b) = \vec u \cdot (\nabla f) (a, b)
$$

### Linear Approximation, Total Differential
[Table of Contents](#table-of-contents)

**Local Linear Approximation** to $z = f(x, y)$ at point $(x_0, y_0, f(x_0, y_0))$:

$$
L(x, y) \stackrel{def}{=} f(x_0, y_0) + (x - x_0) f_x (x_0, y_0) + (y - y_0)f_y (x_0, y_0)
$$

L is exactly the **tangent plane** to the surface $z = f(x, y)$ at point $(x_0, y_0, f(x_0, y_0))$

\
**Definition: Total Differential 全微分**

Suppose that $z = f(x, y)$ is a real-valued function, which is differentiable at point $(x_0, y_0)$. If a point moves from $(x_0, y_0)$ to $(x_0 + \Delta x, y_0 + \Delta y)$

$$
\text{Actual change of } f, \Delta f \stackrel{def}{=} f(x_0 + \Delta x, y_0 + \Delta y) - f(x_0, y_0)
$$

$$
\text{Besides, the change in the linear approximation L }\\
df \stackrel{def}{=} L(x_0 + \Delta x, y_0 + \Delta y) - L(x_0, y_0) = \Delta x \cdot f_x(x_0, y_0) + \Delta y \cdot f_y(x_0, y_0)\\
\text{Somtimes, we write } dx, dy \text{ instead of } \Delta x, \Delta y.\\
df \text{ is called the total differential of f}
$$

### Local Extremes
[Table of Contents](#table-of-contents)

**Definitions of Critical Point and Saddle point**

- **Critical Point 临界点** is an interior point $(a, B)$ in domain of function $z = f(x, y)$ where:
  1. both $\frac{\partial f}{\partial x}(a, b) = \frac{\partial f}{\partial y} = 0$, or
  2. one or both of $\frac{\partial f}{\partial x}(a, b), \frac{\partial f}{\partial y}(a, b)$ does not exist
- **Saddle Point 鞍点** $(a, b, f(a,b))$ is a critical point and there are domain points $(x, y)$ where $f(x, y) > f(a, b)$ and domain points $f(x, y) < f(a, b)$


**Second Derivative Test for Local Extreme Value**
Suppose that $z = f(x, y)$ and its first and second partial derivatives are continuous throughout a disk centered at $(a, b)$ and that $f_x (a, b) = f_y (a, b) = 0$. Then we have the following
  1. $f$ has a **local maximum** at $(a, b)$ if $f_{xx}(a, b) < 0$ and $f_{xx}(a, b) f_{yy}(a, b) - (f_{xy}(a, b))^2 > 0$
  2. $f$ has a **local minimum** at $(a, b)$ if $f_{xx}(a, b) > 0$ and $f_{xx}(a, b) f_{yy}(a, b) - (f_{xy}(a, b))^2 > 0$
  3. $f$ has a **saddle point** at $(a, b)$ if $f_{xx}(a, b) > 0$ and $f_{xx}(a, b) f_{yy}(a, b) - (f_{xy}(a, b))^2 < 0$
  4. The test is inconclusive at $(a, b)$ if $f_{xx}(a, b) > 0$ and $f_{xx}(a, b) f_{yy}(a, b) - (f_{xy}(a, b))^2 = 0$

### Lagrange Multiplier
[Table of Contents](#table-of-contents)

**Extreme-Value Theorem** 极值定理
Suppose that A is a **closed and bounded** region on xy-plane. Function $z = f(x, y)$ is continuous on region A,  then such a function must attain its absolute maximum and minimum at points in region A.

\
**Lagrange Multipliers 拉格朗日乘数**

- One constraint function $g(x, y) = k$. Assume that $\nabla g \neq \vec 0$ at any point on $g(x, y) = k$
  To find the maximum/minimum value and corresponding point of $z = f(x, y)$, solve the following equations

$$
\nabla f(a, b) = \lambda \nabla g(a, b)\\
g(a, b) = k
$$

- Two contraints
  Suppose that there is a point $P(a, b, c)$ such that $w = f(x, y, z)$ has maximum/minimum value at $P(a, b, c)$ subject to the following 2 constraints simultaneously: $g_1(x, y, z) = k_1, g_2(x, y, z) = k_2$. Assume that $\nabla g_i \neq \vec 0$ on each point of $g_i(x, y, z) = k_i$ for each $i = 1, 2$ and $\nabla g_1(P)$ and $\nabla g_2(P)$ are not parellel to each other,

$$
(\nabla f)(a, b, c) = \lambda _1 (\nabla g_1)(a, b, c) + \lambda _2 (\nabla g_2)(a, b, c)\\
g_1(a, b, c) = k_1 \text{ and } g_2(a, b, c) = k_2
$$

### Fubini's Theorem (First Form)
[Table of Contents](#table-of-contents)

Suppose that $z = f(x, y)$ is a continuous function throughtout the rectangular region R: $a \leq x \leq b, c \leq y \leq d$. The we have

$$
\int ^b _a \int ^d _c f(x, y)\ dy\ dx = \iint _R f(x, y)\ dA = \int ^d _c \int ^b _a f(x, y)\ dx\ dy
$$

### Rectangular Integral => Polar Integral
[Table of Contents](#table-of-contents)

**Find slope of tangent line to a polar curve in polar coordinate**

Suppose that $r = f(\theta)$. f is differentiable at $\theta=\theta_0$, then the slope of tangent line to the curve at point $(r_0, \theta_0)$ is given by

$$
\frac{dy}{dx} = \frac{f'(\theta_0) \sin \theta_0 + f(\theta_0) \cos \theta_0}{f'(\theta_0) \cos \theta_0 - f(\theta_0) \sin \theta_0}
$$

provided that the denominator is nonzero at the point. At angle $\theta_0$ for which $f(\theta_0)=0$ and$f'(\theta_0) \neq 0$, the tangent line has slope $\tan \theta_0$.

\
**Theorem: Changing Rectangular Integrals into Polar Integrals**

Keypoint: $dA = dy dx = r dr d\theta$

If $z = f(x, y)$ is a continuous function of 2 real variables over region R,

$$
\iint_R f(x, y) dA = \iint _R f(r \cos \theta, r\sin \theta)rdr d\theta
$$

Where G is the region of integration in polar coordinates.

### Surface area
[Table of Contents](#table-of-contents)

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
S = \iint _R \sqrt{(\frac{\partial f}{\partial x})^2 + (\frac{\partial f}{\partial y})^2 + 1}\ dA, \text{ where } dA = dy dx = dx dy
$$

(Just use the rectangular equation to form a vector function $\vec{r}(x, y) = <x, y, f(x, y)>$)

### Triple Integral in Cylindrical Coordinates
[Table of Contents](#table-of-contents)

\
**Definition: Cylindrical Coordinates System**

$$(r, \theta, z), r \text{ and } \theta \text{ are polar coordinates for the vertical projection of the point onto the xy-plane }$$

$0 \leq r \leq \infty, 0 \leq \theta \leq 2\pi, -\infty < z < \infty$

**Theorem: Triple Integrals in Cylindrical Coordinates System**

If $w = F(x, y, z)$ is continuous over a solid region D in 3d,

$$
\iiint_D F(x, y, z) dV = \iiint_D F(r \cos \theta, r \sin \theta, z)\ dz\ r\ dr\ d \theta
$$

### Triple Integral in Spherical Coordinates

[Table of Contents](#table-of-contents)

Spherical coordinates is especially useful when there is symmetry about a point.

Point $P(\rho, \theta, \phi)$, where $\rho$ is the distance to the origin, $\theta$ is defined same as in Cylindrical coordinates, $0 \leq \phi \leq \pi$ is the angle between OP and positive z-axis

$$
\text{ Trivially, } x = \rho \sin \phi \cos \theta, y = \rho \sin \phi \sin \theta, z = \rho \cos \phi \\
\text{ And the distance } \rho = \sqrt{x^2 + y^2 + z^2}
$$

\
**Theorem: Triple Integral in Spherical Coordinates**

$$
\iiint _D F(x, y, z)\ dV = \int ^{\theta_{max}} _{\theta_{min}} \int ^{\phi_{max}} _{\phi _{min}} \int ^{\rho_{max}} _{\rho_{min}} F(\rho \sin \phi \cos \theta, \rho \sin \phi \sin \theta, \rho \cos \phi)\ \rho^2\ \sin \phi\ d\rho\ d\phi\ d\theta
$$

where the solid D is a spherical wedge 球面楔 defined as follows

$$
D = \{(\rho, \theta, \phi): \theta_{min} \leq \theta \leq \theta_{max}, \phi_{min} \leq \phi \leq \phi_{max}, \rho_{min} \leq \rho \leq \rho_{max} \}
$$

Keypoint: write out the above D when solving problems could reduce the possibility of making pointless errors.

### Line Integral
[Table of Contents](#table-of-contents)

\
Suppose that $z = f(x, y)$ is continuous in a region containing curve C, which is traced out by $\vec r(t) = <x(t), y(t)>$,

$$
\int _C f(x, y)\ ds = \int _C f(x(t), y(t)) \left| \frac{d \vec r}{dt} \right| dt = \int _C f(x(t), y(t)) \sqrt{(\frac{dx}{dt})^2 + (\frac{dy}{dt})^2} dt
$$

A line traced out by $\vec r(t) = <x(t), y(t), z(t)>$ can be computed in a similar way.  Curve line can also be computed separately 分段积分.

### Vector Fields, Work Done, Flux
[Table of contents](#table-of-contents)

\
**Definition: Vector Fields 矢量场**

1. Vector field over planar region R, and M, N are real-valued functions

$$
\vec F(x, y) = M(x, y)\ \vec i + N(x, y)\ \vec j
$$

2. Vector field in solid region R in 2d, and M, N and P are real-valued functions
   
$$
\vec F(x, y, z) = M(x, y, z)\ \vec i + N(x, y, z)\ \vec j + P(x, y, z)\ \vec k
$$
  
**Example: Gradient Field**

The gradient field of a differentiable function $w = f(x, y, z)$ is the field of gradient vectors

$$
\nabla f(x, y, z) = <\frac{\partial f}{\partial x}, \frac{\partial f}{\partial y}, \frac{\partial f}{\partial z}>
$$

\
**Work Done by a force field along a smooth curve C**

$$
\int_C \vec F(x, y, z) \cdot \vec T(x, y, z)\ ds\\
\text{where } \vec T(x, y, z) = \frac{\frac{d \vec r}{dt}}{\left| \frac{d \vec r}{dt} \right|} \text{ is the unit tangent vector to C }
$$

**Remark: equivalent ways to compute work done**

$$
\begin{align*}
\text{Work Done} &= \int_C \vec{F}(x, y, z) \cdot \vec{T}(x, y, z)\ ds \\
&= \int_C \vec{F}(x, y, z) \cdot \frac{\frac{d \vec{r}}{dt}}{\left| \frac{d \vec{r}}{dt} \right|}\ \left| \frac{d \vec{r}}{dt} \right|\ dt \\
&= \int_{t_{\min}}^{t_{\max}} \vec{F}(x(t), y(t), z(t)) \cdot \frac{d \vec{r}}{dt}\ dt \\
&= \int_C \vec{F}(x, y, z) \cdot d \vec{r} \\
&= \int_{t_{\min}}^{t_{\max}} \left( M(x(t), y(t), z(t)) \frac{dx}{dt} + N(x(t), y(t), z(t)) \frac{dy}{dt} + P(x(t), y(t), z(t)) \frac{dz}{dt} \right) dt \\
&= \int_C M\ dx + N\ dy + P\ dz
\end{align*}
$$

Given that $\vec F(x, y, z) = <M(x, y, z), N(x, y, z), P(x, y, z)>$

\
**Fluid's Flow**
Suppose that $\vec F$ is a velocity field of a fluid flowing. $\vec r(t)$ is a smooth curve in the domain of the continuous velocity field

$$
\textbf{fluid's flow } of \vec F \textbf{ along the curve C } = \int _C \vec F \cdot \vec T\ ds\\
\text{ where } \vec T = \frac{\frac{d \vec r}{dt}}{\left| \frac{d \vec r}{dt} \right|} \text{ is the unit tangent vector of } \vec F
$$

The line integral above is called a **flow integral**. If the curve C is closed, then the flow above is called **the circulation of $\vec F$ around loop C**.

**Flux 通量**
Given that Curve C is **smooth and closed** (starting and ending points are same) on contiunous vector field and $\vec n$ is the <u>outward-pointing unti vector on C</u>

$$
\text{Flux of } \vec F \text{ across the curve C } = \int _C \vec F \cdot \vec n\ ds 
$$

The line integral above represents the rate at which the fluid entering and leaving the region enclosed by the curve C.

### Conservative Vector Field
[Table of Contents](#table-of-contents)

Suppose that the vector field $\vec F(x, y, z) = M(x, y, z)\ \vec i + N(x, y, z)\ \vec j + P(x, y, z)\ \vec k$ has continuous first partial derivatives in an open connected region R.

Any vector fields satisfying one of the following three logically equivalent conditions is called a **conservative vector field (definition)**.

**Condition 1**: For any 2 points A and B lying inside R, the work done integral from A to B is **the same over all paths joining points from A to B**
   
$$
\int _C \vec F \cdot d \vec r= \int _C \vec F \cdot \vec T\ ds
$$

**Condition 2**: For every smooth closed curve C

$$
\int _C \vec F \cdot d \vec r = 0
$$

**Condition 3**: There is a scalar function $w = f(x, y, z)$ such that for every point $(x, y, z)$ in the region R, such a function is called **a potential function of the vector field $\vec F$**

$$
\nabla f(x, y, z) = \vec F(x, y, z), i.e. \frac{\partial f}{\partial x} = M(x, y, z), \frac{\partial f}{\partial y} = N(x, y, z), \frac{\partial f}{\partial z} = P(x, y, z)
$$

\
**Fundamental Theorem for Line Integral** (applicable to vector fields with 2 or 3 variables)

(3D) Let C be a smooth curve joining the points A and B and given by $\vec r(t)$. Let f be a scalar differentiable function with a continuous gradient vector $\nabla f(x, y, z) = \vec F(x, y, z)$, Then we must have

$$
\int _C \vec F \cdot d \vec r = \int ^{terminal\ point\ B} _{terminal\ point\ A} \nabla f \cdot d \vec r = f(B) - f(A)
$$

\
**Test for Conservative Vector**

Let $\vec F(x, y, z)$ be a vector field on a connected and simply connected domain whose component functions have continuous first order partial derivatives. Then the vector field is conservative **if and only if**

$$
旋度\ (curl\ \vec F)(x, y, z) \stackrel{def}{=} (\nabla \times \vec F)(x, y, z) = \begin{vmatrix} \vec i & \vec j & \vec k \\ \frac{\partial}{\partial x} & \frac{\partial}{\partial y} & \frac{\partial}{\partial z} \\ M & N & P \end{vmatrix} = \vec 0
$$

\
**Some terminologies of region** (applicable to 2D and 3D)

- **open region**: if for every point (x, y) taken from the region R, there exists at least one disk centered at (x, y) that lies **entirely in R**
- **open connected region**: if R is oopen and any two points taken from R can be joined by a path the entirely lies in R
- **simple curve**: if the curve doesn't intersect itself anywhere between its endpoints, i.e. $\vec r(a) = \vec r(b)$ but $\vec r(t_1) \neq \vec r(t_2)$ when $a < t_1 < t_2 < b$
- **simply connected region**: a connected region such that every simply closed curve in R encloses only points that are in R
  - Intuitively speaking, a simply connected region contains no hole and cannot consist of 2 separate pieces

### Green's Theorem in Curl Form

[Table of Contents](#table-of-contents)

**Green's theorem in Circulation-Curl or Tangential Form**

Let C be a piecewise smooth, simple (means no cross) and closed curve

$$
\oint _C \vec F \cdot \vec T\ ds = \iint _R (Curl\ \vec F) \cdot \vec k\ dA
$$

The circle on the first integral sign means the integration around C is in the counterclockwise direction. Sometimes, this said to be in **positive orientation**

### Divergence Theorem

[Table of Contents](#table-of-contents)

**(Definition)** A surface S is said to be **orientable** if the normal vectors can vary continuously over the surface. i.e. counterexample: Mobius strip is not orientable.

**(Definition)** The **divergence of a vector field** $\vec F(x, y, z) = <M(x, y, z), N(x, y, z), P(x, y, z)$ is defined as a scalar function below

$$
div(\vec F) = \nabla \cdot \vec F = <\frac{\partial}{\partial x}, \frac{\partial}{\partial y}, \frac{\partial}{\partial z}> \cdot <M, N, P> = <\frac{\partial M}{\partial x}, \frac{\partial N}{\partial y}, \frac{\partial P}{\partial z}>
$$

\
**Theorem: Divergence Theorem 高斯散度定理**：将3D向量场的通量与该区域的边界联系起来
Suppose $\vec F(x, y, z)$ has continuous first partial derivatives, the S be a piecewise smooth orientable closed surface. $\vec n$ is the outward unit normal vector over the surface

$$
\iint _S \vec F \cdot \vec n\ dS = \iiint _D div(\vec F)\ dV
$$

Remark: The surface S must be a **closed surface enclosing a solid region having finite volume**

### Stokes' Theorem
[Table of Contents](#table-of-contents)

$$
\oint P dx +Q dy + R dz = \iint _{\sum} (\frac{\partial R}{\partial y} - \frac{\partial Q}{\partial z})\ dydz + (\frac{\partial P}{\partial z} - \frac{\partial R}{\partial x})\ dzdx + (\frac{\partial Q}{\partial x} - \frac{\partial P}{\partial y})\ dxdy\\
\text{ could be simply written as }\\
\oint _{\partial \sum} \vec v \cdot d \vec r = \iint _{\sum} \nabla \times \vec v \cdot d \vec S
$$