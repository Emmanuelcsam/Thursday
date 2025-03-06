# Comprehensive Study Guide for Physics 401: Electromagnetism

## Introduction to Electromagnetism

This study guide covers fundamental concepts of electromagnetism as taught in Physics 401, focusing on electrostatics through Maxwell's equations. We'll carefully build your understanding from vector calculus foundations to advanced applications like the method of images.

## Table of Contents
1. [Vector Calculus Foundations](#vector-calculus-foundations)
2. [Electric Fields and Coulomb's Law](#electric-fields-and-coulombs-law)
3. [Gauss's Law](#gausss-law)
4. [Electric Potential](#electric-potential)
5. [Work and Energy in Electrostatic Fields](#work-and-energy-in-electrostatic-fields)
6. [Conductors](#conductors)
7. [Capacitors](#capacitors)
8. [Poisson's and Laplace's Equations](#poissons-and-laplaces-equations)
9. [Method of Images](#method-of-images)
10. [Separation of Variables](#separation-of-variables)
11. [Problem-Solving Strategies](#problem-solving-strategies)
12. [Exam Preparation Tips](#exam-preparation-tips)

## Vector Calculus Foundations

### Coordinate Systems

#### Cartesian Coordinates (x, y, z)
- Position vector: $\vec{r} = x\hat{x} + y\hat{y} + z\hat{z}$
- Differential length element: $d\vec{l} = dx\hat{x} + dy\hat{y} + dz\hat{z}$
- Volume element: $d\tau = dxdydz$

#### Cylindrical Coordinates (s, φ, z)
- Position vector: $\vec{r} = s\hat{s} + z\hat{z}$
- Differential length element: $d\vec{l} = ds\hat{s} + sd\phi\hat{\phi} + dz\hat{z}$
- Volume element: $d\tau = sdsd\phi dz$
- Conversion from Cartesian:
  - $s = \sqrt{x^2 + y^2}$
  - $\phi = \tan^{-1}(y/x)$
  - $z = z$

#### Spherical Coordinates (r, θ, φ)
- Position vector: $\vec{r} = r\hat{r}$
- Differential length element: $d\vec{l} = dr\hat{r} + rd\theta\hat{\theta} + r\sin\theta d\phi\hat{\phi}$
- Volume element: $d\tau = r^2\sin\theta dr d\theta d\phi$
- Conversion from Cartesian:
  - $r = \sqrt{x^2 + y^2 + z^2}$
  - $\theta = \cos^{-1}(z/r)$ (angle from z-axis)
  - $\phi = \tan^{-1}(y/x)$ (angle in xy-plane)

### Vector Calculus Operations

#### Gradient
The gradient of a scalar field f produces a vector field pointing in the direction of steepest increase of f.

In Cartesian coordinates:
$\nabla f = \frac{\partial f}{\partial x}\hat{x} + \frac{\partial f}{\partial y}\hat{y} + \frac{\partial f}{\partial z}\hat{z}$

In Spherical coordinates:
$\nabla f = \frac{\partial f}{\partial r}\hat{r} + \frac{1}{r}\frac{\partial f}{\partial \theta}\hat{\theta} + \frac{1}{r\sin\theta}\frac{\partial f}{\partial \phi}\hat{\phi}$

In Cylindrical coordinates:
$\nabla f = \frac{\partial f}{\partial s}\hat{s} + \frac{1}{s}\frac{\partial f}{\partial \phi}\hat{\phi} + \frac{\partial f}{\partial z}\hat{z}$

#### Divergence
The divergence of a vector field $\vec{A}$ measures the "outflow" of the vector field from a point.

In Cartesian coordinates:
$\nabla \cdot \vec{A} = \frac{\partial A_x}{\partial x} + \frac{\partial A_y}{\partial y} + \frac{\partial A_z}{\partial z}$

In Spherical coordinates:
$\nabla \cdot \vec{A} = \frac{1}{r^2}\frac{\partial}{\partial r}(r^2 A_r) + \frac{1}{r\sin\theta}\frac{\partial}{\partial \theta}(\sin\theta A_{\theta}) + \frac{1}{r\sin\theta}\frac{\partial A_{\phi}}{\partial \phi}$

In Cylindrical coordinates:
$\nabla \cdot \vec{A} = \frac{1}{s}\frac{\partial}{\partial s}(s A_s) + \frac{1}{s}\frac{\partial A_{\phi}}{\partial \phi} + \frac{\partial A_z}{\partial z}$

#### Curl
The curl of a vector field $\vec{A}$ measures the rotation or circulation of the field.

In Cartesian coordinates:
$\nabla \times \vec{A} = \left(\frac{\partial A_z}{\partial y} - \frac{\partial A_y}{\partial z}\right)\hat{x} + \left(\frac{\partial A_x}{\partial z} - \frac{\partial A_z}{\partial x}\right)\hat{y} + \left(\frac{\partial A_y}{\partial x} - \frac{\partial A_x}{\partial y}\right)\hat{z}$

#### Laplacian
The Laplacian of a scalar field is the divergence of the gradient:
$\nabla^2 f = \nabla \cdot (\nabla f)$

In Cartesian coordinates:
$\nabla^2 f = \frac{\partial^2 f}{\partial x^2} + \frac{\partial^2 f}{\partial y^2} + \frac{\partial^2 f}{\partial z^2}$

### Fundamental Theorems

#### Gradient Theorem
$\int_{\vec{a}}^{\vec{b}} (\nabla f) \cdot d\vec{l} = f(\vec{b}) - f(\vec{a})$

This states that the line integral of the gradient of a scalar field depends only on the values at the endpoints, not the path taken.

#### Divergence Theorem (Gauss's Theorem)
$\int_V (\nabla \cdot \vec{A}) d\tau = \oint_S \vec{A} \cdot d\vec{a}$

This relates the volume integral of the divergence to the flux through the closed surface bounding the volume.

#### Stokes' Theorem
$\int_S (\nabla \times \vec{A}) \cdot d\vec{a} = \oint_P \vec{A} \cdot d\vec{l}$

This relates the surface integral of the curl to the line integral around the boundary of the surface.

## Electric Fields and Coulomb's Law

### Coulomb's Law
The electric force between two point charges $q_1$ and $q_2$ separated by a distance $r$ is:

$\vec{F} = \frac{1}{4\pi\epsilon_0}\frac{q_1q_2}{r^2}\hat{r}$

where:
- $\epsilon_0 = 8.85 \times 10^{-12}$ C²/(N·m²) is the permittivity of free space
- $\hat{r}$ is the unit vector pointing from $q_1$ to $q_2$

### Electric Field
The electric field $\vec{E}$ at a point in space is defined as the force per unit charge that would be experienced by a test charge placed at that point:

$\vec{E} = \frac{\vec{F}}{q}$

For a point charge $q$, the electric field at a distance $r$ is:

$\vec{E} = \frac{1}{4\pi\epsilon_0}\frac{q}{r^2}\hat{r}$

### Electric Field from Continuous Charge Distributions

For a continuous charge distribution, the electric field is calculated by integrating over the charge distribution:

$\vec{E}(\vec{r}) = \frac{1}{4\pi\epsilon_0}\int \frac{\rho(\vec{r}')(\vec{r}-\vec{r}')}{|\vec{r}-\vec{r}'|^3}d\tau'$

where:
- $\rho(\vec{r}')$ is the volume charge density at position $\vec{r}'$
- $\vec{r}$ is the position where we want to know the electric field
- $\vec{r}'$ is the position of the source charge element
- $d\tau'$ is the volume element at position $\vec{r}'$

For different types of charge distributions:

1. **Volume charge density** ($\rho$): charge per unit volume (C/m³)
   $dq = \rho(\vec{r}')d\tau'$

2. **Surface charge density** ($\sigma$): charge per unit area (C/m²)
   $dq = \sigma(\vec{r}')dA'$

3. **Line charge density** ($\lambda$): charge per unit length (C/m)
   $dq = \lambda(\vec{r}')dl'$

### Principle of Superposition

For multiple charges, the net electric field is the vector sum of the fields due to each individual charge:

$\vec{E}_{total} = \sum_i \vec{E}_i$

For continuous distributions:

$\vec{E}_{total} = \int \vec{E}(\vec{r}')d\tau'$

### Electric Field Patterns

The electric field strength depends on the geometry of the charge distribution:

1. **Point charge**: $E \propto \frac{1}{r^2}$ (inverse square law)
2. **Infinite line charge**: $E \propto \frac{1}{r}$ (falls off more slowly)
3. **Infinite plane of charge**: $E = \text{constant}$ (independent of distance)

## Gauss's Law

### Integral Form
Gauss's Law relates the electric flux through a closed surface to the enclosed charge:

$\oint_S \vec{E} \cdot d\vec{a} = \frac{Q_{enclosed}}{\epsilon_0}$

where:
- $\oint_S$ indicates a closed surface integral
- $d\vec{a}$ is a differential area element pointing outward from the surface
- $Q_{enclosed}$ is the total charge enclosed by the surface

### Differential Form
The differential form of Gauss's Law is:

$\nabla \cdot \vec{E} = \frac{\rho}{\epsilon_0}$

This is one of Maxwell's equations and states that the divergence of the electric field at any point is proportional to the charge density at that point.

### Applications of Gauss's Law

Gauss's Law is most useful for finding the electric field in situations with high symmetry:

1. **Spherical symmetry** (e.g., spherical charge distributions)
2. **Cylindrical symmetry** (e.g., infinite line charges, cylindrical conductors)
3. **Planar symmetry** (e.g., infinite sheets of charge)

#### Example: Electric Field of a Uniform Spherical Charge

For a sphere of radius $R$ with uniform charge density $\rho$ and total charge $Q$:

1. **Inside the sphere** ($r < R$):
   $E(r) = \frac{1}{4\pi\epsilon_0}\frac{Qr}{R^3}$

2. **Outside the sphere** ($r > R$):
   $E(r) = \frac{1}{4\pi\epsilon_0}\frac{Q}{r^2}$

#### Example: Electric Field of an Infinite Sheet of Charge

For an infinite sheet with uniform surface charge density $\sigma$:

$E = \frac{\sigma}{2\epsilon_0}$

The field is perpendicular to the sheet and independent of distance.

#### Example: Electric Field of Two Parallel Charged Plates

For two parallel plates with equal and opposite charge densities $+\sigma$ and $-\sigma$:

1. **Between the plates**:
   $E = \frac{\sigma}{\epsilon_0}$

2. **Outside the plates**:
   $E = 0$ (the fields from the two plates cancel)

## Electric Potential

### Definition
The electric potential $V$ at a point is defined as the work per unit charge required to move a test charge from infinity to that point:

$V(\vec{r}) = -\int_{\infty}^{\vec{r}} \vec{E} \cdot d\vec{l}$

The electric potential is a scalar field measured in volts (V).

### Relation to Electric Field
The electric field is the negative gradient of the potential:

$\vec{E} = -\nabla V$

In Cartesian coordinates:

$\vec{E} = -\left(\frac{\partial V}{\partial x}\hat{x} + \frac{\partial V}{\partial y}\hat{y} + \frac{\partial V}{\partial z}\hat{z}\right)$

### Electric Potential of Point Charges

For a point charge $q$, the potential at a distance $r$ is:

$V = \frac{1}{4\pi\epsilon_0}\frac{q}{r}$

### Electric Potential from Continuous Charge Distributions

For a continuous charge distribution, the potential is:

$V(\vec{r}) = \frac{1}{4\pi\epsilon_0}\int \frac{\rho(\vec{r}')}{|\vec{r}-\vec{r}'|}d\tau'$

### Potential Energy of a System of Charges

The potential energy of a system of point charges is:

$U = \frac{1}{2}\sum_i q_i V_i$

where $V_i$ is the potential at the position of charge $q_i$ due to all other charges.

For continuous distributions:

$U = \frac{1}{2}\int \rho(\vec{r})V(\vec{r})d\tau$

### Equipotential Surfaces

Equipotential surfaces are surfaces on which the electric potential is constant. The electric field is always perpendicular to equipotential surfaces.

## Work and Energy in Electrostatic Fields

### Work and Potential Difference

The work required to move a charge $q$ from point A to point B in an electric field is:

$W = q(V_A - V_B) = -q\int_A^B \vec{E} \cdot d\vec{l}$

This work is independent of the path taken because the electrostatic field is conservative.

### Energy Stored in Electric Fields

The energy stored in an electric field is:

$U = \frac{\epsilon_0}{2}\int_V |\vec{E}|^2 d\tau$

This represents the energy density $\frac{\epsilon_0}{2}|\vec{E}|^2$ integrated over all space.

### Energy in a System of Charges

For a system of point charges, the energy can be calculated as:

$U = \frac{1}{2}\sum_{i}\sum_{j\neq i} \frac{1}{4\pi\epsilon_0}\frac{q_i q_j}{r_{ij}}$

For continuous charge distributions:

$U = \frac{1}{2}\int \rho(\vec{r})V(\vec{r})d\tau$

## Conductors

### Properties of Conductors in Electrostatic Equilibrium

1. **Electric field inside is zero** ($\vec{E} = 0$)
   - This occurs because free charges in the conductor move until they cancel out any internal electric field.

2. **Potential is constant** throughout the conductor
   - Since $\vec{E} = -\nabla V$, if $\vec{E} = 0$, then $V$ must be constant.

3. **Charge density in the bulk is zero** ($\rho = 0$)
   - All net charge resides on the surface.

4. **All net charge resides on the surface**
   - The surface charge density is denoted as $\sigma$.

5. **Electric field just outside the conductor is perpendicular to the surface**
   - The magnitude is $E = \frac{\sigma}{\epsilon_0}$
   - If there were a component parallel to the surface, charges would move to eliminate it.

### Conductors and Electric Fields

When a neutral conductor is placed in an external electric field:
1. Charges within the conductor redistribute
2. Positive charges move in the direction of the field
3. Negative charges move opposite to the field
4. This creates an induced electric field that cancels the external field inside the conductor
5. The total electric field inside becomes zero

### Charging by Induction

When a conductor is connected to a ground (large reservoir of charge):
1. Charges can flow freely between the conductor and the ground
2. The conductor maintains a fixed potential (usually zero)
3. If a charged object is brought near, it induces an opposite charge on the nearer side of the conductor
4. If the ground connection is removed while the charged object is still present, the conductor retains the induced charge

## Capacitors

### Definition
A capacitor consists of two conductors with equal and opposite charges. The capacitance $C$ is defined as:

$C = \frac{Q}{V}$

where:
- $Q$ is the magnitude of the charge on each conductor
- $V$ is the potential difference between the conductors

The unit of capacitance is the farad (F), equal to 1 coulomb/volt.

### Parallel Plate Capacitor

For a parallel plate capacitor with area $A$ and separation $d$ (assuming $d \ll \sqrt{A}$):

$C = \frac{\epsilon_0 A}{d}$

The electric field between the plates is uniform:

$E = \frac{\sigma}{\epsilon_0} = \frac{Q}{\epsilon_0 A}$

The potential difference is:

$V = Ed = \frac{Qd}{\epsilon_0 A}$

### Energy Stored in a Capacitor

The energy stored in a capacitor is:

$U = \frac{1}{2}CV^2 = \frac{1}{2}\frac{Q^2}{C} = \frac{1}{2}QV$

### Capacitors in Combination

For capacitors in parallel:
$C_{parallel} = C_1 + C_2 + ... + C_n$

For capacitors in series:
$\frac{1}{C_{series}} = \frac{1}{C_1} + \frac{1}{C_2} + ... + \frac{1}{C_n}$

## Poisson's and Laplace's Equations

### Poisson's Equation
Poisson's equation relates the Laplacian of the potential to the charge density:

$\nabla^2 V = -\frac{\rho}{\epsilon_0}$

This is derived from Gauss's law in differential form and the relationship between the electric field and potential.

### Laplace's Equation
In regions with no charge ($\rho = 0$), Poisson's equation reduces to Laplace's equation:

$\nabla^2 V = 0$

Solutions to Laplace's equation are called harmonic functions and have important mathematical properties:
1. The value of the potential at any point is the average of the potential on any surrounding sphere
2. The maximum and minimum values of the potential occur on the boundaries of the region
3. If the potential is known on all boundaries, there is a unique solution for the potential throughout the region

### Uniqueness Theorem

The uniqueness theorem states that:
1. The solution to Laplace's equation is uniquely determined if the potential is specified on all boundaries.
2. In a volume containing charges and surrounded by conductors, the electric field is uniquely determined if the total charge on each conductor is specified.

This theorem is crucial for the method of images and separation of variables techniques.

## Method of Images

### Concept
The method of images is a technique for solving electrostatic problems involving conductors by replacing the conductor and its induced charges with fictitious "image charges."

### Key Steps
1. Replace the conductor with one or more image charges positioned to maintain the same boundary conditions
2. Verify that the proposed solution satisfies:
   - Laplace's equation ($\nabla^2 V = 0$) in the region of interest
   - The appropriate boundary conditions on the conducting surfaces
3. Calculate the potential and electric field as if the image charges were real

### Example: Point Charge Near a Grounded Conducting Plane
For a point charge $+q$ at a distance $d$ above an infinite grounded conducting plane:

1. Replace the plane with an image charge $-q$ at a distance $d$ below where the plane would be
2. The potential is:
   $V(x,y,z) = \frac{1}{4\pi\epsilon_0}\left[\frac{q}{\sqrt{x^2+y^2+(z-d)^2}} - \frac{q}{\sqrt{x^2+y^2+(z+d)^2}}\right]$
3. At the plane ($z = 0$), $V = 0$, satisfying the boundary condition
4. The induced surface charge density on the plane is:
   $\sigma(x,y) = -\frac{q}{2\pi}\frac{d}{(x^2+y^2+d^2)^{3/2}}$
5. The total induced charge is $-q$
6. The force on the charge is:
   $F = \frac{1}{16\pi\epsilon_0}\frac{q^2}{d^2}$ (attractive)
7. The energy of the system is:
   $U = \frac{1}{16\pi\epsilon_0}\frac{q^2}{d}$

### Important Note
Image charges are fictitious; they don't physically exist. They are mathematical constructs that help solve the problem by creating the correct boundary conditions.

## Separation of Variables

### Concept
Separation of variables is a technique for solving partial differential equations like Laplace's equation by assuming the solution can be written as a product of functions, each depending on only one coordinate variable.

### General Approach
For Laplace's equation in Cartesian coordinates ($\nabla^2 V = 0$):

1. Assume a solution of the form $V(x,y,z) = X(x)Y(y)Z(z)$
2. Substitute into Laplace's equation:
   $\nabla^2 V = \frac{\partial^2 V}{\partial x^2} + \frac{\partial^2 V}{\partial y^2} + \frac{\partial^2 V}{\partial z^2} = 0$
3. Divide by $V = XYZ$ to get:
   $\frac{1}{X}\frac{d^2X}{dx^2} + \frac{1}{Y}\frac{d^2Y}{dy^2} + \frac{1}{Z}\frac{d^2Z}{dz^2} = 0$
4. Since each term depends on only one variable, they must each equal constants:
   $\frac{1}{X}\frac{d^2X}{dx^2} = -\alpha^2$
   $\frac{1}{Y}\frac{d^2Y}{dy^2} = -\beta^2$
   $\frac{1}{Z}\frac{d^2Z}{dz^2} = \gamma^2$
   where $\alpha^2 + \beta^2 = \gamma^2$
5. Solve these ordinary differential equations:
   $X(x) = A\cos(\alpha x) + B\sin(\alpha x)$ or $X(x) = Ce^{\alpha x} + De^{-\alpha x}$
   $Y(y) = E\cos(\beta y) + F\sin(\beta y)$ or $Y(y) = Ge^{\beta y} + He^{-\beta y}$
   $Z(z) = Ie^{\gamma z} + Je^{-\gamma z}$ or $Z(z) = K\cos(\gamma z) + L\sin(\gamma z)$
6. Apply boundary conditions to determine the constants
7. The general solution is often a sum or infinite series of these solutions

### Example: Rectangular Box
For a rectangular box with five grounded sides and one side at potential $V_0(x,y)$ at $z = 0$:

1. The solution must satisfy $V = 0$ at the boundaries $x = 0, x = a, y = 0, y = b, z = c$
2. The boundary condition at $z = 0$ is $V(x,y,0) = V_0(x,y)$
3. The solution has the form:
   $V(x,y,z) = \sum_{m=1}^{\infty}\sum_{n=1}^{\infty} A_{mn}\sin\left(\frac{m\pi x}{a}\right)\sin\left(\frac{n\pi y}{b}\right)\sinh\left(\gamma_{mn}(c-z)\right)$
   where $\gamma_{mn} = \pi\sqrt{\frac{m^2}{a^2}+\frac{n^2}{b^2}}$
4. The coefficients $A_{mn}$ are determined by:
   $A_{mn} = \frac{4}{ab\sinh(\gamma_{mn}c)}\int_0^a\int_0^b V_0(x,y)\sin\left(\frac{m\pi x}{a}\right)\sin\left(\frac{n\pi y}{b}\right)dxdy$

# Detailed Problem-Solving Strategies for Electromagnetism

## General Approach - Detailed Examples

Let me walk through an extremely detailed example that shows how to apply the general problem-solving approach to a specific electromagnetism problem.

### Example Problem: A hollow spherical conductor of inner radius a and outer radius b carries a total charge Q. A point charge q is placed at the center. Find the electric field and potential everywhere.

#### Step 1: Identify the symmetry of the problem
This problem has spherical symmetry around the center. The charge distributions (both the point charge and any induced charges on the conductor) will be spherically symmetric. All physical quantities will depend only on the radial distance r from the center.

When identifying symmetry, look for:
- Point charges or spherical charge distributions → spherical symmetry
- Infinite line charges or cylindrical objects → cylindrical symmetry
- Infinite planes of charge → planar symmetry

The symmetry in this problem is clearly spherical because:
- The hollow spherical conductor creates concentric spherical boundaries
- The point charge at the center maintains the spherical symmetry
- There's no aspect of the problem that breaks this symmetry

#### Step 2: Choose the appropriate coordinate system based on the symmetry
For spherical symmetry, we use spherical coordinates (r, θ, φ). In this coordinate system:
- The position is specified by distance r from origin
- Polar angle θ (measured from the z-axis)
- Azimuthal angle φ (measured in the xy-plane)

Since the problem has perfect spherical symmetry, the electric field will have only a radial component E = E(r)r̂, and the potential will depend only on r: V = V(r).

#### Step 3: Determine the appropriate method
With high spherical symmetry, Gauss's law is the most efficient approach. We'll use a spherical Gaussian surface centered at the origin.

Why Gauss's law is appropriate here:
- The charge distribution has spherical symmetry
- We can draw a Gaussian surface (a sphere) where E is constant in magnitude and perpendicular to the surface
- This makes the surface integral in Gauss's law straightforward to evaluate

#### Step 4: Solve for the potential or electric field
We need to consider three regions:
1. Inside the hollow space (r < a)
2. Within the conductor (a < r < b)
3. Outside the conductor (r > b)

For Region 1 (r < a):
Using Gauss's law: ∮E⋅dA = Q_enclosed/ε₀
With a spherical Gaussian surface of radius r < a:
- Q_enclosed = q (just the point charge)
- E is constant in magnitude and radial, so E⋅dA = E·4πr²
- Therefore: E·4πr² = q/ε₀
- Solving for E: E(r) = (1/4πε₀)(q/r²)r̂
- The electric field is the same as that of a point charge in empty space

For Region 2 (a < r < b):
Inside a conductor in electrostatic equilibrium, the electric field must be zero: E(r) = 0.

For Region 3 (r > b):
With a Gaussian surface of radius r > b:
- Q_enclosed = q + Q (the point charge plus the conductor's charge)
- Therefore: E(r) = (1/4πε₀)((q+Q)/r²)r̂
- The field is that of a point charge with total charge q+Q

Now for the potential, we integrate the electric field:
- V(r) = -∫E(r)·dr
- For r < a: V(r) = (1/4πε₀)(q/r) + constant₁
- For a < r < b: V(r) = constant₂ (since E = 0, the potential is constant)
- For r > b: V(r) = (1/4πε₀)((q+Q)/r) + constant₃

The constants are determined by requiring the potential to be continuous at r = a and r = b, and usually setting V(∞) = 0.

#### Step 5: Verify the solution
To verify our solution:
1. Check continuity of potential at boundaries r = a and r = b
2. Check that the electric field E = -∇V
3. Verify Gauss's law is satisfied in each region
4. Confirm that E = 0 inside the conductor, as required
5. Ensure the total charge on the conductor is Q

For example, the potential at r = a from inside must equal the potential at r = a from within the conductor:
(1/4πε₀)(q/a) + constant₁ = constant₂

Similarly at r = b.

Setting V(∞) = 0 means constant₃ = 0.

From these conditions, we can fully determine the potential and electric field everywhere.

## Using Gauss's Law - Detailed Example

### Example Problem: An infinitely long cylindrical insulator of radius R has a uniform volume charge density ρ. Find the electric field everywhere.

#### Step 1: Identify the symmetry of the problem
This problem has cylindrical symmetry. The charge distribution extends infinitely along the z-axis and is uniform in the radial direction out to radius R.

The charge density is uniform within the cylinder, and there is no variation along the length (z-direction) or with angle (φ-direction). This perfect cylindrical symmetry means the electric field will only have a radial component.

#### Step 2: Draw an appropriate Gaussian surface that aligns with the symmetry
For cylindrical symmetry, we use a cylindrical Gaussian surface:
- For points inside the charged cylinder (s < R), use a cylindrical Gaussian surface of radius s and length L centered on the axis.
- For points outside the charged cylinder (s > R), use a similar cylindrical Gaussian surface of radius s > R.

The cylindrical surface consists of:
- Two circular end caps (perpendicular to the z-axis)
- A cylindrical side surface (parallel to the z-axis)

Since the electric field will point radially outward (due to symmetry), it will be:
- Parallel to the end caps (so E·dA = 0 on the end caps)
- Perpendicular to the cylindrical side (so E·dA = E·dA on the side)

#### Step 3: Calculate the enclosed charge
For a cylindrical Gaussian surface of radius s and length L:

**Inside the cylinder (s < R)**:
- Volume enclosed = πs²L
- Charge enclosed = ρ × volume = ρπs²L

**Outside the cylinder (s > R)**:
- Volume enclosed that contains charge = πR²L
- Charge enclosed = ρπR²L (all of the charge in a length L)

#### Step 4: Use Gauss's law to find the electric field
Gauss's law states: ∮E·dA = Q_enclosed/ε₀

**Inside the cylinder (s < R)**:
- The flux only comes from the cylindrical side: E·(2πsL) = ρπs²L/ε₀
- Solving for E: E(s) = (ρs/2ε₀)ŝ
- The electric field increases linearly with distance from the axis

**Outside the cylinder (s > R)**:
- The flux is again only from the cylindrical side: E·(2πsL) = ρπR²L/ε₀
- Solving for E: E(s) = (ρR²/2ε₀s)ŝ
- The electric field decreases as 1/s outside the cylinder

#### Step 5: Calculate the potential by integrating the electric field
We find the potential by integrating: V(s) = -∫E(s)·ds

**Inside the cylinder (s < R)**:
- V(s) = -∫(ρs/2ε₀)ds = -(ρs²/4ε₀) + C₁

**Outside the cylinder (s > R)**:
- V(s) = -∫(ρR²/2ε₀s)ds = (ρR²/2ε₀)ln(s) + C₂

The constants C₁ and C₂ are determined by:
- Setting a reference point for zero potential (often at infinity)
- Ensuring the potential is continuous at s = R

If we set V(∞) = 0, then:
- Since ln(s) → ∞ as s → ∞, we must have C₂ = 0
- From continuity at s = R: -(ρR²/4ε₀) + C₁ = (ρR²/2ε₀)ln(R)
- Solving: C₁ = (ρR²/4ε₀) + (ρR²/2ε₀)ln(R)

Therefore:
- Inside: V(s) = -(ρs²/4ε₀) + (ρR²/4ε₀) + (ρR²/2ε₀)ln(R)
- Outside: V(s) = (ρR²/2ε₀)ln(s) for s > R

This gives us the complete solution for the electric field and potential everywhere.

## Using the Method of Images - Detailed Example

### Example Problem: A point charge q is placed at position (0, 0, d) above an infinite grounded conducting plane in the xy-plane. Find the potential and electric field everywhere above the plane, the surface charge density induced on the plane, and the force on the charge.

#### Step 1: Replace conductors with image charges
The key insight in the method of images is to replace the conductor with an appropriate image charge that creates the same boundary conditions.

For a point charge q at distance d above a grounded conducting plane, we place an image charge -q at position (0, 0, -d) below the plane.

Detailed reasoning:
- The potential from a point charge q at position (0, 0, d) is: V₁(x,y,z) = (1/4πε₀)(q/√((x² + y² + (z-d)²))
- The potential from an image charge -q at (0, 0, -d) is: V₂(x,y,z) = (1/4πε₀)(-q/√((x² + y² + (z+d)²))
- The total potential is: V(x,y,z) = V₁ + V₂

We need to verify this satisfies our boundary condition: V(x,y,0) = 0 (the plane is grounded).
When z = 0:
- V₁(x,y,0) = (1/4πε₀)(q/√((x² + y² + d²))
- V₂(x,y,0) = (1/4πε₀)(-q/√((x² + y² + d²))
- V(x,y,0) = V₁ + V₂ = 0 ✓

This confirms our image charge setup creates the correct boundary condition.

#### Step 2: Check that the potential on the conducting surfaces is correct
As we just verified, the potential at z = 0 (the conducting plane) is V(x,y,0) = 0, which matches our boundary condition that the conducting plane is grounded.

Another way to check is to recognize that any point on the xy-plane is equidistant from the real charge and the image charge, so the potentials cancel exactly.

#### Step 3: Calculate the potential and field using the superposition principle
Now we can find the potential and electric field everywhere above the plane (z > 0).

**Potential**:
V(x,y,z) = (1/4πε₀)(q/√((x² + y² + (z-d)²)) - q/√((x² + y² + (z+d)²)))

**Electric field**:
E = -∇V

Computing this gradient:
- Ex = (1/4πε₀)q·x·[(x² + y² + (z-d)²)^(-3/2) - (x² + y² + (z+d)²)^(-3/2)]
- Ey = (1/4πε₀)q·y·[(x² + y² + (z-d)²)^(-3/2) - (x² + y² + (z+d)²)^(-3/2)]
- Ez = (1/4πε₀)q·[-(z-d)·(x² + y² + (z-d)²)^(-3/2) + (z+d)·(x² + y² + (z+d)²)^(-3/2)]

This gives us the electric field at any point (x,y,z) above the plane.

**Surface charge density on the plane**:
The surface charge density induced on the conducting plane is:
σ(x,y) = -ε₀Ez|z=0

At z = 0, Ez becomes:
Ez|z=0 = (1/4πε₀)q·[d·(x² + y² + d²)^(-3/2) + d·(x² + y² + d²)^(-3/2)]
       = (1/2πε₀)q·d·(x² + y² + d²)^(-3/2)

Therefore:
σ(x,y) = -ε₀Ez|z=0 = -(1/2π)q·d·(x² + y² + d²)^(-3/2)

This negative charge density shows that the conducting plane has induced negative charges to neutralize the effect of the positive charge above it.

**Total induced charge**:
The total induced charge on the plane is:
Qtotal = ∫∫σ(x,y)dxdy = ∫₀^(2π)∫₀^∞σ(r)rdrdφ = -q

This confirms that the total induced charge is exactly -q, which equals the magnitude of the image charge.

**Force on the charge**:
The force on charge q is due to the electric field from the image charge only:
F = qEimage = (1/4πε₀)(q·(-q))/(2d)² = -(1/16πε₀)(q²/d²)

The negative sign indicates the force is attractive toward the plane.

#### Step 4: Remember that energy calculations must only consider real charges
The energy of the system is NOT calculated as the interaction energy between the real charge and the image charge. That would give:
U = (1/4πε₀)(q·(-q)/(2d)) = -(1/8πε₀)(q²/d)

Instead, the correct energy is:
U = (1/16πε₀)(q²/d)

This is half the nominal energy of the two charges because the image charge is fictitious. The correct way to calculate energy is to consider:
- The work needed to bring the real charge from infinity to its position
- The energy stored in the electric field

The factor of 1/2 comes from the fact that the conductor allows charges to flow freely without requiring work to move them.

## Using Separation of Variables - Detailed Example

### Example Problem: A rectangular box with sides at x = 0, x = a, y = 0, y = b, z = 0, and z = c has five grounded sides (V = 0) at x = 0, x = a, y = 0, y = b, and z = c. The bottom side at z = 0 is maintained at a potential V(x,y,0) = V₀sin(πx/a). Find the potential everywhere inside the box.

#### Step 1: Write the solution as a product of functions
We need to solve Laplace's equation ∇²V = 0 inside the box with the given boundary conditions.

For rectangular geometry, we assume a separable solution of the form:
V(x,y,z) = X(x)Y(y)Z(z)

This assumption is justified because:
- The rectangular geometry aligns perfectly with Cartesian coordinates
- The boundary conditions are defined on planes of constant x, y, or z
- Solutions to Laplace's equation in Cartesian coordinates often have this separable form

#### Step 2: Substitute into Laplace's equation
Laplace's equation in Cartesian coordinates is:
∇²V = ∂²V/∂x² + ∂²V/∂y² + ∂²V/∂z² = 0

Substituting our separable form:
Y(y)Z(z)·d²X/dx² + X(x)Z(z)·d²Y/dy² + X(x)Y(y)·d²Z/dz² = 0

Dividing by X(x)Y(y)Z(z):
(1/X)·d²X/dx² + (1/Y)·d²Y/dy² + (1/Z)·d²Z/dz² = 0

#### Step 3: Separate into independent ordinary differential equations
Since each term depends on only one variable, and their sum is zero for all (x,y,z), each term must equal a constant:

(1/X)·d²X/dx² = -α²
(1/Y)·d²Y/dy² = -β²
(1/Z)·d²Z/dz² = α² + β²

where α² and β² are separation constants with α² + β² > 0.

This gives us three ordinary differential equations:
d²X/dx² + α²X = 0
d²Y/dy² + β²Y = 0
d²Z/dz² - (α² + β²)Z = 0

#### Step 4: Solve these equations with appropriate boundary conditions
The general solutions to these equations are:

X(x) = A cos(αx) + B sin(αx)
Y(y) = C cos(βy) + D sin(βy)
Z(z) = E cosh(γz) + F sinh(γz)

where γ² = α² + β².

Now we apply the boundary conditions:

1. V = 0 at x = 0:
   X(0) = A = 0 → X(x) = B sin(αx)

2. V = 0 at x = a:
   X(a) = B sin(αa) = 0 → αa = nπ, n = 1,2,3,...
   So α = nπ/a and X(x) = B sin(nπx/a)

3. V = 0 at y = 0:
   Y(0) = C = 0 → Y(y) = D sin(βy)

4. V = 0 at y = b:
   Y(b) = D sin(βb) = 0 → βb = mπ, m = 1,2,3,...
   So β = mπ/b and Y(y) = D sin(mπy/b)

5. V = 0 at z = c:
   Z(c) = E cosh(γc) + F sinh(γc) = 0 → F = -E cosh(γc)/sinh(γc)
   So Z(z) = E [cosh(γz) - cosh(γc)·sinh(γz)/sinh(γc)]
   Simplifying: Z(z) = E·sinh(γ(c-z))/sinh(γc)

where γ = π√((n/a)² + (m/b)²)

#### Step 5: Form the general solution as a superposition of these solutions
The complete solution is a superposition of all possible solutions:

V(x,y,z) = ∑∑ A_nm sin(nπx/a) sin(mπy/b) sinh(γ_nm(c-z))/sinh(γ_nm c)

where γ_nm = π√((n/a)² + (m/b)²)

Finally, we determine the coefficients A_nm using the boundary condition at z = 0:

V(x,y,0) = ∑∑ A_nm sin(nπx/a) sin(mπy/b) = V₀ sin(πx/a)

Comparing terms, we see that:
- Only n = 1 terms contribute
- Only m-odd terms might be non-zero
- From orthogonality of the sines: A_1m = 0 for m ≠ 1

Therefore:
V(x,y,z) = V₀ sin(πx/a) sinh(γ₁₁(c-z))/sinh(γ₁₁c)

where γ₁₁ = π√(1/a² + 1/b²)

This is the complete solution to the potential inside the box.

## Exam Preparation - Detailed Example Questions

### Gauss's Law Applications

**Example Question 1:** A solid non-conducting sphere of radius R has a charge density that varies with distance from the center as ρ(r) = ρ₀(1 - r/R). Calculate the electric field everywhere and sketch its magnitude as a function of distance from the center.

**Step-by-step solution:**
1. Identify the symmetry: Spherical symmetry means E = E(r)r̂
2. Set up Gauss's law: ∮E·dA = Q_enclosed/ε₀
3. Calculate the enclosed charge for r < R:
   Q_enclosed = ∫ρ(r')4πr'²dr' = ∫ρ₀(1-r'/R)4πr'²dr' from 0 to r
   = 4πρ₀[r³/3 - r⁴/(4R)] = (4πρ₀R³/12)[4(r/R)³ - 3(r/R)⁴]
4. For r < R, Gauss's law gives:
   E(r)·4πr² = Q_enclosed/ε₀
   E(r) = (ρ₀R³/3ε₀r²)[4(r/R)³ - 3(r/R)⁴]
   = (ρ₀R/3ε₀)[4(r/R) - 3(r/R)²]
5. For r > R, the enclosed charge is the total charge of the sphere:
   Q_total = ∫ρ₀(1-r'/R)4πr'²dr' from 0 to R
   = (4πρ₀R³/12)[4 - 3] = πρ₀R³/3
6. For r > R, the field is:
   E(r) = (1/4πε₀)(Q_total/r²) = (ρ₀R³/12ε₀r²)
7. Verify the field is continuous at r = R:
   Letting r = R in the r < R solution:
   E(R) = (ρ₀R/3ε₀)[4 - 3] = ρ₀R/3ε₀
   Letting r = R in the r > R solution:
   E(R) = (ρ₀R³/12ε₀R²) = ρ₀R/12ε₀
   The field is NOT continuous at r = R, indicating a surface charge at r = R.

**Sketch:** The field increases from zero at the origin to a maximum inside the sphere, then decreases. At r = R, there's a discontinuity. For r > R, the field decreases as 1/r².

**Example Question 2:** Explain why Gauss's law works particularly well for certain geometries but not for others. Provide specific examples.

**Answer:** Gauss's law works efficiently when:
1. The charge distribution has high symmetry
2. A Gaussian surface can be drawn where:
   - The electric field is either constant in magnitude and perpendicular to the surface
   - Or the electric field is parallel to the surface
   - Or the electric field is zero on parts of the surface

In these cases, the surface integral ∮E·dA simplifies dramatically.

**Specific examples where Gauss's law works well:**
- Spherical charge distributions: Using a spherical Gaussian surface, E is constant in magnitude and perpendicular to the surface
- Infinite line charges: Using a cylindrical Gaussian surface, E is constant and perpendicular to the cylindrical side
- Infinite plane charges: Using a cylindrical "pillbox" with faces parallel to the plane, E is constant and perpendicular to the top and bottom faces

**Examples where Gauss's law is difficult to apply:**
- A finite line charge: No simple Gaussian surface exists where E has constant magnitude on the surface
- A dipole: The field is not perpendicular to any simple closed surface
- Any asymmetric charge distribution: The surface integral becomes complex and no simpler than direct integration

In these cases, direct integration of the charge distribution is usually more practical.

### Method of Images

**Example Question:** Two infinite grounded conducting planes meet at a right angle. A point charge q is placed at coordinates (d, d, 0) in the region between the planes, where the planes are at x = 0 and y = 0. Find:
a) The image charges required to solve this problem
b) The potential everywhere in the first quadrant
c) The force on the charge

**Step-by-step solution:**

a) **Image charges:**
   1. Due to the plane at x = 0, we need an image charge -q at (-d, d, 0)
   2. Due to the plane at y = 0, we need an image charge -q at (d, -d, 0)
   3. The image of the image charge -q at (-d, d, 0) reflected in the y = 0 plane gives a charge +q at (-d, -d, 0)

   Total: Four charges:
   - Real charge: +q at (d, d, 0)
   - Image charges: -q at (-d, d, 0), -q at (d, -d, 0), and +q at (-d, -d, 0)

b) **Potential:**
   The potential at any point (x, y, z) in the first quadrant is:
   
   V(x,y,z) = (1/4πε₀)[
      q/√((x-d)² + (y-d)² + z²) - 
      q/√((x+d)² + (y-d)² + z²) - 
      q/√((x-d)² + (y+d)² + z²) + 
      q/√((x+d)² + (y+d)² + z²)
   ]

   Verify this satisfies V = 0 at x = 0:
   At x = 0: 
   V(0,y,z) = (1/4πε₀)[
      q/√(d² + (y-d)² + z²) - 
      q/√(d² + (y-d)² + z²) - 
      q/√(d² + (y+d)² + z²) + 
      q/√(d² + (y+d)² + z²)
   ] = 0 ✓

   Similarly, V = 0 at y = 0.

c) **Force on the charge:**
   The force comes from the electric field of the image charges only:
   
   F = q(E₁ + E₂ + E₃)
   
   where E₁, E₂, E₃ are the fields from the three image charges.
   
   From Coulomb's law:
   E₁ = (1/4πε₀)(-q)/(2d)² in the -x direction
   E₂ = (1/4πε₀)(-q)/(2d)² in the -y direction
   E₃ = (1/4πε₀)(q)/(2√2d)² at 45° into the first quadrant
   
   Combining and simplifying:
   F = (q²/4πε₀)[1/(4d²)(-x̂) + 1/(4d²)(-ŷ) + 1/(8d²)(x̂+ŷ)/√2]
   
   Evaluating the components:
   Fx = -(q²/16πε₀d²)[1 - 1/(2√2)] ≈ -(q²/16πε₀d²)·0.65
   Fy = -(q²/16πε₀d²)[1 - 1/(2√2)] ≈ -(q²/16πε₀d²)·0.65
   
   The force pulls the charge towards both planes with slightly reduced magnitude due to the positive image charge at the corner.

### Separation of Variables

**Example Question:** A cube with sides of length L has five sides grounded (V = 0) and one side (at z = L) held at a potential V(x,y,L) = V₀. Find the potential inside the cube.

**Step-by-step solution:**

1. **Set up the problem:**
   - Laplace's equation: ∇²V = 0
   - Boundary conditions:
     * V(0,y,z) = V(L,y,z) = V(x,0,z) = V(x,L,z) = V(x,y,0) = 0
     * V(x,y,L) = V₀

2. **Assume a separable solution:**
   V(x,y,z) = X(x)Y(y)Z(z)
   
   Substituting into Laplace's equation and dividing by XYZ:
   (1/X)·d²X/dx² + (1/Y)·d²Y/dy² + (1/Z)·d²Z/dz² = 0
   
   This leads to three equations:
   d²X/dx² + α²X = 0
   d²Y/dy² + β²Y = 0
   d²Z/dz² - (α² + β²)Z = 0
   
   with α² + β² > 0.

3. **Solve each equation with boundary conditions:**
   
   For X(x):
   - General solution: X(x) = A cos(αx) + B sin(αx)
   - Boundary condition X(0) = 0 gives A = 0
   - Boundary condition X(L) = 0 gives sin(αL) = 0, so α = nπ/L for n = 1,2,3,...
   - Therefore: X(x) = B sin(nπx/L)
   
   For Y(y):
   - Similar analysis gives Y(y) = C sin(mπy/L) for m = 1,2,3,...
   - where β = mπ/L
   
   For Z(z):
   - General solution: Z(z) = D sinh(γz) + E cosh(γz), where γ = π√((n/L)² + (m/L)²)
   - Boundary condition Z(0) = 0 gives E = 0
   - Therefore: Z(z) = D sinh(γz)

4. **Form the general solution:**
   V(x,y,z) = ∑∑ A_nm sin(nπx/L) sin(mπy/L) sinh(γ_nm z)
   
   where γ_nm = π√((n/L)² + (m/L)²)/L

5. **Apply the final boundary condition at z = L:**
   V(x,y,L) = ∑∑ A_nm sin(nπx/L) sin(mπy/L) sinh(γ_nm L) = V₀
   
   To find A_nm, multiply both sides by sin(pπx/L)sin(qπy/L) and integrate over the surface:
   
   ∫₀ᴸ∫₀ᴸ V₀·sin(pπx/L)sin(qπy/L) dxdy = ∑∑ A_nm·sinh(γ_nm L)·∫₀ᴸ∫₀ᴸ sin(nπx/L)sin(mπy/L)sin(pπx/L)sin(qπy/L) dxdy
   
   Using the orthogonality of sine functions:
   
   ∫₀ᴸ∫₀ᴸ sin(nπx/L)sin(pπx/L) dxdy = (L²/4)δ_np δ_mq
   
   This gives:
   A_nm = (4V₀/L²)/sinh(γ_nm L) · ∫₀ᴸ∫₀ᴸ sin(nπx/L)sin(mπy/L) dxdy
   
   Since V₀ is constant, this simplifies to:
   
Let me continue with the detailed separation of variables example and then provide more worked examples for exam preparation topics.

## Separation of Variables (continued)

   Since V₀ is constant, the integral simplifies to:
   
   A_nm = (4V₀/L²)/sinh(γ_nm L) · (L/nπ)(1-cos(nπ)) · (L/mπ)(1-cos(mπ))
   
   Evaluating the terms:
   - (1-cos(nπ)) = 0 for even n and = 2 for odd n
   - (1-cos(mπ)) = 0 for even m and = 2 for odd m
   
   Therefore:
   A_nm = (16V₀/(π²nm))/sinh(γ_nm L) for odd n and odd m
   A_nm = 0 for even n or even m
   
6. **Final solution:**
   V(x,y,z) = (16V₀/π²)∑∑ sin(nπx/L)sin(mπy/L)sinh(γ_nm z)/(nm·sinh(γ_nm L))
   
   where the sum is over odd n and odd m, and γ_nm = π√((n/L)² + (m/L)²).
   
   The dominant term will be n=m=1, as higher terms diminish rapidly due to the nm product in the denominator and the increasing sinh term.

7. **Verification:**
   We can verify that:
   - The solution satisfies Laplace's equation (by construction)
   - The boundary conditions at x = 0, x = L, y = 0, y = L, and z = 0 are satisfied (all sines are zero)
   - The boundary condition at z = L approximates V₀ (verified by Fourier analysis)

This example demonstrates all the key steps in the separation of variables technique for a 3D boundary value problem with mixed boundary conditions.

## More Detailed Exam Preparation Examples

### Vector Calculus Operations in Different Coordinate Systems

**Example Question:** Calculate the divergence and curl of the vector field $\vec{A} = r\sin\theta\cos\phi\,\hat{r} + r\cos\theta\sin\phi\,\hat{\theta} + r\sin\theta\sin\phi\,\hat{\phi}$ in spherical coordinates.

**Step-by-step solution:**

1. **Identify the components:**
   $A_r = r\sin\theta\cos\phi$
   $A_\theta = r\cos\theta\sin\phi$
   $A_\phi = r\sin\theta\sin\phi$

2. **Calculate the divergence using the formula in spherical coordinates:**
   $\nabla \cdot \vec{A} = \frac{1}{r^2}\frac{\partial}{\partial r}(r^2 A_r) + \frac{1}{r\sin\theta}\frac{\partial}{\partial \theta}(\sin\theta A_{\theta}) + \frac{1}{r\sin\theta}\frac{\partial A_{\phi}}{\partial \phi}$

   Calculating each term:
   - $\frac{1}{r^2}\frac{\partial}{\partial r}(r^2 A_r) = \frac{1}{r^2}\frac{\partial}{\partial r}(r^3\sin\theta\cos\phi) = \frac{1}{r^2} \cdot 3r^2\sin\theta\cos\phi = 3\sin\theta\cos\phi$
   
   - $\frac{1}{r\sin\theta}\frac{\partial}{\partial \theta}(\sin\theta A_{\theta}) = \frac{1}{r\sin\theta}\frac{\partial}{\partial \theta}(r\sin\theta\cos\theta\sin\phi) = \frac{1}{r\sin\theta} \cdot r(\cos^2\theta\sin\phi - \sin^2\theta\sin\phi) = \frac{\cos^2\theta - \sin^2\theta}{\sin\theta}\sin\phi = \frac{\cos(2\theta)}{\sin\theta}\sin\phi$
   
   - $\frac{1}{r\sin\theta}\frac{\partial A_{\phi}}{\partial \phi} = \frac{1}{r\sin\theta}\frac{\partial}{\partial \phi}(r\sin\theta\sin\phi) = \frac{1}{r\sin\theta} \cdot r\sin\theta\cos\phi = \cos\phi$

   Adding all terms:
   $\nabla \cdot \vec{A} = 3\sin\theta\cos\phi + \frac{\cos(2\theta)}{\sin\theta}\sin\phi + \cos\phi$

3. **Calculate the curl using the formula in spherical coordinates:**
   $(\nabla \times \vec{A})_r = \frac{1}{r\sin\theta}\left[ \frac{\partial}{\partial \theta}(\sin\theta A_{\phi}) - \frac{\partial A_{\theta}}{\partial \phi} \right]$
   
   $(\nabla \times \vec{A})_{\theta} = \frac{1}{r}\left[ \frac{1}{\sin\theta}\frac{\partial A_r}{\partial \phi} - \frac{\partial}{\partial r}(r A_{\phi}) \right]$
   
   $(\nabla \times \vec{A})_{\phi} = \frac{1}{r}\left[ \frac{\partial}{\partial r}(r A_{\theta}) - \frac{\partial A_r}{\partial \theta} \right]$

   Calculating each component:
   
   - $(\nabla \times \vec{A})_r = \frac{1}{r\sin\theta}\left[ \frac{\partial}{\partial \theta}(r\sin^2\theta\sin\phi) - \frac{\partial}{\partial \phi}(r\cos\theta\sin\phi) \right]$
     $= \frac{1}{r\sin\theta}\left[ r\sin\phi \cdot 2\sin\theta\cos\theta - r\cos\theta\cos\phi \right]$
     $= \frac{2\cos\theta\sin\phi - \frac{\cos\theta\cos\phi}{\sin\theta}}{\sin\theta}$

   - $(\nabla \times \vec{A})_{\theta} = \frac{1}{r}\left[ \frac{1}{\sin\theta}\frac{\partial}{\partial \phi}(r\sin\theta\cos\phi) - \frac{\partial}{\partial r}(r \cdot r\sin\theta\sin\phi) \right]$
     $= \frac{1}{r}\left[ \frac{r\sin\theta \cdot (-\sin\phi)}{\sin\theta} - (2r\sin\theta\sin\phi) \right]$
     $= \frac{-\sin\phi - 2\sin\theta\sin\phi}{r}$

   - $(\nabla \times \vec{A})_{\phi} = \frac{1}{r}\left[ \frac{\partial}{\partial r}(r \cdot r\cos\theta\sin\phi) - \frac{\partial}{\partial \theta}(r\sin\theta\cos\phi) \right]$
     $= \frac{1}{r}\left[ 2r\cos\theta\sin\phi - r\cos\theta\cos\phi + r\sin\theta\sin\phi \right]$
     $= 2\cos\theta\sin\phi - \cos\theta\cos\phi + \sin\theta\sin\phi$

   Therefore:
   $\nabla \times \vec{A} = \left(\frac{2\cos\theta\sin\phi - \frac{\cos\theta\cos\phi}{\sin\theta}}{\sin\theta}\right)\hat{r} + \left(\frac{-\sin\phi - 2\sin\theta\sin\phi}{r}\right)\hat{\theta} + (2\cos\theta\sin\phi - \cos\theta\cos\phi + \sin\theta\sin\phi)\hat{\phi}$

This example shows the application of vector calculus operations in spherical coordinates, which requires careful attention to the coordinate-specific formulas.

### Relationship Between Electric Field and Potential

**Example Question:** A point charge q is placed at the origin. Another point charge 2q is placed at (0,0,d). Find the potential V(x,y,z) and the electric field at the point (0,0,d/2).

**Step-by-step solution:**

1. **Calculate the potential at (0,0,d/2):**
   The potential due to both charges is:
   
   $V(x,y,z) = \frac{1}{4\pi\epsilon_0}\left(\frac{q}{\sqrt{x^2+y^2+z^2}} + \frac{2q}{\sqrt{x^2+y^2+(z-d)^2}}\right)$
   
   At the point (0,0,d/2):
   $V(0,0,d/2) = \frac{1}{4\pi\epsilon_0}\left(\frac{q}{\sqrt{(d/2)^2}} + \frac{2q}{\sqrt{(d/2)^2}}\right) = \frac{1}{4\pi\epsilon_0}\frac{3q}{d/2} = \frac{6q}{4\pi\epsilon_0 d}$

2. **Calculate the electric field at (0,0,d/2):**
   Method 1 - Using $\vec{E} = -\nabla V$:
   
   $\frac{\partial V}{\partial x} = \frac{1}{4\pi\epsilon_0}\left(-\frac{qx}{(x^2+y^2+z^2)^{3/2}} - \frac{2qx}{(x^2+y^2+(z-d)^2)^{3/2}}\right)$
   
   $\frac{\partial V}{\partial y} = \frac{1}{4\pi\epsilon_0}\left(-\frac{qy}{(x^2+y^2+z^2)^{3/2}} - \frac{2qy}{(x^2+y^2+(z-d)^2)^{3/2}}\right)$
   
   $\frac{\partial V}{\partial z} = \frac{1}{4\pi\epsilon_0}\left(-\frac{qz}{(x^2+y^2+z^2)^{3/2}} - \frac{2q(z-d)}{(x^2+y^2+(z-d)^2)^{3/2}}\right)$
   
   At (0,0,d/2):
   $\frac{\partial V}{\partial x}|_{(0,0,d/2)} = 0$
   $\frac{\partial V}{\partial y}|_{(0,0,d/2)} = 0$
   $\frac{\partial V}{\partial z}|_{(0,0,d/2)} = \frac{1}{4\pi\epsilon_0}\left(-\frac{q(d/2)}{((d/2)^2)^{3/2}} - \frac{2q((d/2)-d)}{((d/2)^2+(-d/2)^2)^{3/2}}\right)$
   $= \frac{1}{4\pi\epsilon_0}\left(-\frac{q(d/2)}{(d/2)^3} - \frac{2q(-d/2)}{(d/2)^3}\right)$
   $= \frac{1}{4\pi\epsilon_0}\left(-\frac{q}{(d/2)^2} + \frac{2q}{(d/2)^2}\right)$
   $= \frac{1}{4\pi\epsilon_0}\frac{q}{(d/2)^2} = \frac{4q}{4\pi\epsilon_0 d^2}$
   
   Therefore: $\vec{E}(0,0,d/2) = \frac{q}{\pi\epsilon_0 d^2}\hat{z}$
   
   Method 2 - Using direct Coulomb's law:
   
   $\vec{E}_{q} = \frac{1}{4\pi\epsilon_0}\frac{q}{(d/2)^2}(-\hat{z})$
   $\vec{E}_{2q} = \frac{1}{4\pi\epsilon_0}\frac{2q}{(d/2)^2}(\hat{z})$
   
   Total field: $\vec{E} = \vec{E}_{q} + \vec{E}_{2q} = \frac{1}{4\pi\epsilon_0}\frac{q}{(d/2)^2}(-\hat{z} + 2\hat{z}) = \frac{q}{\pi\epsilon_0 d^2}\hat{z}$

3. **Verification:**
   We can verify that $\vec{E} = -\nabla V$ by checking if the z-component of E matches the negative derivative of V with respect to z:
   
   $E_z = \frac{q}{\pi\epsilon_0 d^2}$ and $-\frac{\partial V}{\partial z} = \frac{q}{\pi\epsilon_0 d^2}$ ✓

This example demonstrates the relationship between the electric field and potential, showing two equivalent approaches for calculating the electric field.

### Properties of Conductors in Electrostatic Equilibrium

**Example Question:** A hollow conducting sphere with inner radius a and outer radius b carries a total charge Q. Inside the hollow cavity, at the center, there is a point charge q. Find the electric field and potential everywhere, and the surface charge density on both the inner and outer surfaces of the conductor.

**Step-by-step solution:**

1. **Identify the regions:**
   - Region 1: Inside the cavity (0 < r < a)
   - Region 2: Within the conducting shell (a < r < b)
   - Region 3: Outside the conductor (r > b)

2. **Apply conductor properties:**
   - The electric field inside the conductor (Region 2) is zero
   - The potential is constant throughout the conductor
   - All charge on the conductor resides on the surfaces
   
3. **Find the electric field in each region:**
   
   **Region 1 (0 < r < a):**
   The field is due to the point charge q at the center only. By Gauss's law:
   $E_1(r) = \frac{1}{4\pi\epsilon_0}\frac{q}{r^2}$
   
   **Region 2 (a < r < b):**
   $E_2(r) = 0$ (inside the conductor)
   
   **Region 3 (r > b):**
   The field is due to the total charge (q + Q) at the center. By Gauss's law:
   $E_3(r) = \frac{1}{4\pi\epsilon_0}\frac{q+Q}{r^2}$

4. **Find the potential in each region:**
   
   **Region 3 (r > b):**
   $V_3(r) = \frac{1}{4\pi\epsilon_0}\frac{q+Q}{r} + C_3$
   Setting $V(\infty) = 0$ gives $C_3 = 0$
   So $V_3(r) = \frac{1}{4\pi\epsilon_0}\frac{q+Q}{r}$
   
   **Region 2 (a < r < b):**
   The potential is constant throughout the conductor. Defining $V_2(r) = V_c$ (a constant)
   
   **Region 1 (0 < r < a):**
   $V_1(r) = \frac{1}{4\pi\epsilon_0}\frac{q}{r} + C_1$
   
5. **Apply continuity of potential at boundaries:**
   
   At r = b:
   $V_2(b) = V_3(b)$
   $V_c = \frac{1}{4\pi\epsilon_0}\frac{q+Q}{b}$
   
   At r = a:
   $V_1(a) = V_2(a)$
   $\frac{1}{4\pi\epsilon_0}\frac{q}{a} + C_1 = V_c = \frac{1}{4\pi\epsilon_0}\frac{q+Q}{b}$
   
   Solving for $C_1$:
   $C_1 = \frac{1}{4\pi\epsilon_0}\frac{q+Q}{b} - \frac{1}{4\pi\epsilon_0}\frac{q}{a} = \frac{1}{4\pi\epsilon_0}\left(\frac{q+Q}{b} - \frac{q}{a}\right)$
   
   Therefore:
   $V_1(r) = \frac{1}{4\pi\epsilon_0}\frac{q}{r} + \frac{1}{4\pi\epsilon_0}\left(\frac{q+Q}{b} - \frac{q}{a}\right)$

6. **Find the surface charge densities:**
   
   **Inner surface (r = a):**
   The electric field just inside the cavity at r = a is:
   $E_1(a) = \frac{1}{4\pi\epsilon_0}\frac{q}{a^2}$
   
   The electric field just inside the conductor at r = a is zero.
   
   By Gauss's law, the difference in normal components of the electric field across a surface with charge density σ is:
   $E_1(a) - 0 = \frac{\sigma_a}{\epsilon_0}$
   
   Solving for $\sigma_a$:
   $\sigma_a = \epsilon_0 E_1(a) = \frac{q}{4\pi a^2}$
   
   **Outer surface (r = b):**
   The electric field just outside the conductor at r = b is:
   $E_3(b) = \frac{1}{4\pi\epsilon_0}\frac{q+Q}{b^2}$
   
   The electric field just inside the conductor at r = b is zero.
   
   By Gauss's law:
   $0 - E_3(b) = -\frac{\sigma_b}{\epsilon_0}$
   
   Solving for $\sigma_b$:
   $\sigma_b = \epsilon_0 E_3(b) = \frac{q+Q}{4\pi b^2}$

7. **Verify charge conservation:**
   
   Total charge on inner surface = $4\pi a^2 \cdot \sigma_a = q$
   Total charge on outer surface = $4\pi b^2 \cdot \sigma_b = q+Q$
   
   Therefore, charge on the conductor = $(q+Q) - q = Q$ ✓

This detailed example demonstrates all the key properties of conductors in electrostatic equilibrium, including zero field inside the conductor, constant potential throughout the conductor, and charge residing only on the surfaces.

### Capacitance Calculations

**Example Question:** Two concentric metal spherical shells have radii a and b (a < b). Find the capacitance of this configuration.

**Step-by-step solution:**

1. **Set up the problem:**
   - Inner sphere has radius a
   - Outer sphere has radius b
   - We'll assign charge +Q to the inner sphere and -Q to the outer sphere
   - We need to find the potential difference between the spheres
   
2. **Find the electric field in the region a < r < b:**
   By Gauss's law applied to a spherical surface of radius r (a < r < b):
   $\oint \vec{E} \cdot d\vec{A} = \frac{Q}{\epsilon_0}$
   
   Due to spherical symmetry:
   $E(r) \cdot 4\pi r^2 = \frac{Q}{\epsilon_0}$
   
   Solving for E(r):
   $E(r) = \frac{Q}{4\pi\epsilon_0 r^2}$
   
3. **Calculate the potential difference:**
   $V_a - V_b = -\int_a^b \vec{E} \cdot d\vec{r} = -\int_a^b \frac{Q}{4\pi\epsilon_0 r^2} dr$
   
   $V_a - V_b = -\frac{Q}{4\pi\epsilon_0} \left[-\frac{1}{r}\right]_a^b = \frac{Q}{4\pi\epsilon_0} \left(\frac{1}{a} - \frac{1}{b}\right) = \frac{Q}{4\pi\epsilon_0} \frac{b-a}{ab}$
   
4. **Calculate the capacitance:**
   $C = \frac{Q}{V_a - V_b} = \frac{Q}{\frac{Q}{4\pi\epsilon_0} \frac{b-a}{ab}} = 4\pi\epsilon_0 \frac{ab}{b-a}$
   
5. **Analysis:**
   - As b → ∞, C → 4πε₀a, which is the capacitance of an isolated sphere
   - As b → a, C → ∞, as expected when the separation approaches zero
   - The formula has the correct dimensions: [C] = [ε₀][length] = [Q]/[V]

6. **Alternative method:**
   We can also calculate this by considering two capacitances in series:
   - C₁ = 4πε₀a (isolated inner sphere)
   - C₂ = 4πε₀b (isolated outer sphere, with opposite sign)
   
   For capacitors in series: 1/C = 1/C₁ + 1/C₂
   1/C = 1/(4πε₀a) + 1/(4πε₀b) = (a+b)/(4πε₀ab)
   
   Therefore: C = 4πε₀ab/(a+b)
   
   This differs from our previous result because the isolated sphere formulas assume a reference point at infinity, not the other sphere.

This example demonstrates the systematic approach to calculate capacitance for a geometry with spherical symmetry, relating charge, potential difference, and electric field.

### Conceptual Understanding - Divergence, Curl, and Gradient

**Example Question:** Explain the physical meaning of the divergence, curl, and gradient in electromagnetism, providing specific examples of electromagnetic quantities where each operation is important.

**Detailed answer:**

**Gradient (∇f):**

The gradient of a scalar field f is a vector field that points in the direction of the greatest rate of increase of f, with magnitude equal to the rate of change in that direction.

Physical meaning: The gradient represents the direction and magnitude of the maximum spatial rate of change of a scalar quantity.

In electromagnetism, the gradient appears in:

1. **Electric field and potential**: E = -∇V
   This fundamental relationship shows that the electric field points in the direction of the steepest decrease in potential. For example, near a positive point charge, the potential decreases as you move away from the charge. The gradient of this potential points radially inward, giving an electric field that points radially outward.

2. **Energy in fields**: A charged particle in an electric potential experiences a force F = -q∇V, pushing it toward lower potential energy.

3. **Pressure gradients in plasmas**: ∇p contributes to charged particle motion in plasmas.

Specific electromagnetic example: Around a dipole consisting of charges +q and -q separated by distance d, the potential varies as V ∝ cos(θ)/r² at large distances. The gradient of this gives the familiar dipole electric field, which falls off as 1/r³ and has a characteristic angular pattern different from a single charge.

**Divergence (∇·A):**

The divergence of a vector field A at a point measures the net flow of the vector field away from that point - essentially quantifying whether the point is a source, sink, or neither.

Physical meaning: The divergence represents the extent to which a point acts as a source or sink of the vector field.

In electromagnetism, the divergence appears in:

1. **Gauss's Law**: ∇·E = ρ/ε₀
   This shows that electric charge density (ρ) is the source of the electric field's divergence. Positive charges are sources of electric field lines (positive divergence), while negative charges are sinks (negative divergence).

2. **Charge conservation**: ∇·J + ∂ρ/∂t = 0
   This continuity equation relates current density and charge density.

3. **Absence of magnetic monopoles**: ∇·B = 0
   This states that magnetic fields have no sources or sinks, which manifests as closed magnetic field lines.

Specific electromagnetic example: Consider a point charge q. The electric field is E = (1/4πε₀)(q/r²)r̂. The divergence of this field is zero everywhere except at r = 0, where it's proportional to a delta function. This mathematically represents that the charge is the source of the field, and the field lines truly originate from the charge.

**Curl (∇×A):**

The curl of a vector field A measures the field's rotation or circulation around a point.

Physical meaning: The curl represents the tendency of a vector field to circulate around a point, like a microscopic whirlpool.

In electromagnetism, the curl appears in:

1. **Faraday's Law**: ∇×E = -∂B/∂t
   This shows that a changing magnetic field creates a circulating electric field. This is the principle behind electrical generators and transformers.

2. **Ampère's Law with Maxwell's correction**: ∇×B = μ₀J + μ₀ε₀∂E/∂t
   This shows that currents and changing electric fields create circulating magnetic fields.

3. **Electrostatic fields**: ∇×E = 0 (for static fields)
   This confirms that electrostatic fields are conservative (path-independent).

Specific electromagnetic example: Around a long, straight current-carrying wire, the magnetic field circulates around the wire according to the right-hand rule. If the current is I, the field at distance r is B = (μ₀I/2πr)φ̂. The curl of this field is non-zero only at the wire itself, mathematically representing that the current is the source of the field's circulation.

These mathematical operations are not just abstract concepts but represent fundamental physical properties of electromagnetic fields, connecting the mathematics to observable phenomena.

