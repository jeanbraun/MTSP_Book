# Diffusion-advection equation

The partial differential equation (PDE) governing the one-dimensional, transient transport of heat by diffusion (conduction) and advection is:
```{math}
:label: heat
\frac{\partial T}{\partial t}-u_0\frac{\partial T}{\partial z}=K\frac{\partial^2T}{\partial z^2}
```
where $T$ is temperature, $u_0$ the velocity at which the material moves with respect to the model boundaries - in our case we will consider that this is an erosion velocity or rate, i.e., $u_0=\dot\epsilon$ in equation {eq}`spl-eps` - $K$ is the thermal diffusivity and $z$ and $t$ are depth and time, respectively.

```{note}
Note that because we are interested in erosion, the velocity of rocks towards the surface is in the opposite direction to that of increasing depth, $z$. This is the reason why the advection term is negative.
```

To this PDE, one must associate two boundary conditions, one at the surface ($z=0$) and one at a depth $L$ that corresponds to the thickness of the layer being eroded towards the surface:
```{math}
:label: heat-bc
T(z=0)=0 \textrm{ and }T(z=L)=T_L
```
In this particular case, it is assumed that the temperature is fixed at $L$, but one could use a constant heat flux boundary condition that would impose a value on the temperature gradient, $dT/dz$, rather than the temperature.

Because it is a transient (evolution) equation, one also needs to impose an initial condition, i.e., a temperature distribution with depth at a reference time ($t=0$ in our case).
```{math}
T(t=0)=T_0(z)
```

The need for boundary and initial conditions arise from the fact that the equation is a *differential* equation meaning that it only informs us on the rate of change (in space or time) of the solution, not on its absolute value. There is therefore a need to *fix* the solution in space and time (or give some reference values for the solution) so that an obsolute value can be derived from the equation.

To define dimensionless numbers, one needs to introduce dimensionless variables. To do so we use the initial and boundary conditions:
```{math}
z'=z/L,\ T'=T/T_L,\ t'=t/\tau
```
Note that we have introduced an arbitrary time scale, $\tau$. We will see later how it can be defined.

If we introduce these dimensionless variables in the equation, we obtain the dimensionless form of the equation:
```{math}
\frac{T_L}{\tau}\frac{\partial T'}{\partial t'}-u_0\frac{T_L}{L}\frac{\partial T'}{\partial z'}=K\frac{T_L}{L^2}\frac{\partial^2T'}{\partial z'^2}
```
or
```{math}
\frac{\partial T'}{\partial t'}-\frac{u_0\tau}{L}\frac{\partial T'}{\partial z'}=\frac{K\tau}{L^2}\frac{\partial^2T'}{\partial z'^2}
```
Here we see that two choices are available for $\tau$ that would simplify this expression even more. We can use $\tau=L/u_0$, which would lead to:
```{math}
\frac{\partial T'}{\partial t'}-\frac{\partial T'}{\partial z'}=\frac{K}{Lu_0}\frac{\partial^2T'}{\partial z'^2}
```
or use $\tau=L^2/K$, which would lead to:
```{math}
\frac{\partial T'}{\partial t'}+\frac{Lu_0}{K}\frac{\partial T'}{\partial z'}=\frac{\partial^2T'}{\partial z'^2}
```
In both cases we see appear the ratio $Lu_0/K$. This is the dimensionless number, called the Péclet number ($\mathbf{Pe}$) defined as:
```{math}
\mathbf{Pe}=\frac{Lu_0}{K}
```
which leads to the following dimensionless form of the equation:
```{math}
:label: heat-nodim
\frac{\partial T'}{\partial t'}-\mathbf{Pe}\frac{\partial T'}{\partial z'}=\frac{\partial^2T'}{\partial z'^2}
```

Note that the Péclet number can also be regarded as the ratio of two time scales:
```{math}
\mathbf{Pe}=\frac{Lu_0}{K}=\frac{\tau_c}{\tau_a}
```
with
```{math}
\tau_c=\frac{L^2}{K}
```
the conductive (or diffusion) time scale and
```{math}
\tau_a=\frac{L}{u_0}
```
the advection time scale.

We see that the value of the Péclet number determines the behaviour of this solution. If $\mathbf{Pe}<<1$, the second term of the equation becomes negligible; advection does not contribute to the transport of heat. Conversely, if $\mathbf{Pe}>>1$, advection dominates.

To further illustrate the use of this dimensionless number, I will now derive the steady-state solution to the above equation and demonstrate how it can be expressed in terms of a single parameter, namely, the Péclet number.