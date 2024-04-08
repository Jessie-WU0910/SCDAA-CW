# SCDAA-CW
Student Name and Student Number: `[JIEYI WU s2013144]`, `[YISHAN DING s2502386]`, `[YANAN ZENG s2500831]` Adjust the contribution percentages as per your group's agreement: [ 1/3, 1/3, 1/3]

# Stochastic Control and Deep Learning Methods Coursework

This repository contains the Python code developed for the Stochastic Control and Deep Learning Methods Coursework for the academic year 2023-24. The coursework involves the implementation of a numerical algorithm for solving stochastic control problems using policy iteration combined with the "deep Galerkin method" for solving linear PDEs.

## Coursework Overview

The coursework is divided into several exercises, each contributing to building the final algorithm. These include:

1. **Linear Quadratic Regulator (LQR) Problem**: Solving the LQR problem in 2 spatial and 2 control dimensions.
2. **Supervised Learning**: Training neural networks for optimal Markovian control and value functions.
3. **Deep Galerkin Method**: Implementing the method for solving a linear PDE.
4. **Policy Iteration**: Combining the above methods to implement policy iteration for stochastic control.

## Prerequisites

The code is developed using Python, and the following libraries are required:
- numpy
- scipy
- matplotlib
- torch

Please ensure that you have a recent version of Python installed on your system along with the above libraries.

## Running the Code

To reproduce the results and figures reported in the accompanying PDF submission, follow the steps outlined below for each exercise:

### Exercise 1.1: Solving LQR using the Ricatti ODE

1. Initialize the `LQRSolver` class with the matrices specifying the LQR problem.
2. Use the `solve_riccati` method to solve the associated Ricatti ODE on a given time grid.
3. Call the `compute_value_function` method to obtain the control problem value for each batch.
4. Run `compute_control_function` to get the Markov control function for each batch.

# Initialize LQRSolver with the specified matrices
lqr_solver = LQRSolver(H, M, C, R, D, T, sigma)

# Solve Ricatti ODE
S_sol = lqr_solver.solve_riccati(time_grid)

# Compute value function
values = lqr_solver.compute_value_function(t_batch, x_batch)

# Compute control function
controls = lqr_solver.compute_control_function(t_batch, x_batch)





