# DyNeRF_nODE
<!-- Check-->

We tackle the problem of 4D reconstruction and modeling of the underlying dynamics of a scene. We design a novel setup using NeRF and neural ODE. The NeRF learns the spatial information of a scene and the nODE learns the temporal information and the dynamics of the scene. Our setup can not only reconstruct the original scene, but 
* Extrapolates beyond the scene trajectory
* Generalizes across different physical parameters (friction) of the scene
* Generalizes across different initial condition (position, velocity) of the scene

We curate three deterministic scenes with different number of stable points for our experiments.
* **Scene1:** Pendulum (1 stable point)
* **Scene2:** Ball in a bowl (1 stable point)
* **Scene3:** Ball in a hill (2 stable points)

## Single Trajectory Reconstruction + Extrapolation


<!-- Single Trajectory Pendulum -->
<!--<div style="display: flex; justify-content: space-between;">
  <figure style="text-align: center;">
    <img src="https://github.com/user-attachments/assets/02d828f4-222c-46a5-948f-9f3809833e6f" alt="train_pendulum" width="300" />
    <figcaption style="font-size: 14px; margin-top: 5px;">Training Video</figcaption>
  </figure>

  <figure style="text-align: center;">
    <img src="https://github.com/user-attachments/assets/9c42bdb2-b872-43e9-8e70-9095cbf4aa91" alt="Pendulum_extrapolation" width="300" />
    <figcaption style="font-size: 14px; margin-top: 5px;">Reconstruction + Extrapolation</figcaption>
  </figure>
</div>-->

We train the our model on a posed monocular video of a deterministic scene. Our model not only reconstructs the scene, but also extrapolates beyond the seen trajectory.

### Scene 1
<!-- Single Trajectory Pendulum -->
<div style="display: flex; justify-content: space-between;">
  <figure style="text-align: center;">
    <img src="https://github.com/user-attachments/assets/02d828f4-222c-46a5-948f-9f3809833e6f" alt="train_pendulum" width="300" />
  </figure>

  <figure style="text-align: center;">
    <img src="https://github.com/user-attachments/assets/9c42bdb2-b872-43e9-8e70-9095cbf4aa91" alt="Pendulum_extrapolation" width="300" />
  </figure>
</div>

> **Left:** Input Video  &ensp;  **Right:** Reconstructed + Extrapolated Video

### Scene 2
<!-- Single Trajectory Ball Bowl -->
<div style="display: flex; justify-content: space-between;">
  <figure style="text-align: center;">
    <img src="https://github.com/user-attachments/assets/98877aca-ddda-4c66-95bc-7fa97264cbbe" alt="train_pendulum" width="300" />
  </figure>

  <figure style="text-align: center;">
    <img src="https://github.com/user-attachments/assets/92ffb4b5-30c9-4940-8123-3cb418829ea0" alt="Pendulum_extrapolation" width="300" />
  </figure>
</div>

> **Left:** Input Video  &ensp;  **Right:** Reconstructed + Extrapolated Video


## Generalizing across different physical parameters

We train our model on a few trajectories with varying values of the physical parameters (damping, friction) of the scene, while keeping the initial conditions the same. Our model successfully generalizes to unseen values of the physical parameters and generates novel trajectories.

### Scene 1

<!-- Friction Pendulum -->

<div style="display: flex; justify-content: space-between;">
  <figure style="text-align: center;">
    <img src="https://github.com/user-attachments/assets/4f4ecbca-cffd-4e5c-b8ee-04bc6d5a4cfc" alt="train_pendulum" width="300" />
  </figure>

  <figure style="text-align: center;">
    <img src="https://github.com/user-attachments/assets/9c23ad9b-ebcd-4e47-aacc-2eea64c26cd0" alt="Pendulum_extrapolation" width="300" />
  </figure>
</div>

> Novel generations on unseen damping factors. . **Left:** 0.2 damping factor  &ensp;  **Right:** 0.35 damping factor

### Scene 2
<!-- Friction Ball Bowl -->


<div style="display: flex; justify-content: space-between;">
  <figure style="text-align: center;">
    <img src="https://github.com/user-attachments/assets/c0900048-a163-43fc-bcf2-4537c482cb0e" alt="train_pendulum" width="250" />
  </figure>

  <figure style="text-align: center;">
    <img src="https://github.com/user-attachments/assets/b103b483-e507-499b-8b3b-66649fdfa0a1" alt="Pendulum_extrapolation" width="250" />
  </figure>

  <figure style="text-align: center;">
    <img src="https://github.com/user-attachments/assets/2c5e3dbc-635e-4466-987b-ee4f4b1d94ff" alt="Pendulum_extrapolation" width="250" />
  </figure>
</div>

> Novel generations on unseen friction values.  **Left:** 0.03 &ensp; **Centre:** 0.25  &ensp;  **Right:** 0.35

## Generalizing across different initial conditions

We train our model on a few trajectories with different initial conditions. Our model successfully generalizes to unseen initial conditions and generates novel trajectories.

### Scene 1
<!-- Generalization Pendulum -->

<div style="display: flex; justify-content: space-between;">
  <figure style="text-align: center;">
    <img src="https://github.com/user-attachments/assets/e6a131e0-cb89-4c78-9b27-1c39255603cb" alt="train_pendulum" width="400" />
  </figure>

  <figure style="text-align: center;">
    <img src="https://github.com/user-attachments/assets/f4229da1-d9ad-4bf3-9bbf-1d5c977b2b58" alt="Pendulum_extrapolation" width="400" />
  </figure>

  <figure style="text-align: center;">
    <img src="https://github.com/user-attachments/assets/3a7eb048-db39-438b-a821-4bdab341d6da" alt="Pendulum_extrapolation" width="400" />
  </figure>

  <figure style="text-align: center;">
    <img src="https://github.com/user-attachments/assets/1cae5872-6c38-4f09-9dfc-a53d64fb79ba" alt="Pendulum_extrapolation" width="400" />
  </figure>

</div>

> Novel generations from unseen starting angles. **Top Left:** -0.03 radians &ensp; **Top Right** 0.4 radians  &ensp;  **Bottom Left:** -0.7 radians &ensp; **Bottom Right:** 0.7 radians

 ### Scene 2
<!-- Generalization Ball Bowl -->

<div style="display: flex; justify-content: space-between;">
  <figure style="text-align: center;">
    <img src="https://github.com/user-attachments/assets/d0ffcae2-2dc9-41aa-9940-bde890678a19" alt="train_pendulum" width="400" />
  </figure>

  <figure style="text-align: center;">
    <img src="https://github.com/user-attachments/assets/31c83acf-474a-4ad8-8684-91997beb4b08" alt="Pendulum_extrapolation" width="400" />
  </figure>

  <figure style="text-align: center;">
    <img src="https://github.com/user-attachments/assets/89a48b85-8d19-4ad4-b1c6-cbbc3498e284" alt="Pendulum_extrapolation" width="400" />
  </figure>

  <figure style="text-align: center;">
    <img src="https://github.com/user-attachments/assets/f1d07ff0-93b6-4185-a0b1-d7698d702db7" alt="Pendulum_extrapolation" width="400" />
  </figure>
</div>

> Novel generations from unseen starting points

### Scene 3
<!-- Generalization Ball Hill -->

<div style="display: flex; justify-content: space-between;">
  <figure style="text-align: center;">
    <img src="https://github.com/user-attachments/assets/9c78ee3d-2e38-452c-8ad9-1e0dee779340" alt="train_pendulum" width="400" />
  </figure>

  <figure style="text-align: center;">
    <img src="https://github.com/user-attachments/assets/19ea6877-1383-4503-95ef-0402ed5e1174" alt="Pendulum_extrapolation" width="400" />
  </figure>
</div>

> Novel generations from unseen starting points


### Divergence Plots
<!-- Divergence Plots -->
<div style="display: flex; justify-content: space-between;">
  <figure style="text-align: center;">
    <img src="https://github.com/user-attachments/assets/bbc21273-74f4-47ad-84f2-7beb647a7d1e" alt="train_pendulum" width="400" />
  </figure>
  <figure style="text-align: center;">
    <img src="https://github.com/user-attachments/assets/9c8dd8d5-609f-4cf5-94c2-b96460726832" alt="train_pendulum" width="400" />
  </figure>
</div>

> **Left:** Divergence Plot of Scene 2. The sink represents the stable point in the nODE where the ball in the bowl comes to rest
> 
> **Right:** Latent and Divergence Plot of Scene 3. The two sinks represent the two stable points in the nODE corresponding to the two troughs, where the ball rolls down and comes to rest. The latent plot on top of it corresponds to the trajectories of the ball. We see a bifurcation point (which represents the position near the top of the hill), from where the latents move towards either sinks.


