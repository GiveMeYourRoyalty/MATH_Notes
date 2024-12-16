# MATH2023 Summary Multivariable Calculus

## Table of Contents

- [MATH2023 Summary Multivariable Calculus](#math2023-summary-multivariable-calculus)
  - [Table of Contents](#table-of-contents)
    - [Retangular Integral =\> Polar Integral](#retangular-integral--polar-integral)
    - [Surface area](#surface-area)
    - [Triple Integral in Cylindrical Coordinates](#triple-integral-in-cylindrical-coordinates)
    - [Triple Integral in Spherical Coordinates](#triple-integral-in-spherical-coordinates)
    - [Line Integral](#line-integral)
    - [Vector Fields, Work Done, Flux](#vector-fields-work-done-flux)
    - [Conservative Vector Field](#conservative-vector-field)
    - [Green's Theorem in Curl Form](#greens-theorem-in-curl-form)
    - [Divergence Theorem](#divergence-theorem)

### Retangular Integral => Polar Integral
[Table of Contents](#table-of-contents)

\
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
\iiint_D F(x, y, z)\ dV = \int ^{\theta_{max}} _{\theta_{min}} \int ^{\phi_{max}} _{\phi _{min}} \int ^{\rho_{max}} _{\rho_{min}} F(\rho \sin \phi \cos \theta, \rho \sin \phi \sin \theta, \rho \cos \phi)\ \rho^2\ \sin \phi\ d\rho\ d\phi\ d\theta
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