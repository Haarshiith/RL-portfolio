# Sensor Fusion – Particle Filter

This folder contains a implementation of a Particle Filter designed for a simulated ball-throwing scenario. The work was developed as part of the course "Reasoning and Decision Making under Uncertainty" (Portfolio Exam 2, Task P2.1) at the Technical University of Applied Sciences Würzburg-Schweinfurt (THWS).


### Overview

This project presents a Particle Filter-based solution to estimate the positions and velocities of **n ≥ 1 balls** in motion. The estimation is performed under conditions of uncertainty, including noisy and incomplete observations. The system demonstrates robust performance even in the presence of sensor dropouts.

### Task Description

The objective is to model a physical environment where multiple balls are launched with unknown initial conditions. Observations of these trajectories are captured intermittently and are subject to measurement noise. The system must:

- Simulate realistic two-dimensional trajectories based on physics (initial velocity, launch angle, and gravity).
- Incorporate Gaussian noise and simulate periods of missing sensor data.
- Use a Particle Filter to accurately infer both position and velocity over time.
- Track multiple indistinguishable balls in a shared observation space.

###  Files

1. `Portfolio 2 - Particle Filter.ipynb` – Jupyter Notebook containing the complete implementation.

You may execute the notebook using Jupyter Lab, Visual Studio Code, or Google Colab.

### Key Features

1. Trajectory Simulation: Realistic modeling using launch angle, speed, and gravitational forces.
2. Noisy Observation Handling: Simulates sensor inaccuracies via Gaussian noise.
3. Particle Filter: Core algorithm including prediction, update, and resampling steps.
4. Robust to Missing Data: Maintains estimates during periods of observation dropout.
5. Multi-Object Tracking: Supports estimation of multiple targets in a single state space.

### Functional Overview

1. Initialization: Randomly initializes the state of multiple balls within a 50×50m 2D area.
2. Observation Generation: Produces noisy measurements at irregular intervals, simulating real-world sensor limitations.
3. Particle Filtering Steps:
   -Prediction: Propagates particle states using physical motion equations.
   -Update: Calculates particle weights based on observation likelihood.
   -Resampling: Draws new particles proportional to their weights.
4. State Estimation: Computes weighted average to infer current position and velocity.

### Prerequisites

1. Python should be installed in your system.
2. The following Python libraries should be installed:
   - Numpy
   - Matplotlib (for visualization)
   - Scikit-Learn
   - scipy.optimize

### Installation

Install the necessary dependencies using the following command:
pip install numpy matplotlib

### Acknowledgement

Grateful appreciation is extended to Prof. Dr. Frank Deinzer for his valuable guidance and enlightening lectures on Reasoning and Decision Making under Uncertainty.






