# SCDAA-CW

# Linear Quadratic Regulator (LQR) Monte Carlo Simulations

This project contains a Python implementation of the LQR control problem and performs Monte Carlo simulations to evaluate the performance of explicit and implicit control schemes over various time steps and sample sizes.

## Overview

The LQR problem is a key concept in control theory that involves finding an optimal control policy for a given linear system subject to quadratic costs. This project includes a Python class `LQRSolver` that utilizes NumPy for matrix computations and the scipy `odeint` function to solve Riccati differential equations.

The Monte Carlo simulations are used to check the converging behavior of the control problem's value function to the optimal solution, obtained by solving the Riccati equations.

## Installation

To run the simulations, you will need to install the required Python packages:
pip install torch torchvision
pip install numpy scipy matplotlib

To simulate the LQR problem, create an instance of the LQRSolver class and call the appropriate methods to solve the Riccati equations and perform the Monte Carlo simulation.
# Initialize the solver with system matrices and parameters
lqr_solver = LQRSolver(H, M, C, R, D, T, sigma)