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

<div style="display: flex; justify-content: space-between;">
  <figure style="text-align: center;">
    <img src="https://github.com/user-attachments/assets/98877aca-ddda-4c66-95bc-7fa97264cbbe" alt="train_pendulum" width="300" />
    <figcaption style="font-size: 14px; margin-top: 5px;">Training Video</figcaption>
  </figure>

  <figure style="text-align: center;">
    <img src="https://github.com/user-attachments/assets/92ffb4b5-30c9-4940-8123-3cb418829ea0" alt="Pendulum_extrapolation" width="300" />
    <figcaption style="font-size: 14px; margin-top: 5px;">Reconstruction + Extrapolation</figcaption>
  </figure>
</div>




## Generalizing across different friction values

<div style="display: flex; justify-content: space-between;">
  <figure style="text-align: center;">
    <img src="https://github.com/user-attachments/assets/4f4ecbca-cffd-4e5c-b8ee-04bc6d5a4cfc" alt="train_pendulum" width="300" />
  </figure>

  <figure style="text-align: center;">
    <img src="https://github.com/user-attachments/assets/9c23ad9b-ebcd-4e47-aacc-2eea64c26cd0" alt="Pendulum_extrapolation" width="300" />
  </figure>
</div>

<div style="display: flex; justify-content: space-between;">
  <figure style="text-align: center;">
    <img src="https://github.com/user-attachments/assets/c0900048-a163-43fc-bcf2-4537c482cb0e" alt="train_pendulum" width="300" />
  </figure>

  <figure style="text-align: center;">
    <img src="https://github.com/user-attachments/assets/b103b483-e507-499b-8b3b-66649fdfa0a1" alt="Pendulum_extrapolation" width="300" />
  </figure>

  <figure style="text-align: center;">
    <img src="https://github.com/user-attachments/assets/2c5e3dbc-635e-4466-987b-ee4f4b1d94ff" alt="Pendulum_extrapolation" width="300" />
  </figure>
</div>


## Generalizing across different initial conditions
