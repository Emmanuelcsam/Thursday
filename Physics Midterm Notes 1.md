
https://youtube.com/playlist?list=PLKxxVVdhQNB5VcSXXqWqbjC73lBNt0APG&si=M6BK0ugiikZ39bwj
https://www.youtube.com/watch?v=jukf82J6raI&list=PLn3nlFjQ6qlFKlmoO2fS956MTHxp6yNXl
https://www.youtube.com/watch?v=2JBALhAPe9Q&list=PLW_rrS5FXW9CR34QmP7RwreteyxtjBPuW
# Comprehensive Explanation of Electrostatics Problems from Physics 401

## Fundamental Concepts in Electrostatics

Before diving into the specific problems, I'll establish the core principles that govern electrostatic phenomena. Electrostatics is the branch of physics that studies electric charges at rest and the electric fields and potentials they create.

### Coulomb's Law: The Foundation of Electrostatics

The fundamental law governing the interaction between electric charges is Coulomb's law. For two point charges q₁ and q₂ separated by a distance r, the electrostatic force they exert on each other is:

F = (1/4πε₀) × (q₁q₂/r²) × r̂

Where:
- F is the force vector (measured in newtons, N)
- ε₀ = 8.85 × 10⁻¹² C²/(N·m²) is the permittivity of free space
- r is the distance between charges (in meters)
- r̂ is the unit vector pointing from one charge to the other
- The factor 1/4πε₀ is approximately 9 × 10⁹ N·m²/C²

If the charges have the same sign (both positive or both negative), the force is repulsive (pushes them apart). If they have opposite signs, the force is attractive (pulls them together).

### The Electric Field Concept

Rather than thinking about direct interactions between charges, we can introduce the concept of an electric field. A charge q₁ creates an electric field in the space around it. When a second charge q₂ is placed in this field, it experiences a force due to the field.

For a point charge q, the electric field at a distance r is:

E = (1/4πε₀) × (q/r²) × r̂

The electric field is a vector quantity measured in newtons per coulomb (N/C) or, equivalently, volts per meter (V/m).

For multiple charges, the total electric field at any point is the vector sum of the fields due to individual charges (the superposition principle):

E_total = E₁ + E₂ + E₃ + ...

### Continuous Charge Distributions

When dealing with continuous distributions of charge rather than discrete point charges, we use charge densities:
- Linear charge density (λ): charge per unit length (C/m)
- Surface charge density (σ): charge per unit area (C/m²)
- Volume charge density (ρ): charge per unit volume (C/m³)

For a continuous charge distribution, the electric field is given by:

E(r) = (1/4πε₀) ∫ [ρ(r')/|r-r'|³] (r-r') dτ'

Where:
- r is the position where we're calculating the field
- r' is the position of each element of charge
- ρ(r') is the charge density at r'
- dτ' is an infinitesimal volume element

This integral must be evaluated over the entire charge distribution.

### Gauss's Law: A Powerful Tool

Gauss's law provides an alternative approach to finding electric fields when symmetry permits. It states:

∮ E·dA = Q_enclosed/ε₀

Where:
- The integral is over a closed surface (the Gaussian surface)
- E is the electric field
- dA is an infinitesimal element of the surface (including direction)
- Q_enclosed is the total charge enclosed by the surface

This law is particularly useful for charge distributions with spherical, cylindrical, or planar symmetry.

### Electric Potential

The electric potential (V) is a scalar quantity that represents the potential energy per unit charge at a point in an electric field. It's related to the electric field by:

E = -∇V

Where ∇ (the gradient operator) is a vector operator that gives the direction and magnitude of the maximum rate of change of the potential.

For a point charge q, the potential at a distance r is:

V = (1/4πε₀) × (q/r)

For a continuous charge distribution:

V(r) = (1/4πε₀) ∫ [ρ(r')/|r-r'|] dτ'

The potential difference (voltage) between two points A and B is:

V_B - V_A = -∫_A^B E·dl

Where the integral is taken along any path from A to B.

### Conductors in Electrostatic Equilibrium

Conductors contain free electrons that can move in response to electric fields. In electrostatic equilibrium (when all charges are at rest), conductors exhibit several important properties:

1. The electric field inside a conductor is zero.
2. All excess charge resides on the surface of the conductor.
3. The electric field just outside a conductor is perpendicular to the surface.
4. The electric field magnitude just outside a conductor is σ/ε₀, where σ is the surface charge density.
5. The entire conductor is an equipotential (the potential is constant throughout).

## Vector Calculus for Electrostatics

Electrostatics relies heavily on vector calculus. Here's a review of the key operations:

### Gradient (∇f)

The gradient of a scalar function f produces a vector field pointing in the direction of greatest increase of f, with magnitude equal to the rate of change in that direction.

In Cartesian coordinates:
∇f = (∂f/∂x)x̂ + (∂f/∂y)ŷ + (∂f/∂z)ẑ

In spherical coordinates:
∇f = (∂f/∂r)r̂ + (1/r)(∂f/∂θ)θ̂ + (1/(r·sinθ))(∂f/∂φ)φ̂

In cylindrical coordinates:
∇f = (∂f/∂s)ŝ + (1/s)(∂f/∂φ)φ̂ + (∂f/∂z)ẑ

### Divergence (∇·A)

The divergence of a vector field A measures how much the field "spreads out" from a point (the source or sink behavior).

In Cartesian coordinates:
∇·A = ∂A_x/∂x + ∂A_y/∂y + ∂A_z/∂z

In spherical coordinates:
∇·A = (1/r²)(∂/∂r)(r²A_r) + (1/(r·sinθ))(∂/∂θ)(sinθ·A_θ) + (1/(r·sinθ))(∂/∂φ)(A_φ)

In cylindrical coordinates:
∇·A = (1/s)(∂/∂s)(s·A_s) + (1/s)(∂A_φ/∂φ) + ∂A_z/∂z

### Curl (∇×A)

The curl of a vector field A measures the field's rotational behavior.

In Cartesian coordinates:
∇×A = [(∂A_z/∂y - ∂A_y/∂z)x̂ + (∂A_x/∂z - ∂A_z/∂x)ŷ + (∂A_y/∂x - ∂A_x/∂y)ẑ]

### Laplacian (∇²f)

The Laplacian of a scalar function f is the divergence of the gradient:
∇²f = ∇·(∇f)

In Cartesian coordinates:
∇²f = ∂²f/∂x² + ∂²f/∂y² + ∂²f/∂z²

The Laplacian appears in Poisson's equation: ∇²V = -ρ/ε₀
And in charge-free regions (where ρ = 0), we get Laplace's equation: ∇²V = 0

### Vector Calculus Theorems

Three major theorems are crucial for electrostatics:

**1. Gradient Theorem:**
∫_a^b (∇f)·dl = f(b) - f(a)

This connects line integrals to the endpoints of the path.

**2. Divergence Theorem (Gauss's Theorem):**
∫_V (∇·A)dτ = ∮_S A·dA

This relates the volume integral of the divergence to the flux through the enclosing surface.

**3. Stokes' Theorem:**
∫_S (∇×A)·dA = ∮_C A·dl

This connects the surface integral of curl to the circulation around the boundary.

Now, let's apply these concepts to solve the specific problems.

## Problem 1: Infinite Line Charge Parallel to a Grounded Conducting Plate

### Problem Statement
An infinite line charge with a constant, positive charge density λ (in C/m) is parallel to an infinite, grounded conducting plate with a distance a between them.

(a) What is the electric field between the line charge and the plane along the y-axis at a height y above the plane?
(b) What is the force per unit length in N/m between the line charge and the plane?

### Solution Using the Method of Images

The method of images is a powerful technique for solving problems involving conductors by replacing the conductor with imaginary "image charges" that create the same boundary conditions.

#### Step 1: Understand the Physical Setup
- The conducting plate is at y = 0 (the xy-plane)
- The line charge is at position (0, a, 0), running parallel to the z-axis
- We want to find the field at points (0, y, 0) where 0 < y < a

#### Step 2: Apply the Method of Images
For a grounded conducting plate, we can replace the plate with an image line charge of equal magnitude but opposite sign, positioned at (0, -a, 0).

The image charge has linear density -λ (negative of the original).

#### Step 3: Calculate the Electric Field from the Real Line Charge
For an infinite line charge with linear density λ, the electric field at a distance r is:

E = λ/(2πε₀r)

This field points radially outward from the line.

At a point (0, y, 0) where 0 < y < a, the distance to the real line charge is:
r₁ = a - y

The electric field due to the real line charge is:
E₁ = λ/(2πε₀(a-y))

The direction of this field is radially outward from the line charge. Since we're considering points directly below the line charge on the y-axis, the field points downward (in the negative y-direction):

E₁ = -λ/(2πε₀(a-y))ŷ

#### Step 4: Calculate the Electric Field from the Image Line Charge
Similarly, at point (0, y, 0), the distance to the image line charge is:
r₂ = y + a

The electric field due to the image charge is:
E₂ = -λ/(2πε₀(y+a))

Since the image charge is negative, its field points inward toward the line (radially inward). For points on the y-axis above the image charge, this is also in the negative y-direction:

E₂ = -λ/(2πε₀(y+a))ŷ

#### Step 5: Apply the Superposition Principle to Find the Total Field
The total electric field is the vector sum of the fields from both charges:

E = E₁ + E₂ = -λ/(2πε₀(a-y))ŷ - λ/(2πε₀(y+a))ŷ
  = -λ/(2πε₀)[(1/(a-y)) + (1/(y+a))]ŷ

Let's simplify this expression:
E = -λ/(2πε₀)[(y+a) + (a-y)]/[(a-y)(y+a)]ŷ
  = -λ/(2πε₀)[2a]/[(a-y)(y+a)]ŷ
  = -λa/(πε₀(a²-y²))ŷ

Therefore, the electric field between the line charge and the plane along the y-axis at height y is:
E = -λa/(πε₀(a²-y²))ŷ

#### Step 6: Calculate the Force per Unit Length
The force on the real line charge is due to the electric field created by the image charge alone (evaluated at the position of the real charge, y = a):

F/L = λE₂(y=a) = λ × [-λ/(2πε₀(a+a))] = -λ²/(4πε₀a)ŷ

The negative sign indicates the force is attractive (toward the plate), which makes physical sense since the line charge is attracted to its opposite-signed image.

### Physical Interpretation

The electric field increases as y approaches either the line charge (y → a) or the conducting plate (y → 0) because:
1. Near the line charge: the 1/(a-y) term dominates
2. Near the conducting plate: the 1/(y+a) term contributes significantly

The force between the line charge and the plate is attractive and follows an inverse relationship with distance (1/a), similar to the force between point charges but with different dependence on distance due to the linear nature of the charge distribution.

## Problem 2: Cylindrical Capacitor

### Problem Statement
A cylindrical capacitor has an inner radius R₁, outer radius R₂, and length L, where L >> R₂. The inner surface has a charge +Q on it and the outer surface has a charge -Q on it.

(a) What is the electric field in between the surfaces at a distance s from the cylinder axis?
(b) What is the potential difference between the plates?
(c) What is the energy stored in the capacitor?

### Detailed Solution

#### Part (a): Finding the Electric Field

##### Step 1: Identify the Symmetry and Use Gauss's Law
The problem has cylindrical symmetry, so we'll use Gauss's law with a cylindrical Gaussian surface.

Gauss's law states:
∮ E·dA = Q_enclosed/ε₀

##### Step 2: Set Up the Gaussian Surface
We'll use a cylindrical Gaussian surface of radius s (where R₁ < s < R₂) and length L' (where L' < L to avoid edge effects, which we can ignore since L >> R₂).

Due to the cylindrical symmetry:
- The electric field is radial (E = E(s)ŝ)
- The field strength is uniform around any circle of radius s
- The field has no z-component or angular component

##### Step 3: Apply Gauss's Law
For our cylindrical Gaussian surface:
- The electric field is perpendicular to the curved surface and has magnitude E(s)
- The flux through the end caps is zero (E is parallel to these surfaces)
- The enclosed charge is +Q(L'/L) (proportional to the length of our Gaussian surface)

∮ E·dA = E(s) × (2πsL') = Q(L'/L)/ε₀

##### Step 4: Solve for the Electric Field
Rearranging:
E(s) = [Q(L'/L)]/[2πsL'ε₀] = Q/[2πsLε₀]

The direction is radially outward from the axis, so:
E = [Q/(2πsLε₀)]ŝ

This is the electric field at a distance s from the axis, where R₁ < s < R₂.

#### Part (b): Finding the Potential Difference

##### Step 1: Relate Potential to Electric Field
The potential difference is the negative line integral of the electric field:
V(R₁) - V(R₂) = -∫_R₁^R₂ E·dl

Since E points in the radial direction (ŝ) and dl = dsŝ when moving radially:
V(R₁) - V(R₂) = -∫_R₁^R₂ [Q/(2πsLε₀)]ds

##### Step 2: Evaluate the Integral
V(R₁) - V(R₂) = -[Q/(2πLε₀)]∫_R₁^R₂ (1/s)ds
                = -[Q/(2πLε₀)][ln(s)]_R₁^R₂
                = -[Q/(2πLε₀)][ln(R₂) - ln(R₁)]
                = -[Q/(2πLε₀)][ln(R₂/R₁)]

##### Step 3: Interpret the Result
Since R₂ > R₁, ln(R₂/R₁) is positive, making V(R₁) - V(R₂) negative.

However, physically we expect V(R₁) > V(R₂) because the inner cylinder has positive charge and the outer has negative charge.

The issue is with our integration direction. When we integrate from R₁ to R₂, we're going in the same direction as the electric field (outward), but potential decreases in the direction of the field.

Let's correct this by interpreting the negative sign properly:
V(R₁) - V(R₂) = [Q/(2πLε₀)][ln(R₂/R₁)]

This is positive, confirming that the inner cylinder is at a higher potential than the outer cylinder.

#### Part (c): Finding the Energy Stored

##### Step 1: Relate Energy to Capacitance and Potential
The energy stored in a capacitor is:
W = (1/2)CV² = (1/2)(Q²/C)

Where C is the capacitance and V is the potential difference.

##### Step 2: Find the Capacitance
Capacitance is defined as C = Q/V, where V is the potential difference.

From part (b):
V = V(R₁) - V(R₂) = [Q/(2πLε₀)][ln(R₂/R₁)]

Therefore:
C = Q/V = Q/([Q/(2πLε₀)][ln(R₂/R₁)]) = (2πLε₀)/[ln(R₂/R₁)]

##### Step 3: Calculate the Energy
Using W = (1/2)(Q²/C):
W = (1/2) × Q² × [ln(R₂/R₁)/(2πLε₀)]
  = [Q²ln(R₂/R₁)]/(4πLε₀)

Therefore, the energy stored in the capacitor is:
W = [Q²ln(R₂/R₁)]/(4πLε₀)

### Physical Interpretation
- The electric field decreases as 1/s as we move outward, which is expected due to the cylindrical geometry
- The potential difference depends logarithmically on the ratio of the radii, not their absolute values
- The energy stored depends on the square of the charge and logarithmically on the ratio of the radii

## Problem 3: Electric Field from a Circular Loop of Charge

### Problem Statement
(a) Find the electric field at point P a distance z above the center of a circular loop of radius R, which carries a uniform line charge density λ.
(b) What would you expect for the electric field when z >> R? Take this limit of your answer to (a), and check if it matches your expectation.

### Detailed Solution

#### Part (a): Finding the Electric Field

##### Step 1: Set Up the Coordinate System
- Place the circular loop in the xy-plane, centered at the origin
- The point P is located at (0, 0, z), a distance z above the center of the loop
- Due to the symmetry of the problem, we expect the electric field to have only a z-component at point P

##### Step 2: Consider a Differential Element of the Loop
Let's take a small element of the loop with length dl. This element carries a charge:
dq = λdl

##### Step 3: Calculate the Electric Field from This Element
The electric field at point P due to this charge element is:
dE = (1/4πε₀) × (dq/r²) × r̂

Where:
- r is the distance from the charge element to point P
- r̂ is the unit vector pointing from the charge element to P

##### Step 4: Analyze the Geometry
For any element on the loop, the distance to point P is:
r = √(R² + z²)

This is constant for all elements of the loop.

The position vector from an element on the loop to point P has components:
r⃗ = (-R·cosθ, -R·sinθ, z)

Where θ is the angle that locates the element on the loop.

The unit vector r̂ = r⃗/|r⃗| has components:
r̂ = (-R·cosθ/√(R² + z²), -R·sinθ/√(R² + z²), z/√(R² + z²))

##### Step 5: Extract the z-Component of the Electric Field
Due to symmetry, when we integrate around the entire loop, the x and y components will cancel out. Only the z-component remains.

The z-component of dE is:
dE_z = dE × (z/r) = (1/4πε₀) × (dq/r²) × (z/r) = (1/4πε₀) × (dq·z/r³)

Substituting dq = λdl and r = √(R² + z²):
dE_z = (1/4πε₀) × (λdl·z/(R² + z²)^(3/2))

##### Step 6: Integrate Around the Loop
The total electric field is:
E_z = ∫ dE_z = (1/4πε₀) × ∫ (λdl·z/(R² + z²)^(3/2))

Since λ, z, and (R² + z²)^(3/2) are constants for the integration:
E_z = (λz/4πε₀) × (1/(R² + z²)^(3/2)) × ∫ dl

The integral ∫ dl is just the circumference of the loop, which is 2πR:
E_z = (λz/4πε₀) × (1/(R² + z²)^(3/2)) × 2πR
    = (λzR/2ε₀) × (1/(R² + z²)^(3/2))

Therefore, the electric field at point P is:
E = (λzR/2ε₀) × (1/(R² + z²)^(3/2)) ẑ

#### Part (b): Finding the Far-Field Approximation

##### Step 1: Consider the Limit z >> R
When z is much larger than R, we can approximate (R² + z²) as z²:
(R² + z²)^(3/2) ≈ z³

Substituting into our expression for E:
E ≈ (λzR/2ε₀) × (1/z³) = (λR/2ε₀) × (1/z²) ẑ

##### Step 2: Compare with the Expected Behavior
For a point charge Q at large distance z, the electric field would be:
E = (1/4πε₀) × (Q/z²) ẑ

The total charge on the loop is Q = λ × 2πR.

Substituting this into the point charge formula:
E = (1/4πε₀) × (λ × 2πR/z²) ẑ = (λR/2ε₀) × (1/z²) ẑ

This matches our far-field approximation, confirming that at large distances, the circular loop behaves like a point charge located at the origin.

### Physical Interpretation
- Near the loop (when z is comparable to R), the field behavior is complex and depends on both z and R
- Far from the loop (z >> R), the field behaves like that of a point charge with the same total charge as the loop
- The 1/z² dependence in the far field is the expected inverse-square relationship for a point charge

## Problem 4: Determining Which Electrostatic Field is Impossible

### Problem Statement
One of the following is an impossible electrostatic field:
E⃗₁(r, θ, φ) = ρ₁(φr̂ + (cosθ/r)θ̂ + (1/sinθ)φ̂)
E⃗₂(s, φ, z) = ρ₂(s cos(φ)ŝ + szẑ)
where ρ₁ and ρ₂ are constants.

(a) Which one is impossible? Why?
(b) For the possible field, what is the charge density that caused it?

### Detailed Solution

#### Part (a): Determining Which Field is Impossible

##### Step 1: Understand the Criteria for a Valid Electrostatic Field
For a vector field to represent a valid electrostatic field, it must be curl-free (∇ × E⃗ = 0). This is because electrostatic fields are conservative.

##### Step 2: Calculate the Curl of E⃗₁ in Spherical Coordinates
The curl in spherical coordinates is:

∇ × E⃗ = 
(1/(r sinθ))[∂/∂θ(sinθ E_φ) - ∂/∂φ(E_θ)]r̂
+ (1/r)[(1/sinθ)(∂/∂φ)(E_r) - ∂/∂r(r E_φ)]θ̂
+ (1/r)[∂/∂r(r E_θ) - ∂/∂θ(E_r)]φ̂

For E⃗₁:
- E_r = ρ₁φ
- E_θ = ρ₁(cosθ/r)
- E_φ = ρ₁(1/sinθ)

Let's compute each component of the curl:

For the r̂ component:
(1/(r sinθ))[∂/∂θ(sinθ · ρ₁/sinθ) - ∂/∂φ(ρ₁cosθ/r)]
= (1/(r sinθ))[∂/∂θ(ρ₁) - ∂/∂φ(ρ₁cosθ/r)]
= (1/(r sinθ))[0 - 0]
= 0

For the θ̂ component:
(1/r)[(1/sinθ)(∂/∂φ)(ρ₁φ) - ∂/∂r(r · ρ₁/sinθ)]
= (1/r)[(1/sinθ) · ρ₁ - ∂/∂r(ρ₁r/sinθ)]
= (1/r)[(ρ₁/sinθ) - (ρ₁/sinθ)]
= 0

For the φ̂ component:
(1/r)[∂/∂r(r · ρ₁cosθ/r) - ∂/∂θ(ρ₁φ)]
= (1/r)[∂/∂r(ρ₁cosθ) - ρ₁ · ∂φ/∂θ]
= (1/r)[0 - 0]
= 0

Therefore, ∇ × E⃗₁ = 0, which means E⃗₁ could be a valid electrostatic field.

##### Step 3: Calculate the Curl of E⃗₂ in Cylindrical Coordinates
The curl in cylindrical coordinates is:

∇ × E⃗ = 
(1/s)[∂/∂z(s E_φ) - ∂/∂φ(E_z)]ŝ
+ [∂/∂s(E_z) - ∂/∂z(E_s)]φ̂
+ (1/s)[∂/∂φ(E_s) - ∂/∂s(s E_φ)]ẑ

For E⃗₂:
- E_s = ρ₂s cos(φ)
- E_φ = 0
- E_z = ρ₂sz

Computing each component:

For the ŝ component:
(1/s)[∂/∂z(s · 0) - ∂/∂φ(ρ₂sz)]
= (1/s)[0 - ρ₂sz · ∂/∂φ(1)]
= (1/s)[0 - 0]
= 0

For the φ̂ component:
[∂/∂s(ρ₂sz) - ∂/∂z(ρ₂s cos(φ))]
= [ρ₂z - ρ₂cos(φ)]
= ρ₂(z - cos(φ))

This is generally not zero, except at special points where z = cos(φ).

For the ẑ component:
(1/s)[∂/∂φ(ρ₂s cos(φ)) - ∂/∂s(s · 0)]
= (1/s)[ρ₂s · (-sin(φ)) - 0]
= -ρ₂sin(φ)

This is generally not zero either, except where φ = 0 or φ = π.

Since at least two components of the curl are non-zero, ∇ × E⃗₂ ≠ 0, which means E⃗₂ cannot be a valid electrostatic field.

Therefore, E⃗₂ is the impossible electrostatic field.

#### Part (b): Finding the Charge Density for the Possible Field

##### Step 1: Use Gauss's Law to Find the Charge Density
For the possible field E⃗₁, we need to find the charge density ρ that produces it. We use Gauss's law:
∇ · E⃗ = ρ/ε₀

The divergence in spherical coordinates is:
∇ · E⃗ = (1/r²)(∂/∂r)(r² E_r) + (1/(r sinθ))(∂/∂θ)(sinθ E_θ) + (1/(r sinθ))(∂/∂φ)(E_φ)

For E⃗₁:
- E_r = ρ₁φ
- E_θ = ρ₁(cosθ/r)
- E_φ = ρ₁(1/sinθ)

##### Step 2: Calculate Each Term of the Divergence
For the first term:
(1/r²)(∂/∂r)(r² · ρ₁φ)
= (1/r²)(∂/∂r)(r²ρ₁φ)
= (1/r²)(2rρ₁φ)
= 2ρ₁φ/r

For the second term:
(1/(r sinθ))(∂/∂θ)(sinθ · ρ₁cosθ/r)
= (ρ₁/(r² sinθ))(∂/∂θ)(sinθ cosθ)
= (ρ₁/(r² sinθ))(∂/∂θ)(sin(2θ)/2)
= (ρ₁/(r² sinθ))(cos(2θ)/2 · 2)
= (ρ₁/(r² sinθ))(cos(2θ))
= (ρ₁/(r² sinθ))(cos²θ - sin²θ)

For the third term:
(1/(r sinθ))(∂/∂φ)(ρ₁(1/sinθ))
= (1/(r sinθ))(∂/∂φ)(ρ₁) · (1/sinθ)
= (1/(r sinθ))(0) · (1/sinθ)
= 0

##### Step 3: Combine the Terms and Find the Charge Density
∇ · E⃗₁ = 2ρ₁φ/r + (ρ₁/(r² sinθ))(cos(2θ)) + 0
        = 2ρ₁φ/r + (ρ₁cos(2θ)/(r² sinθ))

Using Gauss's law, the charge density is:
ρ = ε₀∇ · E⃗₁
  = ε₀[2ρ₁φ/r + (ρ₁cos(2θ)/(r² sinθ))]

Therefore, the charge density that produced the electric field E⃗₁ is:
ρ(r, θ, φ) = ε₀[2ρ₁φ/r + (ρ₁cos(2θ)/(r² sinθ))]

### Physical Interpretation
- Field E⃗₂ is not a valid electrostatic field because it has non-zero curl, meaning it's not conservative
- Field E⃗₁ is valid and is produced by a complex charge distribution that depends on r, θ, and φ
- The charge density for E⃗₁ has a 1/r term (which decreases with distance) and a 1/r² term (which decreases more rapidly)
- The angular dependence through cos(2θ) and sinθ creates a complex spatial pattern

## Additional Insights: Vector Calculus Identities and Their Applications in Electrostatics

### Divergence of a Curl is Zero

∇·(∇×A⃗) = 0 for any vector field A⃗

This identity explains why charge is conserved in electrostatics. Since ∇×E⃗ = 0 (electrostatic fields are curl-free), we can write E⃗ = -∇V. Then, using Gauss's law ∇·E⃗ = ρ/ε₀, we get Poisson's equation ∇²V = -ρ/ε₀.

### Curl of a Gradient is Zero

∇×(∇f) = 0 for any scalar function f

This is why electrostatic fields are conservative. We can write E⃗ = -∇V, ensuring that ∇×E⃗ = ∇×(-∇V) = 0.

### The Method of Images for Solving Electrostatic Problems

The method of images replaces conductors with imaginary "image charges" to create the same boundary conditions:

1. For a point charge q near a grounded infinite conducting plane, the image is a charge -q placed symmetrically on the opposite side of the plane.
2. For a point charge q at distance d from the center of a grounded conducting sphere of radius R, the image is a charge -q(R/d) placed at distance R²/d from the center.

This approach dramatically simplifies calculations while preserving the physics.

## Specific Physical Phenomena in Electrostatics

### Conductors and Surface Charge Distribution

On irregularly shaped conductors, charge tends to accumulate at locations with higher curvature (sharp points). This is why lightning rods have sharp tips to create high electric fields that can ionize air molecules.

### Dielectric Materials and Polarization

Dielectrics (insulators) modify electric fields through polarization (alignment of molecular dipoles). This is described by:
E = E₀/κ
Where κ is the dielectric constant of the material.

### Capacitors in Series and Parallel

For capacitors in series: 1/C_eq = 1/C₁ + 1/C₂ + 1/C₃ + ...
For capacitors in parallel: C_eq = C₁ + C₂ + C₃ + ...

## Summary of Key Equations in Electrostatics

1. Coulomb's Law: F = (1/4πε₀) × (q₁q₂/r²) × r̂
2. Electric Field: E = (1/4πε₀) × (q/r²) × r̂
3. Gauss's Law: ∮ E·dA = Q_enclosed/ε₀
4. Electric Potential: V = (1/4πε₀) × (q/r)
5. Relation between Field and Potential: E = -∇V
6. Poisson's Equation: ∇²V = -ρ/ε₀
7. Laplace's Equation (in charge-free regions): ∇²V = 0
8. Energy in Electric Field: W = (ε₀/2)∫|E|² dτ
9. Capacitance: C = Q/V

These fundamental equations, combined with the mathematical tools of vector calculus, provide a complete framework for analyzing electrostatic phenomena and solving complex problems like those presented in the Physics 401 course.

# Comprehensive Electrostatics Study Guide

## I. Fundamental Principles of Electrostatics

### 1. Coulomb's Law

Coulomb's law describes the force between two point charges:

$$F = \frac{1}{4\pi\varepsilon_0} \frac{q_1 q_2}{r^2} \hat{r}$$

Where:
- $F$ is the force vector (newtons)
- $\varepsilon_0 = 8.85 \times 10^{-12}$ C²/(N·m²) is the permittivity of free space
- $q_1$ and $q_2$ are the charges (coulombs)
- $r$ is the distance between the charges (meters)
- $\hat{r}$ is the unit vector pointing from one charge to the other
- The constant $\frac{1}{4\pi\varepsilon_0} \approx 9 \times 10^9$ N·m²/C²

The force is repulsive for like charges and attractive for opposite charges.

### 2. Electric Field

The electric field is defined as the force per unit charge:

$$E = \frac{F}{q_0}$$

For a point charge $q$, the electric field at distance $r$ is:

$$E = \frac{1}{4\pi\varepsilon_0} \frac{q}{r^2} \hat{r}$$

Units: N/C or V/m (equivalent)

For multiple charges, the principle of superposition applies:
$$E_{total} = E_1 + E_2 + E_3 + \ldots$$

### 3. Continuous Charge Distributions

For continuous distributions, we use charge density:
- Linear charge density ($\lambda$): C/m
- Surface charge density ($\sigma$): C/m²
- Volume charge density ($\rho$): C/m³

The electric field due to a continuous charge distribution is:

$$E(\vec{r}) = \frac{1}{4\pi\varepsilon_0} \int \frac{\rho(\vec{r}')}{|\vec{r}-\vec{r}'|^3} (\vec{r}-\vec{r}') d\tau'$$

### 4. Gauss's Law

Gauss's law states that the total electric flux through a closed surface is proportional to the enclosed charge:

$$\oint \vec{E} \cdot d\vec{A} = \frac{Q_{enclosed}}{\varepsilon_0}$$

This is particularly useful for charge distributions with symmetry (spherical, cylindrical, planar).

### 5. Electric Potential

Electric potential is the potential energy per unit charge:

$$V = \frac{U}{q_0}$$

For a point charge:

$$V = \frac{1}{4\pi\varepsilon_0} \frac{q}{r}$$

The relationship between electric field and potential:

$$\vec{E} = -\vec{\nabla}V$$

For a continuous charge distribution:

$$V(\vec{r}) = \frac{1}{4\pi\varepsilon_0} \int \frac{\rho(\vec{r}')}{|\vec{r}-\vec{r}'|} d\tau'$$

Potential difference between points A and B:

$$V_B - V_A = -\int_A^B \vec{E} \cdot d\vec{l}$$

### 6. Conductors in Electrostatic Equilibrium

Key properties:
1. Electric field inside a conductor is zero
2. All excess charge resides on the surface
3. Electric field just outside is perpendicular to the surface
4. Field magnitude just outside equals $\sigma/\varepsilon_0$
5. The entire conductor is at constant potential

## II. Vector Calculus for Electrostatics

### 1. Gradient (∇f)

The gradient points in the direction of maximum increase of a scalar function with magnitude equal to the rate of change.

Cartesian coordinates:
$$\vec{\nabla}f = \frac{\partial f}{\partial x}\hat{x} + \frac{\partial f}{\partial y}\hat{y} + \frac{\partial f}{\partial z}\hat{z}$$

Spherical coordinates:
$$\vec{\nabla}f = \frac{\partial f}{\partial r}\hat{r} + \frac{1}{r}\frac{\partial f}{\partial \theta}\hat{\theta} + \frac{1}{r\sin\theta}\frac{\partial f}{\partial \phi}\hat{\phi}$$

Cylindrical coordinates:
$$\vec{\nabla}f = \frac{\partial f}{\partial s}\hat{s} + \frac{1}{s}\frac{\partial f}{\partial \phi}\hat{\phi} + \frac{\partial f}{\partial z}\hat{z}$$

### 2. Divergence (∇·A)

The divergence measures how much a vector field "spreads out" from a point.

Cartesian coordinates:
$$\vec{\nabla} \cdot \vec{A} = \frac{\partial A_x}{\partial x} + \frac{\partial A_y}{\partial y} + \frac{\partial A_z}{\partial z}$$

Spherical coordinates:
$$\vec{\nabla} \cdot \vec{A} = \frac{1}{r^2}\frac{\partial}{\partial r}(r^2 A_r) + \frac{1}{r\sin\theta}\frac{\partial}{\partial \theta}(\sin\theta A_\theta) + \frac{1}{r\sin\theta}\frac{\partial A_\phi}{\partial \phi}$$

Cylindrical coordinates:
$$\vec{\nabla} \cdot \vec{A} = \frac{1}{s}\frac{\partial}{\partial s}(sA_s) + \frac{1}{s}\frac{\partial A_\phi}{\partial \phi} + \frac{\partial A_z}{\partial z}$$

### 3. Curl (∇×A)

The curl measures rotational behavior of a vector field.

Cartesian coordinates:
$$\vec{\nabla} \times \vec{A} = \left(\frac{\partial A_z}{\partial y} - \frac{\partial A_y}{\partial z}\right)\hat{x} + \left(\frac{\partial A_x}{\partial z} - \frac{\partial A_z}{\partial x}\right)\hat{y} + \left(\frac{\partial A_y}{\partial x} - \frac{\partial A_x}{\partial y}\right)\hat{z}$$

Spherical coordinates:
$$\vec{\nabla} \times \vec{A} = \frac{1}{r\sin\theta}\left[\frac{\partial}{\partial \theta}(A_\phi\sin\theta) - \frac{\partial A_\theta}{\partial \phi}\right]\hat{r} + \frac{1}{r}\left[\frac{1}{\sin\theta}\frac{\partial A_r}{\partial \phi} - \frac{\partial}{\partial r}(rA_\phi)\right]\hat{\theta} + \frac{1}{r}\left[\frac{\partial}{\partial r}(rA_\theta) - \frac{\partial A_r}{\partial \theta}\right]\hat{\phi}$$

Cylindrical coordinates:
$$\vec{\nabla} \times \vec{A} = \left(\frac{1}{s}\frac{\partial A_z}{\partial \phi} - \frac{\partial A_\phi}{\partial z}\right)\hat{s} + \left(\frac{\partial A_s}{\partial z} - \frac{\partial A_z}{\partial s}\right)\hat{\phi} + \frac{1}{s}\left[\frac{\partial}{\partial s}(sA_\phi) - \frac{\partial A_s}{\partial \phi}\right]\hat{z}$$

### 4. Laplacian (∇²f)

The Laplacian is the divergence of the gradient:
$$\nabla^2 f = \vec{\nabla} \cdot (\vec{\nabla}f)$$

Cartesian coordinates:
$$\nabla^2 f = \frac{\partial^2 f}{\partial x^2} + \frac{\partial^2 f}{\partial y^2} + \frac{\partial^2 f}{\partial z^2}$$

Related equations:
- Poisson's equation: $\nabla^2 V = -\frac{\rho}{\varepsilon_0}$
- Laplace's equation (in charge-free regions): $\nabla^2 V = 0$

### 5. Vector Calculus Theorems

**Gradient Theorem:**
$$\int_a^b (\vec{\nabla}f) \cdot d\vec{l} = f(b) - f(a)$$

**Divergence Theorem:**
$$\int_V (\vec{\nabla} \cdot \vec{A})d\tau = \oint_S \vec{A} \cdot d\vec{A}$$

**Stokes' Theorem:**
$$\int_S (\vec{\nabla} \times \vec{A}) \cdot d\vec{A} = \oint_C \vec{A} \cdot d\vec{l}$$

## III. Problem-Solving Techniques

### 1. Method of Images

The method of images replaces conductors with imaginary charges that create equivalent boundary conditions.

For a point charge near a grounded conducting plane:
1. Place an opposite charge symmetrically on the other side
2. This creates zero potential at the plane location
3. Calculate fields using superposition

For a line charge parallel to a conducting plane:
1. Place an opposite line charge symmetrically on the other side
2. Calculate fields using superposition

### 2. Using Gauss's Law Effectively

1. Identify symmetry in the problem
2. Choose a Gaussian surface that exploits the symmetry
3. Determine where E is parallel to dA and where it's perpendicular
4. Calculate the enclosed charge
5. Solve for the electric field

### 3. Working with Capacitors

Capacitance definitions:
- $C = \frac{Q}{V}$ (charge per voltage)
- Energy stored: $W = \frac{1}{2}CV^2 = \frac{1}{2}\frac{Q^2}{C} = \frac{1}{2}QV$

For a cylindrical capacitor:
- $C = \frac{2\pi\varepsilon_0 L}{\ln(R_2/R_1)}$

### 4. Checking if a Field is a Valid Electrostatic Field

A valid electrostatic field must be:
1. Curl-free: $\vec{\nabla} \times \vec{E} = 0$ (conservative field)
2. Satisfy Gauss's law: $\vec{\nabla} \cdot \vec{E} = \frac{\rho}{\varepsilon_0}$

For an electrostatic field, $\vec{E} = -\vec{\nabla}V$, which ensures it's curl-free.

### 5. Finding Charge Density from Electric Field

Use Gauss's law in differential form:
$$\rho = \varepsilon_0 \vec{\nabla} \cdot \vec{E}$$

### 6. Far-Field Approximations

For charge distributions at large distances (r >> size of distribution):
- Distribution behaves approximately like a point charge with the total charge
- Field follows $1/r^2$ dependence
- Makes calculations much simpler

## IV. Detailed Solutions to Example Problems

### Problem 1: Infinite Line Charge Parallel to a Grounded Conducting Plate

#### Key Approach: Method of Images
For a grounded conducting plate, replace it with an image charge of opposite sign.

#### Solution Steps:
1. Replace the grounded plate with an image line charge of -λ at y = -a
2. Calculate the field from both the real and image charges
3. Sum the contributions using superposition

#### Electric Field:
$$E = -\frac{\lambda a}{\pi\varepsilon_0(a^2-y^2)}\hat{y}$$

#### Force per Unit Length:
$$\frac{F}{L} = -\frac{\lambda^2}{4\pi\varepsilon_0 a}\hat{y}$$

The negative sign indicates attraction toward the plate.

#### Physical Insights:
- The field grows stronger as y approaches either the line charge or the plate
- The force is inversely proportional to the distance between the line and the plate

### Problem 2: Cylindrical Capacitor

#### Key Approach: Gauss's Law with Cylindrical Symmetry

#### Solution Steps:
1. Use a cylindrical Gaussian surface at radius s (R₁ < s < R₂)
2. Apply Gauss's law to find the electric field
3. Integrate the field to find the potential difference
4. Calculate capacitance and energy

#### Electric Field:
$$E = \frac{Q}{2\pi\varepsilon_0 s L}\hat{s}$$

#### Potential Difference:
$$V(R_1) - V(R_2) = \frac{Q}{2\pi\varepsilon_0 L}\ln\left(\frac{R_2}{R_1}\right)$$

#### Energy Stored:
$$W = \frac{Q^2\ln(R_2/R_1)}{4\pi\varepsilon_0 L}$$

#### Physical Insights:
- Electric field decreases as 1/s due to cylindrical geometry
- Potential difference depends logarithmically on the radius ratio
- Energy stored depends on the square of the charge

### Problem 3: Electric Field from a Circular Loop of Charge

#### Key Approach: Direct Integration with Symmetry Considerations

#### Solution Steps:
1. Identify symmetry: only the z-component of the field survives at points along the axis
2. Set up the integral for a differential element of the loop
3. Find the distance from each element to the field point
4. Integrate around the loop

#### Electric Field:
$$E = \frac{\lambda z R}{2\varepsilon_0(R^2 + z^2)^{3/2}}\hat{z}$$

#### Far-Field Approximation (z >> R):
$$E \approx \frac{\lambda R}{2\varepsilon_0 z^2}\hat{z}$$

#### Physical Insights:
- Near the loop, the field behavior is complex
- Far from the loop, it behaves like a point charge with Q = 2πRλ
- The transition to point-charge behavior occurs when z >> R

### Problem 4: Determining Which Electrostatic Field is Impossible

#### Key Approach: Test if the Field is Curl-Free

#### Solution Steps:
1. Calculate the curl of each field
2. If curl is non-zero, the field cannot be an electrostatic field
3. For the valid field, find charge density using $\rho = \varepsilon_0 \vec{\nabla} \cdot \vec{E}$

#### Field E₁:
$$E_1(r, \theta, \phi) = \rho_1(\phi\hat{r} + \frac{\cos\theta}{r}\hat{\theta} + \frac{1}{\sin\theta}\hat{\phi})$$

Curl calculation shows $\vec{\nabla} \times \vec{E}_1 = 0$ (valid electrostatic field)

#### Field E₂:
$$E_2(s, \phi, z) = \rho_2(s\cos(\phi)\hat{s} + sz\hat{z})$$

Curl calculation shows $\vec{\nabla} \times \vec{E}_2 \neq 0$ (impossible electrostatic field)

#### Charge Density for E₁:
$$\rho = \varepsilon_0\left[\frac{2\rho_1\phi}{r} + \frac{\rho_1\cos(2\theta)}{r^2\sin\theta}\right]$$

#### Physical Insights:
- Electrostatic fields must be conservative (curl-free)
- Complex charge distributions can create intricate field patterns
- The charge density for E₁ has 1/r and 1/r² components

## V. Problem-Solving Strategies

### 1. Identify Symmetry First
- Spherical symmetry → Use spherical coordinates
- Cylindrical symmetry → Use cylindrical coordinates
- Planar symmetry → Use Cartesian coordinates
- Symmetry determines the form of the solution and simplifies calculations

### 2. Choose the Right Mathematical Tool
- Point charges or simple distributions → Direct application of Coulomb's law
- Symmetric charge distributions → Gauss's law
- Complex geometries → Method of images
- Finding E from V → Take the negative gradient
- Finding V from E → Line integral

### 3. Breaking Complex Problems into Manageable Parts
1. Identify the physical principles involved
2. Sketch the setup and define coordinates
3. Apply the appropriate mathematical tools
4. Use superposition for multiple charges
5. Check limiting cases and dimensional consistency

### 4. Common Pitfalls and How to Avoid Them

#### Sign Errors
- Be careful with coordinate directions
- Remember that E points away from positive charges and toward negative charges
- Check if forces are attractive or repulsive based on charge signs

#### Integration Direction
- When integrating E to find V, remember the negative sign
- Potential decreases in the direction of the electric field

#### Curl and Divergence Calculations
- Use the correct formulas for the chosen coordinate system
- Check component by component
- Verify that curl is zero for electrostatic fields

#### Boundary Conditions
- At conductor surfaces: E is perpendicular and V is constant
- At charge distributions: E has a discontinuity related to the surface charge density

## VI. Mathematical Relations and Equations to Memorize

### Key Equations for Quick Reference

#### Electric Field
- Point charge: $E = \frac{1}{4\pi\varepsilon_0} \frac{q}{r^2}$
- Infinite line charge: $E = \frac{\lambda}{2\pi\varepsilon_0 r}$
- Infinite plane with uniform charge density: $E = \frac{\sigma}{2\varepsilon_0}$
- Conducting sphere (outside): $E = \frac{1}{4\pi\varepsilon_0} \frac{Q}{r^2}$
- Inside a conductor: $E = 0$

#### Electric Potential
- Point charge: $V = \frac{1}{4\pi\varepsilon_0} \frac{q}{r}$
- Infinite line charge: $V = -\frac{\lambda}{2\pi\varepsilon_0} \ln(r) + C$
- Parallel plate capacitor: $V = Ed$ (where d is the separation)

#### Capacitance
- Parallel plate: $C = \frac{\varepsilon_0 A}{d}$
- Cylindrical: $C = \frac{2\pi\varepsilon_0 L}{\ln(R_2/R_1)}$
- Spherical: $C = 4\pi\varepsilon_0 \frac{R_1 R_2}{R_2 - R_1}$

#### Energy Relations
- Energy density in electric field: $u = \frac{1}{2}\varepsilon_0 E^2$
- Energy stored in capacitor: $W = \frac{1}{2}CV^2 = \frac{1}{2}\frac{Q^2}{C}$

### Vector Identities Useful for Electrostatics

- $\vec{\nabla} \times (\vec{\nabla}f) = 0$
- $\vec{\nabla} \cdot (\vec{\nabla} \times \vec{A}) = 0$
- $\vec{\nabla} \cdot (f\vec{A}) = f(\vec{\nabla} \cdot \vec{A}) + \vec{A} \cdot (\vec{\nabla}f)$
- $\vec{\nabla} \times (f\vec{A}) = f(\vec{\nabla} \times \vec{A}) + (\vec{\nabla}f) \times \vec{A}$
- $\vec{\nabla}(f \cdot g) = f\vec{\nabla}g + g\vec{\nabla}f$

## VII. Mental Models and Physical Intuition

### 1. Field Line Visualization
- Electric field lines start on positive charges and end on negative charges
- Field line density indicates field strength
- Field lines never cross
- Field lines are perpendicular to equipotential surfaces

### 2. Energy Perspective
- Systems tend toward configurations with lower potential energy
- Opposite charges attract to minimize energy
- Like charges repel to maximize the distance between them
- Energy is stored in the electric field itself

### 3. Cause and Effect Relationships
- Charges create electric fields
- Electric fields exert forces on other charges
- Potential difference drives the movement of charges
- Moving charges create currents and magnetic fields

### 4. Thinking in Terms of Flux
- Electric flux represents the "flow" of electric field through a surface
- Gauss's law connects flux to enclosed charge
- Positive flux = field lines leaving the surface
- Negative flux = field lines entering the surface

## VIII. Practical Applications

### 1. Capacitors and Energy Storage
- Energy density is proportional to E²
- Capacitance depends on geometry and material
- Dielectrics increase capacitance by reducing the effective electric field

### 2. Electrostatic Shielding
- Conductors can shield interior regions from external electric fields
- Faraday cages work based on this principle
- Important for protecting sensitive electronics

### 3. High Voltage Engineering
- Corona discharge occurs at sharp points where field is strongest
- Lightning rods use this principle to safely discharge atmospheric electricity
- Insulation breakdown occurs when field exceeds a critical value

### 4. Electrostatic Precipitators
- Use electric fields to charge and collect particles
- Applied in pollution control and industrial processes
- Efficiency depends on field strength and particle properties

## IX. Test-Taking Strategies

### 1. Problem Categorization
When facing a new problem, quickly categorize it:
- Coulombic (direct force/field calculations)
- Gaussian (symmetry-based field calculations)
- Boundary value problem (method of images)
- Field verification (curl/divergence tests)

### 2. Dimensional Analysis
- Always check units for consistency
- Use dimensional analysis to verify equations
- Common units: N/C or V/m for E, V for potential, C for charge

### 3. Limiting Case Analysis
- Check behavior as r → 0 or r → ∞
- Verify symmetry implications
- Compare with known simple cases

### 4. Common Integration Techniques
- For spherical symmetry: $\int \sin\theta d\theta d\phi = 4\pi$
- For cylindrical problems: $\int_0^{2\pi} d\phi = 2\pi$
- For 1/r potentials: $\int \frac{1}{r} dr = \ln(r)$

### 5. Time Management
- Identify the core physical principle quickly
- Set up the problem with appropriate math tools
- Use symmetry to reduce computational effort
- Always verify your answer with a quick dimensional check

## X. Practice Problems

To fully master the concepts, try these additional practice problems:

1. A thin spherical shell of radius R has a uniform surface charge density σ. Find the electric field and potential at all points in space.

2. Two long, parallel line charges with linear densities +λ and -λ are separated by distance d. Find the electric field at all points in the plane perpendicular to both lines.

3. A point charge q is at distance d from the center of a grounded conducting sphere of radius R (where d > R). Find the force on the point charge.

4. Find the capacitance of two concentric conducting spheres with radii a and b (b > a).

5. Verify whether the electric field $\vec{E} = \alpha(y\hat{x} + x\hat{y} + z\hat{z})$ could be an electrostatic field. If possible, find the corresponding potential and charge distribution.

6. A uniformly charged disk of radius R has surface charge density σ. Find the electric field at a point on the axis of the disk at distance z from the center.

7. A hemispherical bowl of radius R carries a uniform surface charge density σ. Find the electric field at the center of the hemisphere.

8. Two large, parallel conducting plates separated by distance d have equal and opposite charge densities ±σ. A thin conducting sheet is inserted parallel to the plates at distance d/3 from the negative plate. Find the surface charge density induced on both sides of the conducting sheet.

Remember to apply the systematic approach outlined in this guide to each problem. Identify the symmetry, choose the appropriate mathematical tools, and verify your solutions through dimensional analysis and limiting case behavior.