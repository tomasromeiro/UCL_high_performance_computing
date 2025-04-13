# Techniques of High-Performance Computing (Computational Finance MSc at UCL)
**Author**: [Tomás Romeiro]

## Overview
This repository contains a the Jupyter notebook — `final_notebook.ipynb` — that presents a numerical solution of the two-dimensional heat equation (a classic partial differential equation) on a square domain \([-1,1]\times[-1,1]\). The primary aim of this assignment is to determine the time \(t^*\) at which the temperature at the center of the plate (\(x=0, y=0\)) reaches \(u=1\), given a specific initial/boundary condition setup. We use both **explicit** and **implicit** finite difference schemes, explore their stability, and compare our numerical results against a known analytic value \(t^* = 0.424011387033\).

This work was completed as part of the **Techniques of High-Performance Computing** course in the Computational Finance MSc at University College London (UCL). The goal of sharing this project is to showcase proficiency in:
1. **High-Performance Computing (HPC)** techniques for partial differential equations (PDEs),
2. **Numerical methods** for time-stepping (explicit vs. implicit),
3. **Code optimization**, such as vectorization or parallelization in Python, 
4. Use of **GPU acceleration**,

## Problem Statement
We consider a square plate \([-1,1]\times[-1,1]\). Initially (at \(t=0\)), one side of the plate is heated to \(u=5\), while all other sides are kept at \(u=0\). As time progresses, the heat diffuses throughout the plate according to the two-dimensional heat equation:
\[
\frac{\partial u}{\partial t} = \nabla^2 u.
\]
We are interested in the time \(t^*\) at which the temperature at the plate’s center \((0,0)\) first reaches \(u=1\).

### Key Tasks
1. **Finite Difference Schemes**:  
   - Implement both **explicit** (forward Euler) and **implicit** (backward Euler or Crank-Nicolson) time-stepping methods.
   - Investigate stability criteria and compare how each scheme behaves with finer and coarser discretizations.

2. **Convergence and Error Analysis**:  
   - Demonstrate how increasing the number of grid points in space refines the accuracy of \(t^*\).
   - Compare the numerical \(t^*\) with the known “true” solution \(t^* \approx 0.424011387033\).
   - Plot and analyze the convergence behavior, illustrating how many correct digits are obtained.

3. **GPU Implementation  **:
   - Porting the explicit scheme to run on GPU(s).
