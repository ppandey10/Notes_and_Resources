# Gauge Conditions

## Spatial Gauge 

We need spatial gauges so as to **minimise spatial distortion**.

### Minimal Distortion Gauge

- Start by defining a *distortion tensor*, which is symmetric
$$Q_{ij} := \dot{\gamma}_{ij} = -2\alpha K + \mathcal{L}_{\beta}\gamma_{ij}$$
  
  and a tracelss tensor:

  $$\Sigma_{ij} = Q_{ij} -\frac{1}{3}Q\gamma_{ij} = -2\alpha A_{ij} + (L\beta)_{ij} := \Psi^4\dot{\tilde{\gamma}}_{ij}$$

- Now, we have to find $\beta$ along with minimisation of some function.

- Proceed further by defining a functional
$$I[\beta^i] = \int \Sigma_{ij}\Sigma^{ij}\sqrt{\gamma}d^3x$$

  and since we wanted a minimisation, we achieve that taking the variation of the functional.
![Alt text](../../../../../../var/folders/ms/qmx19gbx5mb0625j7fcft_wc0000gn/T/TemporaryItems/NSIRD_screencaptureui_UvsIfy/Screenshot%202023-06-13%20at%202.26.07%20PM.png)

- Finally, we get this equation, afte the applying the momentum constraint 
![Alt text](../../../../../../var/folders/ms/qmx19gbx5mb0625j7fcft_wc0000gn/T/TemporaryItems/NSIRD_screencaptureui_sLhdVs/Screenshot%202023-06-13%20at%202.28.42%20PM.png)

- So, the above equation is elliptic in $\beta$. 

- Few properties of this equation:
  1. If $\partial_t = 0$ is a K.V. then $\Sigma_{ij} = 0$
  2. In weak field limit, minimal distortion is a TT gauge. 

- Simpler eqs belong to *gamma freezing* gauge condition.

### Gamma Freezing Condition

- For this we start by working with 
$$ 0 = \mathcal{D}^i\dot{\tilde{\gamma}}_{ij} = \partial_t(\mathcal{D}^i\tilde{\gamma}_{ij})$$
![Alt text](../../../../../../var/folders/ms/qmx19gbx5mb0625j7fcft_wc0000gn/T/TemporaryItems/NSIRD_screencaptureui_0WwCdc/Screenshot%202023-06-13%20at%203.17.49%20PM.png)

- Finally, we get a conformal variable
$$\tilde{\Gamma}^i := -\mathcal{D}_j\tilde{\gamma}^{ij} = (\tilde{\Gamma}^i_{jk} - F^i_{jk})\tilde{\gamma}^{jk}$$
 and 
 $$\boxed{\partial_t\tilde{\Gamma}^i = 0}$$
 
- Also, we get the following equation
![Alt text](../../../../../../var/folders/ms/qmx19gbx5mb0625j7fcft_wc0000gn/T/TemporaryItems/NSIRD_screencaptureui_HBkOUk/Screenshot%202023-06-13%20at%202.48.29%20PM.png)

- Since, the above equation is  elliptic and therefore it becomes difficult to solve. Hence, we convert it into parabolic or hyperbolic equation.

  - *Parabolic gamma driver*
  $$\partial_t\beta^i = k\partial_t\tilde{\Gamma}^i$$
  For this driver, I need boundary as well as initial condition. 
  Normally, the parabolic eqs need to satisfy CFL condition which is necessary for stability
  $$\Delta t \leq c\Delta h^2$$

  - *Hyperbolic gamma driver*
  $$\partial_{tt}\beta^i = k\partial_t\tilde{\Gamma}^i - \eta\partial_t\beta^i$$
  where, $k$ is the final speed of the wave and $\eta$ is the damping factor.
  This approach propogates *much slowly* when compared to the parabolic case. 
  The result not equal to what we observe in other cases, but *similar*.
  Also, the stability condition here are known as the FL condition
  $$\Delta t \leq c\Delta h$$


  
