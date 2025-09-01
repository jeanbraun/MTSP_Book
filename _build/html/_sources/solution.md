# Steady-state solution

The steady-state form of the heat diffusion-advection equation is obtained by setting the transient term to 0 in the dimensionless equation{eq}`heat-nodim`:
```{math}
-\mathbf{Pe}\frac{\partial T'}{\partial z'}=\frac{\partial^2T'}{\partial z'^2}
```
This equation has the following general solution:
```{math}
T'=C_1e^{-\mathbf{Pe}z'}+C_2
```
We can use the boundary conditions from equation {eq}`heat-bc` to determine the values of the two arbitrary constants, $C_1$ and $C_2$, to obtain:
```{math}
T'(z')=\frac{1-e^{-\mathbf{Pe}z'}}{1-e^{-\mathbf{Pe}}}
```
