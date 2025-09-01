(stokes-section)=
# Stokes flow

Stokes equation is a simplified form of Navier-Stokes equation that assumes that one can neglect inertial forces (and thus turbulence). It takes the following form:

```{math}
:label: stokes-force
\frac{\partial\tau_{ij}}{\partial x_j}=\frac{\partial p}{\partial x_i}-\rho gz_i
```

where $\tau_{ij}$ are the compnents of the stress tensor, $p$ the pressure, $\rho$ the density, $g$ the gravitational acceleration and $z_i$ the components of a vector pointing in the direction of $g$. $x_i$ represents the spatial coordinates.

```{note}
A Stoke fluid is, by definition, devoid of inertia which implies that if the driving force stops, the fluid motion stops instantaneously. Honey behaves like a Stoke fluid: if you stir a honey jar with a spoon, once you remove the spoon, the honey stops moving instantly. This behaviour is also observed in the Earth on geological time scales: it explains why hot spot chains (like the [Hawaiian-Emperor seamont chain](https://www.usgs.gov/media/images/hawaiian-emperor-seamount-chain)) display very abrupt strike changes that correspond to "instantaneous" changes in plate velocities.
```

Equation {eq}`stokes-force` represents the balance between three forces that must exist at any point within the fluid:
1. the first term (on the left-hand side of the equation) represents the viscous forces
2. the second term (on the right-hand side of the equation) represents the forces arising from pressure gradient inside the fluid;
3. the third term (last on the right) represents the gravitational forces.

Note that this equation does not contain any time dependency. In other words, the flow is static unless the boundary conditions or one of the parameters (the distribution of density for example) varies with time.

```{note}
Stokes flow have interesting properties. One of them is that they are perfectly reversible. This can be appreciated on the [following video](https://www.youtube.com/watch?v=rA6T83FKuE8)
```

If we wish to use Stokes equation to represent the motion and deformation of plates and flow in the underlying mantle, we must also assume that the flow is incompressible. Mathematically, this is equivalent to assuming that, at every point within the fluid, the divergence of the velocity vector is nil. In other words:
```{math}
:label: incompressibility
\frac{\partial u_i}{\partial x_i}=0
```
where $u_i$ are the components of the velocity vector. Note that in this equation as in equation {eq}`stokes-force`, we have used [Einstein's notation](https://en.wikipedia.org/wiki/Einstein_notation) which assumes that if an index appears more than once in a single term and is not otherwise defined, it implies summation.

We see that the first equation {eq}`stokes-force` refers to stresses (or forces), whereas the second {eq}`incompressibility` referes to velocities. To combine the two equations, one needs to introduce a rheological law or {term}`rheology`, i.e., a rule that defines the relationship between deformation (velocity) and stress (force). Here we assume a non-linear viscous behaviour of the form:
```{math}
:label: rheology
\dot\epsilon_{ij} = B^{-n}T^{n-1}\sigma_{ij}
```
where $\dot\epsilon_{ij}$ is the strain rate tensor, defined from the spatial derivatives of the velocity vector:
```{math}
:label: strain-rate
\dot\epsilon_{ij}=\frac{1}{2}\Bigl(\frac{\partial u_i}{\partial x_j}+\frac{\partial u_j}{\partial x_i}\Bigr)
```
$B$ is a constant and $n$ an exponent that represents the non-linearity of the rheological law (the rheology is linear is $n=1$). Using values of $n>1$ implies that the material is strain softening, i.e., its viscosity drops as the strain rate increases. $T$ is the second {term}`invariant` of the deviatoric part of the stress tensor. The deviatoric part means that the pressure has been substracted from the diagonal elements of the stress tensor. The second invariant is a special combination of the tensor components that remains invariant in any system of reference (the pressure is the first invariant of the stress tensor). More information on the invariants of a tensor can be found [here](https://en.wikipedia.org/wiki/Invariants_of_tensors).

````{note}
Note that the viscosity of rocks is also a strong (exponential) function of temperature. This is because the temperature inside the Earth varies from 0 near the surface to several thousands of degree in its deep interior.
```{figure} images/temperature-profile.jpeg
---
height: 250px
name: temperature-profile
---
Earth's internal temperature structure from {cite:t}`steinberger2006models-a0f`
```
Over that range of temperature (and pressure) values the viscosity of Earth's material (rocks) varies by many orders of magnitude.
```{figure} images/viscosity-profile.jpeg
---
height: 250px
name: viscosity-profile
---
Earth's internal viscosity structure from {cite:t}`steinberger2006models-a0f`
```
````