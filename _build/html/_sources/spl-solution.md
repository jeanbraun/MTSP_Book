# Steady-state profile

The Stream Power Law - equation {eq}`spl` - requires the computation of the drainage area, $A$, at every point of the landscape. Hack's Law {cite:p}`hack1957studies-a1b` state that drainage area varies as a power law of the distance along a stream from the source:
```{math}
A = k(L-x)^p
```
where $x$ is the distance from base level, $L$ is the length of the river (from base level to the source) and $k$ and $p$ are two constants/parameters. The value of these parameters is relatively well constrained {cite:p}`hack1957studies-a1b,he2024global-c99`.

We can use Hack's Law to derive from the SPL a differential equation governing the evolution of the river profile:
```{math}
\frac{\partial h}{\partial t}= U -K_f\Bigr(k(L-x)^p\Bigr)^m\Bigl(\frac{\partial h}{\partial x}\Bigr)^n
```

If we assume steady-state, we obtain a simple differential equation:
```{math}
\frac{\partial h}{\partial x}=\Bigl(\frac{U}{K_fk^m}\Bigr)^{1/n}(L-x)^{-mp/n}
```
that we can use to predict the steady-state profile of a river:
```{math}
h(x) = h_0\bigl[L^{1-mp/n}-(L-x)^{1-mp/n}\bigr]
```
where
```{math}
h_0=\Bigl(\frac{U}{K_fk^m}\Bigr)^{1/n}\frac{1}{1-mp/n}
```
The total river or basin relief, $h_r$, i.e., the difference in height between base level and the source of the river, is given by $h(L)$:
```{math}
h_r=h(L)=h_0L^{1-mp/n}
```

If we normalize height by $h_r$ and distance by $L$, i.e., $h'=h/h_0$ and $x'=x/L$, we can write this solution in its dimensionless form:
```{math}
h'(x')=1-(1-x)^{1-mp/n}
```