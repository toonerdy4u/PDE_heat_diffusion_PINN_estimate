# Physics-Informed Neural Networks (PINNs) for 1D Heat Diffusion

This repository contains my implementations of Physics-Informed Neural Networks (PINNs) for solving and analyzing partial differential equations. The primary model focuses on the **1D heat equation** and demonstrates both forward simulation and **inverse parameter estimation** (learning the thermal diffusivity directly from noisy data). A smaller introductory PINN for a quadratic function is also included.

All code, model implementations, experiments, and analysis in this repository
were written entirely by **Anabel Camarena**.

---

## Project Overview

This project showcases how PINNs combine data and physics by embedding the governing PDE into the neural network loss function. The heat-diffusion PINN enforces:

- Data loss  
- Physics loss:  $T_t = \alpha T_{xx}$
- Initial condition loss  
- Boundary condition loss  

The model is also extended to **learn the diffusivity parameter** $\alpha$, making this an inverse problem.

---

## Results

- Recovered the thermal diffusivity parameter with ~99.8% accuracy
  (learned $\alpha = 0.197777$ vs true $\alpha = 0.2$)

- Reduced prediction error by 99.5% compared to a baseline neural network

- Produced smooth, stable temperature fields, even with noise in the data

These results highlight the advantage of physics-informed training over traditional data-only neural networks.

---

This work was completed as part of my graduate research in Applied Mathematics at UC Irvine under the guidance of Dr. John Lowengrub.
The overall project structure was inspired by example PINN implementations previously shared with me by my advisor.
All code and model development in this repository are my own original work.

If you use or build upon this code in your own work, please cite this repository or credit Anabel Camarena.


