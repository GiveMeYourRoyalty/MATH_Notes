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