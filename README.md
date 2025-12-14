# Numerical Investigation of the Two-Body Problem
Mass Ratio and Eccentricity Effects

---

## Authors
**Madeline Renee Boss**  
**Samhitha Devi Kunadharaju**  
*University of Texas at Austin*  
Course: *CS 323E – Elements of Scientific Computing*

---

## Overview

This project presents a numerical study of the classical Newtonian two-body problem, focusing on how mass ratio and orbital eccentricity influence the resulting orbital dynamics.
The two-body system is reduced to an equivalent one-body problem in the center-of-mass frame and integrated numerically using an adaptive Runge–Kutta (RK45) method via SciPy’s solve_ivp. 
Orbits are simulated for multiple mass ratios and eccentricities, and the individual trajectories of both bodies are reconstructed and visualized.

---

## Included Files

| File | Description |
|------|--------------|
| **`two_body_code.ipynb`** | Jupyter/Colab notebook containing the numerical integration, trajectory reconstruction, and orbit visualizations |
| **`Two_Body_Paper.pdf`** | Full paper describing the physical background, mathematical formulation, numerical methods, and results |
| **`image.png`** | Representative visualization of center-of-mass orbital trajectories |
| **`requirements.txt`** | List of dependencies (NumPy, Matplotlib, SciPy) |

---
## Key Ideas
- The two-body problem can be reduced to a single effective particle moving in a central gravitational potential.
- Eccentricity primarily controls the shape of the orbit (circular → elliptical).
- Mass ratio determines how orbital motion is distributed between the two bodies.
- In high mass-ratio systems, the heavier body remains nearly stationary while the lighter body traces a wide orbit.
- Numerical integration provides a flexible framework for studying gravitational dynamics beyond analytic solutions.

---
## Simulation Parameters
Mass ratios:
1:1, 1:2, 1:4, 1:16

Orbital eccentricities:
0, 0.25, 0.50, 0.75

Reference frame:
Center-of-mass frame

Initial conditions:
Orbits are initialized at pericenter with purely tangential velocity.

Numerical method:
Adaptive Runge–Kutta integration (RK45)

Solver:
scipy.integrate.solve_ivp

Integration interval:
One full orbital period for each configuration

Output:
Reconstructed trajectories of both bodies and orbit visualizations

This results in 16 total simulated orbital configurations.

---
## Results (Summary)
- Increasing eccentricity elongates orbits and increases velocity variation between pericenter and apocenter.
- Increasing mass imbalance causes the heavier body’s motion to localize near the center of mass.
- The equal-mass case exhibits symmetric orbital motion, while extreme mass ratios resemble star–planet systems.
- All simulated orbits close cleanly after one period, indicating numerical stability and conservation behavior.

## How to Run
1. Install the required dependencies
```bash
pip install -r requirements.txt
```
2. Launch the Jupyter notebook:
```bash
jupyter notebook two_body_code.ipynb
```
3. Run all cells to generate the numerical solutions and orbit visualizations.

