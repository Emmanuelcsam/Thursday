
## I. Vector Calculus Fundamentals

### Key Concepts:
- Vector fields and scalar fields
- Gradient, divergence, and curl operations
- Line, surface, and volume integrals
- Fundamental theorems: Gradient Theorem, Divergence Theorem, Stokes' Theorem

### Important Formulas:

**Coordinate Systems:**

1. **Cartesian Coordinates (x, y, z)**:
   - Position vector: $\vec{r} = x\hat{x} + y\hat{y} + z\hat{z}$
   - Volume element: $d\tau = dx\,dy\,dz$

2. **Cylindrical Coordinates (s, φ, z)**:
   - Position vector: $\vec{r} = s\hat{s} + z\hat{z}$
   - Volume element: $d\tau = s\,ds\,d\phi\,dz$
   - Differential length: $d\vec{l} = ds\hat{s} + s\,d\phi\hat{\phi} + dz\hat{z}$

3. **Spherical Coordinates (r, θ, φ)**:
   - Position vector: $\vec{r} = r\hat{r}$
   - Volume element: $d\tau = r^2\sin\theta\,dr\,d\theta\,d\phi$
   - Differential length: $d\vec{l} = dr\hat{r} + r\,d\theta\hat{\theta} + r\sin\theta\,d\phi\hat{\phi}$

**Vector Operations:**

1. **Gradient** (scalar → vector): 
   - $\vec{\nabla}f = \frac{\partial f}{\partial x}\hat{x} + \frac{\partial f}{\partial y}\hat{y} + \frac{\partial f}{\partial z}\hat{z}$
   - Spherical: $\vec{\nabla}f = \frac{\partial f}{\partial r}\hat{r} + \frac{1}{r}\frac{\partial f}{\partial \theta}\hat{\theta} + \frac{1}{r\sin\theta}\frac{\partial f}{\partial \phi}\hat{\phi}$

2. **Divergence** (vector → scalar):
   - $\vec{\nabla}\cdot\vec{A} = \frac{\partial A_x}{\partial x} + \frac{\partial A_y}{\partial y} + \frac{\partial A_z}{\partial z}$
   - Spherical: $\vec{\nabla}\cdot\vec{A} = \frac{1}{r^2}\frac{\partial}{\partial r}(r^2 A_r) + \frac{1}{r\sin\theta}\frac{\partial}{\partial \theta}(\sin\theta A_\theta) + \frac{1}{r\sin\theta}\frac{\partial A_\phi}{\partial \phi}$

3. **Curl** (vector → vector):
   - $\vec{\nabla}\times\vec{A} = \left(\frac{\partial A_z}{\partial y} - \frac{\partial A_y}{\partial z}\right)\hat{x} + \left(\frac{\partial A_x}{\partial z} - \frac{\partial A_z}{\partial x}\right)\hat{y} + \left(\frac{\partial A_y}{\partial x} - \frac{\partial A_x}{\partial y}\right)\hat{z}$

**Fundamental Theorems:**

1. **Gradient Theorem**: $\int_a^b (\vec{\nabla}f) \cdot d\vec{l} = f(b) - f(a)$

2. **Divergence Theorem**: $\int_V (\vec{\nabla}\cdot\vec{A})d\tau = \oint_S \vec{A}\cdot d\vec{a}$

3. **Stokes' Theorem**: $\int_S (\vec{\nabla}\times\vec{A})\cdot d\vec{a} = \oint_P \vec{A}\cdot d\vec{l}$

## II. Electric Field and Coulomb's Law

### Key Concepts:
- Point charges and continuous charge distributions
- Electric field as a vector field
- Superposition principle
- Relationship between electric field and force

### Important Formulas:

1. **Coulomb's Law** (point charge):
   - $\vec{E}(\vec{r}) = \frac{1}{4\pi\epsilon_0}\frac{q}{|\vec{r}-\vec{r}'|^2}\hat{r}$
   - Where $\hat{r}$ is the unit vector pointing from the charge to the observation point

2. **Electric field from a continuous charge distribution**:
   - Volume charge: $\vec{E}(\vec{r}) = \frac{1}{4\pi\epsilon_0}\int_V \frac{\rho(\vec{r}')(\vec{r}-\vec{r}')}{|\vec{r}-\vec{r}'|^3}d\tau'$
   - Surface charge: $\vec{E}(\vec{r}) = \frac{1}{4\pi\epsilon_0}\int_S \frac{\sigma(\vec{r}')(\vec{r}-\vec{r}')}{|\vec{r}-\vec{r}'|^3}da'$
   - Line charge: $\vec{E}(\vec{r}) = \frac{1}{4\pi\epsilon_0}\int_L \frac{\lambda(\vec{r}')(\vec{r}-\vec{r}')}{|\vec{r}-\vec{r}'|^3}dl'$

3. **Force on a charge due to an electric field**:
   - $\vec{F} = q\vec{E}$

### Practice Problem 1:

**Problem**: Find the electric field at point P along the axis of a uniformly charged circular ring of radius R and total charge Q at a distance z from the center of the ring.

**Solution**:

First, I'll establish my coordinate system with the ring centered at the origin in the xy-plane. The point P is located at (0, 0, z).

The ring has a uniform linear charge density of λ = Q/(2πR).

For a small segment of the ring, dq = λdl = (Q/2πR)Rdφ = (Q/2π)dφ.

The distance from this segment to point P is:
$$|\vec{r}-\vec{r}'| = \sqrt{R^2 + z^2}$$

Due to symmetry, the electric field components in the x and y directions cancel out. Only the z-component remains.

For a small segment:
$$dE_z = \frac{1}{4\pi\epsilon_0}\frac{dq}{R^2+z^2}\frac{z}{\sqrt{R^2+z^2}} = \frac{1}{4\pi\epsilon_0}\frac{dq \cdot z}{(R^2+z^2)^{3/2}}$$

Integrating around the entire ring:
$$E_z = \frac{1}{4\pi\epsilon_0}\frac{z}{(R^2+z^2)^{3/2}}\int_0^{2\pi}\frac{Q}{2\pi}d\phi = \frac{1}{4\pi\epsilon_0}\frac{Qz}{(R^2+z^2)^{3/2}}$$

Therefore, the electric field at point P is:
$$\vec{E} = \frac{1}{4\pi\epsilon_0}\frac{Qz}{(R^2+z^2)^{3/2}}\hat{z}$$

Let's check two limiting cases:
1. As z → ∞, E approaches Q/(4πε₀z²), which is the field of a point charge, as expected.
2. At z = 0 (center of the ring), E = 0, which makes sense due to symmetry.

## III. Gauss's Law

### Key Concepts:
- Flux through a closed surface
- Relationship between flux and enclosed charge
- Using symmetry to simplify field calculations
- Differential form of Gauss's Law

### Important Formulas:

1. **Gauss's Law (integral form)**:
   - $\oint_S \vec{E}\cdot d\vec{a} = \frac{Q_{enclosed}}{\epsilon_0}$

2. **Gauss's Law (differential form)**:
   - $\vec{\nabla}\cdot\vec{E} = \frac{\rho}{\epsilon_0}$

3. **Electric field formulas derived using Gauss's Law**:
   - Infinite sheet of charge (σ): $\vec{E} = \frac{\sigma}{2\epsilon_0}\hat{n}$
   - Infinite line of charge (λ): $\vec{E} = \frac{\lambda}{2\pi\epsilon_0 s}\hat{s}$
   - Spherical shell of charge (Q): 
     * $\vec{E} = \frac{1}{4\pi\epsilon_0}\frac{Q}{r^2}\hat{r}$ (outside the shell)
     * $\vec{E} = 0$ (inside the shell)
   - Solid sphere with uniform charge density:
     * $\vec{E} = \frac{1}{4\pi\epsilon_0}\frac{Q}{r^2}\hat{r}$ (outside the sphere)
     * $\vec{E} = \frac{1}{4\pi\epsilon_0}\frac{Qr}{R^3}\hat{r}$ (inside the sphere)

### Practice Problem 2:

**Problem**: A solid non-conducting sphere of radius R has a charge density that varies with distance from the center as ρ(r) = ρ₀(1 - r²/R²) for r ≤ R, where ρ₀ is a constant. Find the electric field both inside and outside the sphere.

**Solution**:

**Step 1**: Find the total charge in the sphere.
$$Q = \int_0^R \rho(r) d\tau = \int_0^R \rho_0 \left(1 - \frac{r^2}{R^2}\right) \cdot 4\pi r^2 dr$$
$$Q = 4\pi\rho_0 \int_0^R \left(r^2 - \frac{r^4}{R^2}\right) dr$$
$$Q = 4\pi\rho_0 \left[\frac{r^3}{3} - \frac{r^5}{5R^2}\right]_0^R$$
$$Q = 4\pi\rho_0 \left(\frac{R^3}{3} - \frac{R^5}{5R^2}\right) = 4\pi\rho_0 \left(\frac{R^3}{3} - \frac{R^3}{5}\right) = 4\pi\rho_0 R^3\left(\frac{5-3}{15}\right)$$
$$Q = \frac{4\pi\rho_0 R^3}{15} \cdot 2 = \frac{8\pi\rho_0 R^3}{15}$$

**Step 2**: Find the electric field outside the sphere (r > R).
Using Gauss's Law, the field is the same as if all the charge were concentrated at the center:
$$E(r) = \frac{1}{4\pi\epsilon_0}\frac{Q}{r^2} = \frac{1}{4\pi\epsilon_0}\frac{8\pi\rho_0 R^3}{15r^2} = \frac{2\rho_0 R^3}{15\epsilon_0 r^2}$$

**Step 3**: Find the electric field inside the sphere (r < R).
For a point at radius r inside the sphere, I need to find the charge enclosed by a Gaussian surface of radius r:
$$Q_{enclosed} = \int_0^r \rho(r') \cdot 4\pi r'^2 dr' = 4\pi\rho_0 \int_0^r \left(r'^2 - \frac{r'^4}{R^2}\right) dr'$$
$$Q_{enclosed} = 4\pi\rho_0 \left[\frac{r'^3}{3} - \frac{r'^5}{5R^2}\right]_0^r = 4\pi\rho_0 \left(\frac{r^3}{3} - \frac{r^5}{5R^2}\right)$$

By Gauss's Law:
$$E(r) \cdot 4\pi r^2 = \frac{Q_{enclosed}}{\epsilon_0}$$
$$E(r) = \frac{Q_{enclosed}}{4\pi\epsilon_0 r^2} = \frac{\rho_0}{\epsilon_0} \left(\frac{r}{3} - \frac{r^3}{5R^2}\right)$$

To summarize:
- For r < R: $E(r) = \frac{\rho_0}{\epsilon_0} \left(\frac{r}{3} - \frac{r^3}{5R^2}\right)$
- For r > R: $E(r) = \frac{2\rho_0 R^3}{15\epsilon_0 r^2}$

## IV. Electric Potential

### Key Concepts:
- Relationship between electric field and potential
- Potential as a scalar field
- Superposition principle for potential
- Calculation of potential from charge distributions
- Equipotential surfaces

### Important Formulas:

1. **Relationship between potential and electric field**:
   - $\vec{E} = -\vec{\nabla}V$
   - $V(\vec{r}) = -\int_{\infty}^{\vec{r}} \vec{E} \cdot d\vec{l}$

2. **Potential due to a point charge**:
   - $V(\vec{r}) = \frac{1}{4\pi\epsilon_0}\frac{q}{|\vec{r}-\vec{r}'|}$

3. **Potential due to a continuous charge distribution**:
   - $V(\vec{r}) = \frac{1}{4\pi\epsilon_0}\int \frac{\rho(\vec{r}')}{|\vec{r}-\vec{r}'|}d\tau'$

4. **Potential energy of a system of charges**:
   - $U = \frac{1}{2}\sum_{i=1}^{n} q_i V(\vec{r}_i)$

5. **Poisson's equation**:
   - $\nabla^2 V = -\frac{\rho}{\epsilon_0}$

6. **Laplace's equation** (in charge-free regions):
   - $\nabla^2 V = 0$

### Practice Problem 3:

**Problem**: Find the electric potential at a point P along the axis of a uniformly charged disk of radius R and surface charge density σ at a distance z from the center of the disk.

**Solution**:

I'll use cylindrical coordinates with the disk centered at the origin in the xy-plane. The point P is located at (0, 0, z).

For a differential ring element of radius s and width ds, the charge is:
$$dq = \sigma \cdot dA = \sigma \cdot 2\pi s \, ds$$

The distance from this ring element to point P is:
$$r' = \sqrt{s^2 + z^2}$$

The potential contribution from this ring is:
$$dV = \frac{1}{4\pi\epsilon_0}\frac{dq}{r'} = \frac{1}{4\pi\epsilon_0}\frac{\sigma \cdot 2\pi s \, ds}{\sqrt{s^2 + z^2}}$$

Integrating over the entire disk:
$$V = \frac{\sigma}{2\epsilon_0}\int_0^R \frac{s \, ds}{\sqrt{s^2 + z^2}}$$

Using the substitution $u = s^2 + z^2$ (which gives $du = 2s \, ds$):
$$V = \frac{\sigma}{4\epsilon_0}\int_{z^2}^{R^2+z^2} \frac{du}{\sqrt{u}} = \frac{\sigma}{2\epsilon_0}[\sqrt{u}]_{z^2}^{R^2+z^2}$$
$$V = \frac{\sigma}{2\epsilon_0}(\sqrt{R^2+z^2} - |z|)$$

Since we're considering a point along the positive z-axis, |z| = z, so:
$$V = \frac{\sigma}{2\epsilon_0}(\sqrt{R^2+z^2} - z)$$

This gives us the potential at any point along the axis of the disk relative to infinity.

Let's check limiting cases:
1. As z → ∞, V approaches 0 (as it should)
2. As R → ∞ (infinite plane), V approaches $\frac{\sigma}{2\epsilon_0} \cdot \frac{R^2}{2z} = \frac{\sigma z}{2\epsilon_0}$ for z << R, which matches the expected result for an infinite plane

## V. Conductors

### Key Concepts:
- Properties of conductors in electrostatic equilibrium
- Charge distribution on conductors
- Electric field inside and outside conductors
- Potential of conductors
- Induced charges

### Important Properties of Conductors:

1. **Electric field inside a conductor in equilibrium is zero**
2. **All excess charge on a conductor resides on its surface**
3. **The electric field just outside a conductor is perpendicular to the surface**
4. **The surface of a conductor is an equipotential**
5. **The electric field just outside a conductor with surface charge density σ is:**
   - $\vec{E} = \frac{\sigma}{\epsilon_0}\hat{n}$

### Practice Problem 4:

**Problem**: A solid conducting sphere of radius a carries a charge Q. It is surrounded by a concentric conducting spherical shell of inner radius b and outer radius c. The shell carries a net charge of -Q. Find the electric field and potential in all regions of space.

**Solution**:

Let me divide the problem into regions:
- Region 1: r < a (inside solid sphere)
- Region 2: a < r < b (between sphere and shell)
- Region 3: b < r < c (inside spherical shell)
- Region 4: r > c (outside both conductors)

**Region 1** (inside solid sphere):
In a conductor, E = 0, so:
$$E_1(r) = 0$$
$$V_1(r) = \text{constant} = V_a$$ (where V_a is the potential at r = a)

**Region 2** (between sphere and shell):
Since there's no charge in this region, Gauss's law gives:
$$E_2(r) \cdot 4\pi r^2 = \frac{Q}{\epsilon_0}$$
$$E_2(r) = \frac{Q}{4\pi\epsilon_0 r^2}$$

The potential is found by integrating:
$$V_2(r) = -\int_{\infty}^{r} E_2(r') \, dr' = -\int_{\infty}^{r} \frac{Q}{4\pi\epsilon_0 r'^2} \, dr' = \frac{Q}{4\pi\epsilon_0} \cdot \frac{1}{r} + C$$

The constant C is determined by the condition that V(r=a) = V_a:
$$V_a = \frac{Q}{4\pi\epsilon_0 a} + C$$
$$C = V_a - \frac{Q}{4\pi\epsilon_0 a}$$

Therefore:
$$V_2(r) = \frac{Q}{4\pi\epsilon_0} \cdot \frac{1}{r} + V_a - \frac{Q}{4\pi\epsilon_0 a} = V_a + \frac{Q}{4\pi\epsilon_0}\left(\frac{1}{r} - \frac{1}{a}\right)$$

**Region 3** (inside spherical shell):
In a conductor, E = 0, so:
$$E_3(r) = 0$$
$$V_3(r) = \text{constant} = V_b$$ (where V_b is the potential at r = b)

The potential must be continuous at r = b, so:
$$V_2(b) = V_b$$
$$V_a + \frac{Q}{4\pi\epsilon_0}\left(\frac{1}{b} - \frac{1}{a}\right) = V_b$$

**Region 4** (outside both conductors):
The net charge enclosed is Q + (-Q) = 0, so Gauss's law gives:
$$E_4(r) \cdot 4\pi r^2 = \frac{0}{\epsilon_0}$$
$$E_4(r) = 0$$

The potential is constant:
$$V_4(r) = V_c$$ (where V_c is the potential at r = c)

The potential at infinity is zero, so V_c = 0.

Now, we need to determine the charge distribution on each surface. 
- At r = a: There's a surface charge density σ_a such that the total charge is Q
- At r = b: There's a surface charge density σ_b
- At r = c: There's a surface charge density σ_c such that σ_b + σ_c = -Q

By Gauss's law and the continuity of the electric field:
- At r = a: $\sigma_a = \frac{\epsilon_0 Q}{4\pi a^2}$
- At r = b: $\sigma_b = -\frac{\epsilon_0 Q}{4\pi b^2}$
- At r = c: $\sigma_c = 0$ (since E = 0 for r > c)

To summarize:
- Region 1 (r < a): E = 0, V = V_a
- Region 2 (a < r < b): E = Q/(4πε₀r²), V = V_a + (Q/4πε₀)(1/r - 1/a)
- Region 3 (b < r < c): E = 0, V = V_b
- Region 4 (r > c): E = 0, V = 0

Setting V_c = 0 (potential at infinity), we can determine V_b and V_a:
V_b = 0 (since V is constant in region 3 and V_c = 0)
V_a = -Q/(4πε₀)(1/b - 1/a) (from the condition V_2(b) = V_b)

## VI. Capacitance and Energy

### Key Concepts:
- Definition of capacitance
- Calculating capacitance for various geometries
- Energy stored in capacitors
- Energy density in electric fields

### Important Formulas:

1. **Capacitance definition**:
   - $C = \frac{Q}{V}$

2. **Common capacitance formulas**:
   - Parallel plate: $C = \frac{\epsilon_0 A}{d}$
   - Cylindrical: $C = \frac{2\pi\epsilon_0 L}{\ln(b/a)}$
   - Spherical: $C = 4\pi\epsilon_0 \frac{ab}{b-a}$

3. **Energy stored in a capacitor**:
   - $U = \frac{1}{2}CV^2 = \frac{1}{2}\frac{Q^2}{C} = \frac{1}{2}QV$

4. **Energy density in an electric field**:
   - $u = \frac{1}{2}\epsilon_0 E^2$

5. **Total energy in an electric field**:
   - $U = \frac{\epsilon_0}{2}\int_V E^2 d\tau$

### Practice Problem 5:

**Problem**: Two concentric spherical conducting shells have radii a and b (with a < b). The inner shell carries charge Q and the outer shell carries charge -Q. Calculate:
a) The electric field in all regions
b) The potential difference between the shells
c) The capacitance of this system
d) The energy stored in the capacitor

**Solution**:

**a) Electric field in all regions**

Let's divide space into three regions:
- Region 1: r < a (inside inner shell)
- Region 2: a < r < b (between shells)
- Region 3: r > b (outside outer shell)

In regions 1 and 3, the electric field is zero (inside conductors and outside a neutral system).

In region 2, using Gauss's law:
$$E(r) \cdot 4\pi r^2 = \frac{Q}{\epsilon_0}$$
$$E(r) = \frac{Q}{4\pi\epsilon_0 r^2}$$

**b) Potential difference between the shells**

The potential difference is:
$$\Delta V = V(a) - V(b) = -\int_a^b E(r) \, dr = -\int_a^b \frac{Q}{4\pi\epsilon_0 r^2} \, dr$$
$$\Delta V = \frac{Q}{4\pi\epsilon_0} \int_a^b \frac{1}{r^2} \, dr = \frac{Q}{4\pi\epsilon_0} \left[-\frac{1}{r}\right]_a^b$$
$$\Delta V = \frac{Q}{4\pi\epsilon_0} \left(-\frac{1}{b} + \frac{1}{a}\right) = \frac{Q}{4\pi\epsilon_0} \frac{b-a}{ab}$$

**c) Capacitance of the system**

Using the definition of capacitance:
$$C = \frac{Q}{\Delta V} = \frac{Q}{\frac{Q}{4\pi\epsilon_0} \frac{b-a}{ab}} = 4\pi\epsilon_0 \frac{ab}{b-a}$$

**d) Energy stored in the capacitor**

The energy can be calculated as:
$$U = \frac{1}{2}Q\Delta V = \frac{1}{2}Q \cdot \frac{Q}{4\pi\epsilon_0} \frac{b-a}{ab} = \frac{Q^2}{8\pi\epsilon_0} \frac{b-a}{ab}$$

Alternatively, we can use:
$$U = \frac{1}{2}\frac{Q^2}{C} = \frac{1}{2} \cdot \frac{Q^2}{4\pi\epsilon_0 \frac{ab}{b-a}} = \frac{Q^2}{8\pi\epsilon_0} \frac{b-a}{ab}$$

## VII. Method of Images

### Key Concepts:
- Solving for the electric field using fictional "image" charges
- Uniqueness theorem and Laplace's equation
- Boundary conditions
- Application to problems with conducting surfaces

### Method of Images Process:

1. Replace a conducting surface with an "image" charge positioned to create the same boundary conditions
2. Verify that the potential satisfies Laplace's equation (∇²V = 0)
3. Verify that the boundary conditions are met
4. Calculate the desired fields/potentials using the original and image charges

### Practice Problem 6:

**Problem**: A point charge q is placed at a distance d above an infinite grounded conducting plane. Find:
a) The electric potential everywhere above the plane
b) The electric field above the plane
c) The surface charge density induced on the conducting plane
d) The force on the point charge

**Solution**:

**a) Electric potential everywhere above the plane**

The image method suggests placing a charge -q at a distance d below the plane. The potential at any point (x, y, z) above the plane is:

$$V(x,y,z) = \frac{1}{4\pi\epsilon_0}\left[\frac{q}{\sqrt{x^2 + y^2 + (z-d)^2}} - \frac{q}{\sqrt{x^2 + y^2 + (z+d)^2}}\right]$$

This potential satisfies:
1. Laplace's equation (∇²V = 0) in the region above the plane
2. The boundary condition V = 0 at z = 0 (the conducting plane)
3. The correct behavior near the charge q

**b) Electric field above the plane**

The electric field is the negative gradient of the potential:

$$\vec{E}(x,y,z) = -\vec{\nabla}V = \frac{1}{4\pi\epsilon_0}\left[\frac{q(\vec{r}-\vec{r}_q)}{|\vec{r}-\vec{r}_q|^3} - \frac{q(\vec{r}-\vec{r}_{-q})}{|\vec{r}-\vec{r}_{-q}|^3}\right]$$

Where:
- $\vec{r}_q = (0,0,d)$ is the position of the charge q
- $\vec{r}_{-q} = (0,0,-d)$ is the position of the image charge -q

This gives components:

$$E_x = \frac{q}{4\pi\epsilon_0}\left[\frac{x}{(x^2 + y^2 + (z-d)^2)^{3/2}} - \frac{x}{(x^2 + y^2 + (z+d)^2)^{3/2}}\right]$$

$$E_y = \frac{q}{4\pi\epsilon_0}\left[\frac{y}{(x^2 + y^2 + (z-d)^2)^{3/2}} - \frac{y}{(x^2 + y^2 + (z+d)^2)^{3/2}}\right]$$

$$E_z = \frac{q}{4\pi\epsilon_0}\left[\frac{z-d}{(x^2 + y^2 + (z-d)^2)^{3/2}} - \frac{z+d}{(x^2 + y^2 + (z+d)^2)^{3/2}}\right]$$

**c) Surface charge density induced on the conducting plane**

The surface charge density is related to the electric field just above the surface:

$$\sigma = \epsilon_0 E_z|_{z=0}$$

At z = 0:

$$E_z|_{z=0} = \frac{q}{4\pi\epsilon_0}\left[\frac{-d}{(x^2 + y^2 + d^2)^{3/2}} - \frac{d}{(x^2 + y^2 + d^2)^{3/2}}\right] = -\frac{qd}{2\pi\epsilon_0(x^2 + y^2 + d^2)^{3/2}}$$

Therefore:

$$\sigma(x,y) = -\frac{qd}{2\pi(x^2 + y^2 + d^2)^{3/2}}$$

The total induced charge on the plane is:

$$Q_{induced} = \int_{-\infty}^{\infty}\int_{-\infty}^{\infty} \sigma(x,y) \, dx \, dy$$

Converting to polar coordinates:

$$Q_{induced} = \int_{0}^{2\pi}\int_{0}^{\infty} -\frac{qd}{2\pi(r^2 + d^2)^{3/2}} \, r \, dr \, d\theta = -qd \int_{0}^{\infty} \frac{r \, dr}{(r^2 + d^2)^{3/2}}$$

Let me continue with the rest of your comprehensive E&M study guide.

$$Q_{induced} = -qd \left[-\frac{1}{\sqrt{r^2 + d^2}}\right]_{0}^{\infty} = -qd \left(0 - \frac{1}{d}\right) = -q$$

This confirms an important result: the total induced charge on the grounded plane is equal and opposite to the original point charge.

**d) Force on the point charge**

The force on the point charge q is due to the electric field created by the induced charges on the plane, which is equivalent to the field created by the image charge -q:

$$\vec{F} = q\vec{E}_{image} = \frac{1}{4\pi\epsilon_0}\frac{q \cdot (-q)}{(2d)^2}\hat{z} = -\frac{q^2}{16\pi\epsilon_0d^2}\hat{z}$$

The negative sign indicates that the force is attractive, pulling the charge toward the conducting plane.

## VIII. Poisson and Laplace Equations

### Key Concepts:
- Poisson's equation for regions with charge: $\nabla^2 V = -\frac{\rho}{\epsilon_0}$
- Laplace's equation for charge-free regions: $\nabla^2 V = 0$
- Uniqueness theorem for boundary-value problems
- Solutions using separation of variables

### Important Results:

1. **Uniqueness Theorem**: If a potential function satisfies Laplace's equation within a volume and matches the specified boundary conditions on the surface of that volume, then it is the unique solution to the electrostatic problem.

2. **General approach to boundary-value problems**:
   - Identify the appropriate coordinate system based on the geometry
   - Express the potential using separation of variables
   - Apply boundary conditions to determine the solution

### Separation of Variables Approach:

In Cartesian coordinates, a separable solution has the form:
$$V(x,y,z) = X(x)Y(y)Z(z)$$

Substituting into Laplace's equation and dividing by V:
$$\frac{1}{X}\frac{d^2X}{dx^2} + \frac{1}{Y}\frac{d^2Y}{dy^2} + \frac{1}{Z}\frac{d^2Z}{dz^2} = 0$$

Each term must equal a constant, and the sum of these constants must be zero:
$$\frac{1}{X}\frac{d^2X}{dx^2} = -\alpha^2$$
$$\frac{1}{Y}\frac{d^2Y}{dy^2} = -\beta^2$$
$$\frac{1}{Z}\frac{d^2Z}{dz^2} = \alpha^2 + \beta^2 = \gamma^2$$

General solutions to these equations:
- If α² > 0: $X(x) = A\sin(\alpha x) + B\cos(\alpha x)$
- If α² = 0: $X(x) = Ax + B$
- If α² < 0: $X(x) = Ae^{\alpha x} + Be^{-\alpha x}$

Similar expressions apply for Y(y) and Z(z).

# Physics 401 - Practice Midterm Exam

**Duration**: 80 minutes
**Total Points**: 100
**Allowed Materials**: Equation sheet and vector calculus reference sheet (provided)

## Problem 1 (25 points)
A thin disk of radius R has a non-uniform surface charge density that varies with distance s from the center according to the formula:
$$\sigma(s) = \sigma_0 \cdot (1 - \frac{s^2}{R^2})$$
where $\sigma_0$ is a positive constant.

a) (10 points) Find the total charge on the disk.

b) (15 points) Find the electric field along the z-axis (perpendicular to the plane of the disk and passing through its center). Express your answer in terms of $\sigma_0$, R, z, and fundamental constants.

## Problem 2 (25 points)
An infinitely long cylindrical shell with inner radius a and outer radius b carries a uniform volume charge density $\rho$.

a) (15 points) Find the electric field in all regions: (i) $r < a$, (ii) $a < r < b$, and (iii) $r > b$.

b) (10 points) Sketch the magnitude of the electric field $|E|$ as a function of the distance r from the axis.

## Problem 3 (25 points)
A point charge q is placed at a distance d from the center of a grounded conducting sphere of radius R, where d > R.

a) (10 points) Find the potential everywhere outside the sphere.

b) (10 points) Calculate the surface charge density induced on the sphere.

c) (5 points) What is the total induced charge on the sphere?

## Problem 4 (25 points)
Two parallel conducting plates are separated by a distance d. The upper plate has a hole of radius a cut in it. A point charge q is placed at a distance h above the center of the hole (h << a).

a) (15 points) Use the method of images to find the approximate electric field at the position of the charge q.

b) (10 points) Calculate the force on the charge q.

---

# Solutions

## Problem 1 Solution

### a) Find the total charge on the disk.

The total charge is the integral of the charge density over the area of the disk:

$$Q = \int \sigma(s) dA = \int_0^{2\pi} \int_0^R \sigma_0 \cdot (1 - \frac{s^2}{R^2}) \cdot s \, ds \, d\phi$$

$$Q = 2\pi \sigma_0 \int_0^R (s - \frac{s^3}{R^2}) \, ds$$

$$Q = 2\pi \sigma_0 [\frac{s^2}{2} - \frac{s^4}{4R^2}]_0^R$$

$$Q = 2\pi \sigma_0 (\frac{R^2}{2} - \frac{R^4}{4R^2}) = 2\pi \sigma_0 (\frac{R^2}{2} - \frac{R^2}{4}) = 2\pi \sigma_0 \cdot \frac{R^2}{4} = \frac{\pi \sigma_0 R^2}{2}$$

### b) Find the electric field along the z-axis.

I'll use the expression for the electric field from a thin disk element and integrate over the entire disk:

A differential ring of radius s and width ds has area $dA = 2\pi s \, ds$ and charge $dq = \sigma(s) \cdot 2\pi s \, ds$.

Due to symmetry, the electric field at a point (0,0,z) on the z-axis only has a z-component. For a ring element:

$$dE_z = \frac{1}{4\pi\epsilon_0} \frac{dq \cdot z}{(s^2 + z^2)^{3/2}}$$

$$dE_z = \frac{1}{4\pi\epsilon_0} \frac{\sigma_0 \cdot (1 - \frac{s^2}{R^2}) \cdot 2\pi s \, ds \cdot z}{(s^2 + z^2)^{3/2}}$$

$$dE_z = \frac{\sigma_0 z}{2\epsilon_0} \frac{(1 - \frac{s^2}{R^2}) \cdot s \, ds}{(s^2 + z^2)^{3/2}}$$

Integrating over the entire disk:

$$E_z = \frac{\sigma_0 z}{2\epsilon_0} \int_0^R \frac{(1 - \frac{s^2}{R^2}) \cdot s \, ds}{(s^2 + z^2)^{3/2}}$$

$$E_z = \frac{\sigma_0 z}{2\epsilon_0} \int_0^R \frac{s \, ds}{(s^2 + z^2)^{3/2}} - \frac{\sigma_0 z}{2\epsilon_0 R^2} \int_0^R \frac{s^3 \, ds}{(s^2 + z^2)^{3/2}}$$

For the first integral, using substitution $u = s^2 + z^2$:
$$\int_0^R \frac{s \, ds}{(s^2 + z^2)^{3/2}} = \frac{1}{2} \int_{z^2}^{R^2+z^2} \frac{du}{u^{3/2}} = \frac{1}{2} \left[-\frac{2}{u^{1/2}}\right]_{z^2}^{R^2+z^2} = \frac{1}{2} \left(-\frac{2}{\sqrt{R^2+z^2}} + \frac{2}{|z|}\right) = \frac{1}{|z|} - \frac{1}{\sqrt{R^2+z^2}}$$

For the second integral, using integration by parts:
$$\int_0^R \frac{s^3 \, ds}{(s^2 + z^2)^{3/2}} = \frac{R^2}{\sqrt{R^2+z^2}} - z^2 \int_0^R \frac{s \, ds}{(s^2 + z^2)^{3/2}} = \frac{R^2}{\sqrt{R^2+z^2}} - z^2 (\frac{1}{|z|} - \frac{1}{\sqrt{R^2+z^2}})$$

Assuming z > 0 to simplify:
$$E_z = \frac{\sigma_0}{2\epsilon_0} \left[1 - \frac{z}{\sqrt{R^2+z^2}} - \frac{z}{R^2} \frac{R^2}{\sqrt{R^2+z^2}} + \frac{z^3}{R^2} \left(\frac{1}{z} - \frac{1}{\sqrt{R^2+z^2}}\right)\right]$$

$$E_z = \frac{\sigma_0}{2\epsilon_0} \left[1 - \frac{z}{\sqrt{R^2+z^2}} - \frac{z}{\sqrt{R^2+z^2}} + \frac{z^2}{R^2} - \frac{z^3}{R^2} \frac{1}{\sqrt{R^2+z^2}}\right]$$

After simplifying:
$$E_z = \frac{\sigma_0}{2\epsilon_0} \left[1 - \frac{2z}{\sqrt{R^2+z^2}} + \frac{z^2}{R^2}\left(1 - \frac{z}{\sqrt{R^2+z^2}}\right)\right]$$

## Problem 2 Solution

### a) Find the electric field in all regions.

Let's use Gauss's law to find the electric field in each region. The charge enclosed by a Gaussian cylinder of radius r and length L is:

(i) For r < a:
No charge is enclosed, so by Gauss's law:
$$\oint \vec{E} \cdot d\vec{a} = \frac{Q_{enclosed}}{\epsilon_0} = 0$$
$$E(r) \cdot 2\pi r L = 0$$
$$E(r) = 0$$

(ii) For a < r < b:
The charge enclosed is:
$$Q_{enclosed} = \rho \cdot \pi(r^2 - a^2) \cdot L$$

By Gauss's law:
$$E(r) \cdot 2\pi r L = \frac{\rho \cdot \pi(r^2 - a^2) \cdot L}{\epsilon_0}$$
$$E(r) = \frac{\rho}{2\epsilon_0} \frac{r^2 - a^2}{r}$$

(iii) For r > b:
The total charge enclosed is:
$$Q_{enclosed} = \rho \cdot \pi(b^2 - a^2) \cdot L$$

By Gauss's law:
$$E(r) \cdot 2\pi r L = \frac{\rho \cdot \pi(b^2 - a^2) \cdot L}{\epsilon_0}$$
$$E(r) = \frac{\rho}{2\epsilon_0} \frac{b^2 - a^2}{r}$$

### b) Sketch the magnitude of the electric field.

The electric field magnitude as a function of r:
- For r < a: E(r) = 0
- For a < r < b: E(r) = $\frac{\rho}{2\epsilon_0} \frac{r^2 - a^2}{r}$
- For r > b: E(r) = $\frac{\rho}{2\epsilon_0} \frac{b^2 - a^2}{r}$

I would sketch this showing:
- Zero field inside the inner radius
- Field increasing from r = a, reaching maximum inside the shell
- Field decreasing as 1/r outside the shell

The field is continuous at r = b, but has a discontinuity at r = a where it jumps from 0 to some non-zero value.

## Problem 3 Solution

### a) Find the potential everywhere outside the sphere.

I'll use the method of images. For a point charge q at distance d from the center of a grounded conducting sphere of radius R, the image charge q' is placed at distance d' from the center, where:

$$d' = \frac{R^2}{d}$$

The magnitude of the image charge is:

$$q' = -q \cdot \frac{R}{d}$$

The potential at any point (r,θ) outside the sphere is:

$$V(r,θ) = \frac{1}{4\pi\epsilon_0} \left[\frac{q}{\sqrt{r^2 + d^2 - 2rd\cos\theta}} + \frac{q'}{\sqrt{r^2 + d'^2 - 2rd'\cos\theta}}\right]$$

$$V(r,θ) = \frac{1}{4\pi\epsilon_0} \left[\frac{q}{\sqrt{r^2 + d^2 - 2rd\cos\theta}} - \frac{qR/d}{\sqrt{r^2 + R^4/d^2 - 2rR^2\cos\theta/d}}\right]$$

### b) Calculate the surface charge density induced on the sphere.

The surface charge density at any point on the sphere is related to the normal component of the electric field just outside the sphere:

$$\sigma(θ) = \epsilon_0 E_r(R,θ)$$

The radial component of the electric field is:

$$E_r(r,θ) = -\frac{\partial V}{\partial r}$$

Evaluating at r = R and after some calculation:

$$\sigma(θ) = -\frac{qR}{4\pi} \frac{d^2-R^2}{(d^2+R^2-2dR\cos\theta)^{3/2}}$$

### c) Find the total induced charge on the sphere.

The total induced charge is:

$$Q_{induced} = \int \sigma(θ) dA = \int_0^{2\pi} \int_0^{\pi} \sigma(θ) R^2 \sin\theta \, d\theta \, d\phi$$

$$Q_{induced} = -\frac{qR^3}{2} \int_0^{\pi} \frac{d^2-R^2}{(d^2+R^2-2dR\cos\theta)^{3/2}} \sin\theta \, d\theta$$

This integral can be evaluated using substitution, and the result is:

$$Q_{induced} = -q \cdot \frac{R}{d}$$

Since d > R, we have |Q_induced| < |q|.

## Problem 4 Solution

### a) Find the approximate electric field at the position of the charge.

When h << a, we can approximate the hole as being in an infinite conducting plane. Using the method of images, the image charge -q is placed at a distance h below the hole.

The electric field at the position of the charge q is due to the image charge -q:

$$\vec{E} = \frac{1}{4\pi\epsilon_0} \frac{q}{(2h)^2} (-\hat{z})$$

$$\vec{E} = -\frac{q}{16\pi\epsilon_0 h^2} \hat{z}$$

### b) Calculate the force on the charge q.

The force on the charge q is:

$$\vec{F} = q\vec{E} = q \cdot (-\frac{q}{16\pi\epsilon_0 h^2} \hat{z}) = -\frac{q^2}{16\pi\epsilon_0 h^2} \hat{z}$$

The negative sign indicates that the force is attractive, pulling the charge toward the conducting plane.

