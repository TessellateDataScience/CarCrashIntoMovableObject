# Car impacting an unconstrained object
Finite Element Method modelling of a smaller vehicle that (front) impacts a heavy object. Modelling was partially developed by Tessellate Data Science using [OpenRadioss](https://github.com/OpenRadioss/OpenRadioss). The car sub-model was developed by Center for Collision Safety and Analysis (CCSA) researchers at George Mason University (more information can be found on [CCSA's website](https://www.ccsa.gmu.edu/models/2010-toyota-yaris/)).

## Object's acceleration
The object was modelled as an movable object that could represent a boulder that has fallen onto the road. As the object lacked constraining to the ground it could possibly be accelerated when a car hit it (as opposed to a fixed barrier that would have zero acceleration). Due to this the acceleration's individual components, in orthogonal directions, were monitored (found directly below). 

<p align="center">
<img src="https://github.com/TessellateDataScience/CarCrashIntoMovableObject/blob/main/plot_m500_accNorm_XYZ.jpg" alt="acceleration over time">
</p>

Overall, the car's forward-facing direction acceleration is significantly higher. In this direction, the acceleration initially increases, followed by a highly-transient peak, and then decreases more gradually than the initial rise. A secondary peak also appears at the onset of acceleration.

### Acceleration of varying object masses
We then ran further computational investigations where the object's mass was varied. Below are more general metrics (where we quantified the acceleration's more exactly) for masses between 100 to 600 kilograms.

<p align="center">
  <img src="https://github.com/TessellateDataScience/CarCrashIntoMovableObject/blob/main/plot_accVsMass.jpg" alt="acceleration versus object's mass">
</p>

Generally the maximum acceleration of the object obtained during the collision appeared stochastic, with no clear dependence on the object's mass. Conversely the integral of the acceleration (over the entire collision duration) showed a decreasing linear trend for increasing masses (which is expected as from Newton's 2nd Law).
