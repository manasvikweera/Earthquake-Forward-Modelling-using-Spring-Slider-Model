# Earthquake-Forward-Modelling-using-Spring-Slider-Model


**Modeling Earthquake Cycles with Spring-Slider Model**

This repository contains MATLAB code for forward modeling earthquake cycles using a single degree of freedom spring-slider model. The model incorporates empirical rate-and-state friction to simulate the behavior of fault lines during seismic events. The code utilizes the `ode45` solver to solve the differential equations relevant to the spring-slider model with friction.

**Introduction**

The spring-slider model offers a simplified representation of earthquake cycles, depicting the accumulation and release of stress along a fault line. In this model, a block of wood rests on a surface and is connected to a spring. As the spring is gradually stretched, it symbolizes the buildup of strain or stress along the fault. The friction between the block and the surface represents the resistance to slippage. Eventually, when the force exerted by the stretched spring overcomes the frictional resistance, the block suddenly slides, mimicking the release of energy during an earthquake. The subsequent oscillations of the block represent the aftershocks that often follow a major seismic event.

**Differential Equations**

The dynamics of the spring-slider system are governed by the following system of differential equations:

- \( \frac{d\theta}{dt} = \frac{1}{\kappa} - u \cdot v \)
- \( \frac{du}{dt} = v - 1 \)
- \( \frac{dv}{dt} = -\gamma \left( u + \frac{1}{\xi} \right) \left( \mu_{\text{drs}} + \ln(v) + (1 + \epsilon) \ln(\kappa \cdot \theta) \right) \)

Where:
- \( \theta \): position
- \( u \): velocity
- \( v \): acceleration
- \( t \): time
- \( \kappa = \frac{A \cdot V_0}{L} \): constant
- \( \xi = \frac{K_s \cdot L}{A} \): constant
- \( \gamma = \frac{r}{\frac{K_s \cdot M \cdot L}{V_0}} \): constant
- \( \mu_{\text{drs}} = 0.64395 \): constant
- \( \epsilon = \frac{B - A}{A} \): constant

This set of equations describes the motion and behavior of the spring-slider system under the influence of frictional forces.
