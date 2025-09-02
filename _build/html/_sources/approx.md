# Thin sheet approximation

## Basic assumptions

The thin sheet approximation is an application of Stokes equation to the behaviour of a thin viscous sheet. It implies:
1. that vertical columns in the sheet cannot be sheared
2. that all variables and properties can be approximated by their vertically averaged values

This can be expressed mathematically as:
```{math}
\dot\epsilon_{13}=\dot\epsilon_{31}=\dot\epsilon_{23}=\dot\epsilon_{32}=0
```
where the 3rd index corresponds to the vertical component, and by integrating Stokes equation along the vertical dimension.

## Thin sheet equation

Using also the incompressibility condition - equation{eq}`incompressibility` -  that can be expressed in terms of the strain rate components:
```{math}
\dot\epsilon_{33}=-(\dot\epsilon_{11}+\dot\epsilon_{22})
```
this yields:
```{math}
B\dot E^{1/n-1}\frac{\dot\epsilon_{ij}}{\partial x_j}+B(1/n-1)\frac{\partial \dot E}{\partial x_j}\dot E^{1/n-2}\dot\epsilon_{ij}=\frac{\partial\bar p}{\partial x_i}
```
where $\bar p$ is the vertically averaged pressure:
```{math}
\bar p=\frac{1}{L}\int_0^L p\ dz=\frac{g\rho_ch^2}{2L}(1-\rho_c/\rho_m)+\frac{g\rho_mL}{2}
```
$L$ and $h$ are the lithospheric and crustal thicknesses, respectively, $\rho_c$ and $\rho_m$ the crustal and mantle densities and $\dot E$ is the second {term}`invariant<invariant>` of the strain rate tensor.

## Interpretation

Combining the last two equations yields:
```{math}
:label: thinsheet
\frac{1}{2}\frac{\partial}{\partial x_j}(\frac{\partial u_j}{\partial x_i}+\frac{\partial u_i}{\partial x_j})=\frac{g\rho_c h}{BL}(1-\rho_c/\rho_m)\dot E^{1-1/n}\frac{\partial h}{\partial x_i}+(1-1/n)\dot E^{-1}\frac{\partial\dot E}{\partial x_j}\dot\epsilon_{ij}
```
where the indices $i$ and $j$ now only vary between 1 and 2.

In this formulation the pressure gradients arise from lateral variations in density interfaces; it implies that there remain only two forces at play and the equation therefore expresses a balance between viscous and gravitational forces only. The first term in equation{eq}`thinsheet` is the main viscous term, the second the gravitational term and the third term arises from the non-linearity of the rheology (it drops out when $n=1$).
