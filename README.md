# Car impacting an unconstrained object
Finite Element Method modelling of a smaller vehicle that (front) impacts a heavy object. Modelling was partially developed by Tessellate Data Science using [OpenRadioss](https://github.com/OpenRadioss/OpenRadioss). The car sub-model was developed by Center for Collision Safety and Analysis (CCSA) researchers at George Mason University (more information can be found on [CCSA's website](https://www.ccsa.gmu.edu/models/2010-toyota-yaris/)).

## Object's acceleration
The object was modelled as an movable object and not a fixed barrier. As a result of the object's lack of constraining to the ground it was accelerated during the collision. As such the acceleration components (in orthogonal directions) were monitored, shown directly below. 

<p align="center">
<img src="https://github.com/TessellateDataScience/CarCrashIntoMovableObject/blob/main/plot_m500_accNorm_XYZ.jpg" alt="acceleration over time">
</p>

Overall, the car's forward-facing direction acceleration is significantly higher. In this direction, the acceleration initially increases, followed by a highly-transient peak, and then decreases more gradually than the initial rise. A secondary peak also appears at the onset of acceleration.
