# DyNeRF_nODE

We tackle the problem of reconstruction and modeling of the underlying dynamics of a scene. We design a novel setup using NeRF and neural ODE. The NeRF learns the spatial information of a scene and the nODE learns the various dynamics in the scene. Our setup can not only reconstruct the original scene, but 
* Extrapolates beyond the scene trajectory
* Generalizes across different physical parameters (friction) of the scene
* Generalizes across different initial condition (position, velocity) of the scene

## Reconstruction + Extrapolation


<div style="display: flex; justify-content: space-between;">
  <figure style="text-align: center;">
    <img src="https://github.com/user-attachments/assets/02d828f4-222c-46a5-948f-9f3809833e6f" alt="train_pendulum" width="300" />
    <figcaption style="font-size: 14px; margin-top: 5px;">Training Video</figcaption>
  </figure>

  <figure style="text-align: center;">
    <img src="https://github.com/user-attachments/assets/9c42bdb2-b872-43e9-8e70-9095cbf4aa91" alt="Pendulum_extrapolation" width="300" />
    <figcaption style="font-size: 14px; margin-top: 5px;">Reconstruction + Extrapolation</figcaption>
  </figure>
</div>




## Generalizing across different friction values




## Generalizing across different initial conditions
