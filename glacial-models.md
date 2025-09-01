# Ice models

Ice mechanical behaviour is best represented by a non-linear form of [Stokes equation](stokes-section). The main difficulty in solving (or using) this equation arises from the non-linear rheological behaviour of ice that follows a power law (like rocks) with an exponent close to 3. Ice can be considered to be incompressible.

Solving the problem of the flow of ice on a landscape is therefore equivalent to solving Stokes equation on a highly irregular geometry (the basal boundary condition is the bedrock geometry). Note, however, that the mass conservation equation that expresses the incompressibility has been "enriched" with a source term that represents the processus of snow/ice accumulation and ablation. Indeed, the dynamics of a glacier is controlled by climate. In high altitude regions (or in the *accumulation zone*) precipitation leads to accumulation of ice on the glacier. In low altitude region (or in the *ablation zone*), melting and sublimation lead to a loss of ice. The altitude where accumulation and ablation perfectly balance eqch other is called the *Equilibrium Line Altitude* (ELA).

```{figure} images/ice-balance.png
---
height: 300px
name: ice-balance
---
from {cite:t}`siegert2013encyclopedia-771`
```

The shallow ice approximation {cite:p}`knap1996climate-8d6` was the most commonly used approximation to model ice flow and was incorporated in various glacial erosion models {cite:p}`Braun1999`. It is similar to the [thin-sheet](thin-sheet-section) approximation. It was first developed to model ice sheets and is therefore not ideally suited to represent the flow of ice on a high relief, mountaineous topography, as it assumes that horizontal gradients in ice thickness must be small (or on a scale much larger than the ice thickness). This model cannot be used to reproduce details of glacial landscapes such as U-shaoed valleys, unless it includes a constriction factor {cite:p}`Braun1999`.

A higher-order approximation (iSOSIA) has become quite popular {cite:p}`Egholm2011JournalofGeophysicalResearchEarthSurface20032012`. It produces ice velocities that are much more realistic and in phase with the underlying complex topography, and, consequently, the erosion that it predicts through the glacial erosion law {eq}`glacial` produces much more realistic landscape features such as U-shaped valleys, aretes and cirques. However, it is much more computationally demanding and relatively unstable such that it is not well suited to be coupled to tectonic models.

More recently, the use of mahcine learning methods to solve Stokes equation have greatly sped up the computation of ice geometry {cite:p}`cordonnier2023forming-d23` and most of the current simulations are now performed using this new technique.
