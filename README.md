# 3D Richards Equation Simulation using FEniCSx
## Author: Souvik Roy, Roshan M. D'souza

This repository simulates unsaturated water flow through soil using the **3D Richards Equation** in its moisture content form. The numerical solution is implemented in [FEniCSx](https://fenicsproject.org/), leveraging **Picard iteration** for stability and convergence. Moisture distribution is visualized dynamically via PyVista and Matplotlib.

---

## 🔍 Features

- 3D simulation on a hexahedral mesh
- Soil moisture modeled using **Van Genuchten** parameters
- Picard iteration for nonlinear solver
- Boundary conditions:
  - Random head values on the top surface (Dirichlet)
  - Constant head on side and bottom surfaces
- 1-hour timestep for 100 timesteps
- Interpolation from unstructured mesh to regular grid (for post-processing)
- 2D slice visualization of moisture content at fixed depths
- Animated moisture evolution over time (`Richards.gif`)

---

## 🧪 Numerical Details

- **Richards Equation (Moisture Form)**  
  Nonlinear parabolic PDE solved using Picard iterations.

- **Discretization**
  - Time: Implicit Euler (1-hour step)
  - Space: Continuous Galerkin (CG1 elements)

- **Soil Parameters (Van Genuchten)**
  - $\theta_s = 0.41$
  - $\theta_r = 0.065$
  - $\alpha = 0.075$
  - $n = 1.89$
  - $K_s = 4.42$

---

## 🧰 Dependencies

- FEniCSx
- NumPy
- Scipy
- Matplotlib
- PyVista
- PETSc + mpi4py
- UFL

## Acknowledgements
Authors are not responsible for succesfull execution of the code as proper installation of the necessary libraries are essential for running the codes, and there might be some version changes over time.
