# SPL in details

## Hypotheses

Here, inspired by {cite:t}`Whipple1999JournalofGeophysicalResearchSolidEarth19782012`, we provide the details of the derivation of the SPL so that the reader can appreciate the hypotheses and approximations it is based on.

`````{tab-set}

````{tab-item} Erosion rate
##### Hypothesis
Erosion rate is proportional to shear stress exerted by river flow on the bedrock to the power $a$:
```{math}
\dot\epsilon=k_b\tau_b^a
```
Note that this shear stress definition includes the effect of tools carried by the river. It also assumed that there exists no threshold for motion/erosion. See the effect of including a threshold in {cite:t}`Deal2018JournalofGeophysicalResearchEarthSurface`, for example.

Typical value for $a$ is 5/2, assuming that the dominant eroding mechanism is abrasion, or 1 for plucking (see {cite:t}`Whipple2000GSABulletin`).
````

````{tab-item} Shear stress
##### Hypothesis
Conservation of momentum implies that the viscous shear stress is proportional to water depth and slope:
```{math}
\tau_b=\rho g D S=\rho C_fV^2
```
````

````{tab-item} Discharge
##### Hypothesis
Discharge is the product of flow velocity, depth and width of the channel:
```{math}
Q = VDW
```
````

````{tab-item} Channel width
##### Hypothesis
Channel width varies as a power ($b$) of discharge:
```{math}
W=k_wQ^b
```
Commonly observed value for $b$ is 1/2.
````

````{tab-item} Drainage area
##### Hypothesis
Discharge is proportional to drainage area:
```{math}
Q = k_qA^c
```
commonly observed value for $c$ is 1.
````

`````

## Combined equation

Combining all these relationships leads to the following expression for the erosion rate:
```{math}
:label: spl-eps
\dot\epsilon=KA^{2ac(1-b)/3}S^{2a/3}=KA^mS^n
```
and
```{math}
m=2ac(1-b)/3\\
n=2a/3\\
m/n = c(1-b)
```
