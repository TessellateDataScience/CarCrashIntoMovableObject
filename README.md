# Car impacting an unconstrained object
Finite Element Method modelling of a smaller vehicle that (front) impacts a heavy object. Modelling was partially developed by Tessellate Data Science using [OpenRadioss](https://github.com/OpenRadioss/OpenRadioss). The car sub-model was developed by Center for Collision Safety and Analysis (CCSA) researchers at George Mason University (more information can be found on [CCSA's website](https://www.ccsa.gmu.edu/models/2010-toyota-yaris/)).

## Object's acceleration
The object was modelled as an movable object and not a fixed barrier. As a result of the object's lack of constraining to the ground it was accelerated during the collision, as such the acceleration components were monitored in orthogonal directions. Below are these accelerations, where the mass of the object was varied (essentially changing it's density) between 100 to 500 [kg]. 

<img src="https://github.com/TessellateDataScience/CarCrashIntoMovableObject/blob/main/plot_mX_accNorm_pBack.png" alt="acceleration versus object's mass">
