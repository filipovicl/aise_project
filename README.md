# aise_project
Leo Filipovic's repository for the AI in the Sciences &amp; Engineering project 2024

The main purpose of the final project in AISE Fall Semester 2024 is to implement machine-learning based methods for solving Partial Differential Equations. 

## Tasks summary

### Task 1 - Training a Fourier Neural Operator to solve the 1D Wave Equation
In this task, I train a FNO based neural network to output solutions of the 1D wave equation.
Neural Operators are a generalization of Deep Neural Networks that learn mappings between function spaces. The model architecture is loosely based on the structure outlined in (*Zongyi Li, Nikola Kovachki, Kamyar Azizzadenesheli, Burigede Liu, Kaushik
Bhattacharya, Andrew Stuart, and Anima Anandkumar. Fourier Neu-
ral Operator for Parametric Partial Differential Equations, May 2021.
arXiv:2010.08895*). The model is able to learn solutions with fixed time interval on various grid resolutions, and performs well on out-of-distribution trajectories, but has significantly higher-relative errors on when an additional time dependency is introduced. 

### Task 2 - PDE-Find: Reconstructing PDEs from data
The objective of this task is to use the regression-based method PDE-FIND (*Samuel H Rudy et al. “Data-driven discovery of partial differential equations”. In: Science
advances 3.4 (2017), e1602614*) to recognize the governing time-dependent PDE of an unknown system by using measurements of the solution.
The implemented model, strongly based on the original version implemented in the aforementioned paper, is able to recognize a variety of systems, including misleading PDEs such as the Korteweg - de Vries equation with two solitons.

### Task 3 - Foundation Model for Phase-Field Dynamics
In the third ask, I attempt to train a foundation model that returns time-dependent trajectories of the Allen-Cahn equation, given different initial conditions.
Unfortunately the model wasn't able to learn the dynamics correctly, and instead overfits either to the initial condition, or rapidly evolves to some incorrect state. 