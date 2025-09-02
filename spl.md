(spl-section)=
# Stream Power Law

## Basic equation

The Stream Power Law (SPL) or Stream Power Incision Model (SPIM) {cite:p}`Whipple1999JournalofGeophysicalResearchSolidEarth19782012` describes the competition between uplift and river incision to control the amplitude of surface topography. Mathematically it is expressed as:
```{math}
:label: spl
\frac{\partial h}{\partial t}=U-K_fA^mS^n
```
where $h$ is the elevation of the river bed, $U$ is tectonic uplift, $A$ is {term}`drainage area<drainage area>`, a proxy for water discharge, and $S$ is slope. $K_f$ is a rate constant that depends on many parameters including rainfall, lithology or vegetation; $m$ and $n$ are exponents. All three are poorly constrained.

````{note}
A more general version of the SPL assumes that incision by the river is proportional to water discharge, $\Phi$, which is the integral of the rainfall rate, $\nu$, over the upstream drainage area, $A$:
```{math}
\Phi=\int_A\nu\ dA
```
It is commonly assumed that rainfall rate is uniform over a catchment, or, more correctly, that variations in rainfall rate occur on a broader scale than that of a single catchment. In that case, the discharge is equal to the product of the drainage aerea $A$ by the mean rainfall rate, $\bar\nu$, which justifies the use of catchment area as a proxy for discharge. It also implies that the rate constant $K_f$ in equation {eq}`spl` contains the mean rainfall rate to the power $m$, i.e., $K_f\propto\bar\nu^m$.
````