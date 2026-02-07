# LTI-System-Control-MATLAB
# LTI System Analysis and Optimal Control Design (LQR/LQG/LTR)

## Project Overview
[cite_start]This repository contains the full analysis and control design for a Linear Time-Invariant (LTI) SISO system, developed as part of the **Multivariable Feedback Control** course at the University of Campania "Luigi Vanvitelli"[cite: 1, 6]. 

[cite_start]The project covers the entire workflow of a control engineer: from mathematical modeling and structural analysis to the implementation of advanced optimal control strategies using **MATLAB**[cite: 2, 8].

**Student:** Gaetano Improta  
[cite_start]**Academic Year:** 2025/2026 [cite: 3, 4]  
[cite_start]**Professor:** Alberto Cavallo [cite: 6]

---

## 1. System Modeling
[cite_start]The study focuses on a second-order dynamical system represented in state-space form[cite: 11, 12]:

$$
\begin{cases}
\dot{x}(t) = Ax(t) + Bu(t) \\
y(t) = Cx(t) + Du(t)
\end{cases}
$$

[cite_start]With physical parameters $m=10$, $c=0.5$, and $k=2$, resulting in the following transfer function[cite: 14, 18, 59]:
[cite_start]$$G(s) = \frac{0.1}{s^2 + 0.05s + 0.2}$$ [cite: 59]

---

## 2. Structural Analysis
[cite_start]A rigorous analysis of the system's internal properties was performed[cite: 8]:
* [cite_start]**Stability:** Verified through eigenvalue analysis and diagonalizability of the A matrix[cite: 67, 68].
* [cite_start]**Controllability:** Analyzed using the Controllability Matrix, Reachability Gramian, and Lyapunov tests[cite: 63, 89, 118, 194].
* [cite_start]**Observability:** Confirmed via the Observability Matrix and Gramian to ensure the feasibility of state estimation[cite: 387, 402, 426].
* [cite_start]**Advanced Linear Algebra:** Implementation of Singular Value Decomposition (SVD) to study system gain properties[cite: 1258, 1266].

---

## 3. Control & Estimation Strategies
[cite_start]The project implements several control architectures to handle different operational requirements[cite: 8]:

### Classical & State-Space Control
* [cite_start]**Lyapunov-based Control:** Designing a stabilizing control law $u = -Kx$ based on Lyapunov theory[cite: 250, 290].
* [cite_start]**Pole Placement:** Direct assignment of closed-loop poles to meet specific damping and frequency requirements[cite: 332, 344].
* [cite_start]**Luenberger Observer:** Implementation of a state estimator to reconstruct non-measurable states, verified by analyzing the error convergence ($e \rightarrow 0$)[cite: 453, 459, 566].

### Optimal Control Architecture
* [cite_start]**LQR (Linear Quadratic Regulation):** Minimizing a quadratic cost function to find the optimal trade-off between performance and control energy[cite: 854, 859, 863].
* [cite_start]**LQG (Linear Quadratic Gaussian):** Combining LQR with a Kalman Filter to maintain performance in the presence of process and measurement noise[cite: 988, 990].
* [cite_start]**LTR (Loop Transfer Recovery):** Recovering the robustness margins of the LQR design within the LQG framework[cite: 988, 998].



---

## 4. Constraint Analysis
[cite_start]Specific attention was given to fundamental performance limits[cite: 613]:
* [cite_start]**Transmission Zeros:** Analysis of signal-blocking frequencies[cite: 614, 616].
* [cite_start]**RHP Zeros:** Study of the unavoidable bandwidth constraints and phase lag introduced by Right Half-Plane zeros[cite: 659, 660].
* [cite_start]**Roll-off Condition:** Verification of high-frequency attenuation for noise rejection[cite: 803, 804].

---

## 5. Simulation Results
[cite_start]The MATLAB simulations confirm the theoretical findings[cite: 17, 315]:
* [cite_start]**Stability Recovery:** Successfully stabilized an initially unstable system configuration using feedback gains[cite: 251, 315].
* [cite_start]**Estimation Accuracy:** The Luenberger observer shows rapid convergence of the estimated state to the real simulated state[cite: 611].
* [cite_start]**Robustness:** The LQG/LTR controller demonstrates superior performance in recovering ideal robustness margins[cite: 998].

---

## Tools
* **MATLAB**
* **Control System Toolbox**
