# Car impacting an unconstrained object
_Finite Element Method modelling of a smaller vehicle that (front) impacts a heavy object._ Acceleration (change of velocity) is of interest as a proxy for potential head trauma during a car crash, with linear rates of ~ 100 times that of gravity implicated as causing concussion of helment-wearing folks in traditional sports. Here we are interested in potential head trauma to car passengers during an accident where a car collides with a heavy object (that could represent a bolder) on the shoulder of the road. 

Research is led by Tessellate Data Science with modelling using [OpenRadioss](https://github.com/OpenRadioss/OpenRadioss). The car sub-model was developed by Center for Collision Safety and Analysis (CCSA) researchers at George Mason University (more information can be found on [CCSA's website](https://www.ccsa.gmu.edu/models/2010-toyota-yaris/)). Numerous sensitivity investigations were run within OpenRadioss, instilling confidence that the modelling approach that our results are derived from is reliable. Currently no validation against real-world (non-computational) investigation's results has been done.  

## Acceleration
Acceleration components in in orthogonal directions were monitored and are visualised directly below. 

<p align="center">
<img src="https://github.com/TessellateDataScience/CarCrashIntoMovableObject/blob/main/plot_m500_accNorm_XYZ.jpg" alt="acceleration over time">
</p>

Overall, the car's forward-facing direction acceleration is significantly higher. In this direction, the acceleration initially increases, followed by a highly-transient peak, and then decreases more gradually than the initial rise. A secondary peak also appears at the onset of acceleration.

### Acceleration for different object masses
We then ran further computational investigations where the object's mass was varied. Below are more general metrics (where we quantified the acceleration's more exactly) for masses between 100 to 600 kilograms.

<p align="center">
  <img src="https://github.com/TessellateDataScience/CarCrashIntoMovableObject/blob/main/plot_accVsMass.jpg" alt="acceleration versus object's mass">
</p>

Generally the maximum acceleration obtained during the collision appeared stochastic, with no clear dependence on the object's mass. Conversely the integral of the acceleration (over the entire collision duration) showed a decreasing linear trend for increasing masses (which is expected as from Newton's 2nd Law).
