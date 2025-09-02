# Principle of isostasy

## Simple formulation

The principle of {term}`isostasy<isostasy>` is Archimede's principle applied to the Earth's {term}`lithosphere<lithosphere>`/{term}`asthenosphere<asthenosphere>` system. It can be simply stated as **all lithospheric columns must have the same weight**. It relies on the existence of a so-called compensation depth, which corresponds to a level in the Earth's interior that has very low viscosity (the asthenosphere) and thus behaves, on geological time scales, as an inviscid fluid. Such a fluid cannot sustain any horizontal stress and therefore the weight of any column of material above it must be uniform. This compensation depth is usually taken as the base of the lithosphere, which is commonly regarded as the depth where the {term}`geotherm<geotherm>` is closest to the solidus and thus considered as the least viscous layer in the Earth's upper regions.

```{warning}
Even though the viscosity of the asthenosphere is much lower than that of the overlying lithosphere, it remains finite. This means, for example, that the flow of asthenosphere caused by loading of an ice sheet will take several tens of thousands of years to bring the system into isostatic equilibrium. Although very large on human time scales, this time can be considered as negligible compared to the tectonic time scales of the order of millions of years. This is why one can consider, when considering tectonic processes, that isostatic adjustment is instantaneous.
```

## Mathematical form

From the definition of the principle of isostasy, one can see that it is most useful when used to compare the topography between two lithospheric columns, for example, the difference in height between a continental interior and a mountain belt.

In mathematical form, the principle of isostasy can be written as:
```{math}
\Delta \sigma_{zz}=g\int_{z_0}^L\Delta\rho\ dz=0
```
where $\Delta\rho$ is the difference in density between any two columns of lithosphere (as a function of $z$), $L$ is the compensation depth, $z_0$ is the height of the surface topography and $g$ is the gravitational acceleration.

```{note}
The principle of isostasy is also a direct consequence of the quasi-static form of Newton's second law that the sum of all forces at any point must be equal to zero.
```

## Potential energy

Note that, under the quasi-static approximation, Newton's second law also implies that the sum of all torques (or force moments) at any point must be balanced; this implies that, even if two lithospheric columns are in isostatic balance, there may exist a horizontal stress exerted by one column on the other {cite:p}`Fleitout1982Tectonics`:
```{math}
\bar\tau_{xx}=\frac{g}{L}\int_{z_0}^L\Delta\rho\ z\ dz\ne 0
```
One also states that the two columns have different potential energy. This implies that unless an external force acts on the system, a lithosphere characterized by a thickened crust will naturally deform and thin, until its potential energy becomes identical to that of a reference or adjacent column. This may lead, for example, to orogenic collapse once the tectonic force that drives continantal collision stops acting.

```{note}
The principle of isostasy neglects the strength of the lithosphere and the potential it has for sustaining a differential horizontal stress. To address this limitation, one commonly assumes that the lithospehre behaves as a thin elastic plate that is able to sustain some of the stress imposed by additional topography (caused by crustal thickening for example) by flexing. This leads to the concept of {term}`flexural isostasy <flexural isostasy>`.
```
