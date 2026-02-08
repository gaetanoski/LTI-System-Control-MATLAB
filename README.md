# **LTI Dynamic System Analysis and Multivariable Control**
This project features a comprehensive study and control design for a Linear Time-Invariant (LTI) mass-spring-damper system using MATLAB. The work bridges the gap between theoretical state-space analysis and advanced multivariable control techniques, ensuring both mathematical optimality and practical robustness. 
+1

## **Structural Analysis and State Estimation**
The core of the study begins with a rigorous verification of the system's structural properties. Stability, controllability, and observability are assessed through multiple frameworks, including Lyapunov equations, reachability Gramians, and eigenvector tests. To address the practical limitation of unmeasurable states, a Luenberger observer was implemented, successfully demonstrating rapid error convergence between simulated and estimated states. 
+4

## **Advanced Control Strategies: From Pole Placement to LQG/LTR**
The project evolves from basic stabilization via Pole Placement and Lyapunov-based control to high-level optimal control strategies. A significant portion of the work is dedicated to Linear Quadratic Regulation (LQR) for minimizing energy expenditure and Linear Quadratic Gaussian (LQG) control for handling process and measurement noise. A key highlight is the application of the Loop Transfer Recovery (LTR) procedure, which was used to recover the robustness margins of the LQR regulator typically lost when using a Kalman filter. 
+4

## **Design Constraints and Frequency Domain Insights**
Beyond time-domain performance, the analysis explores critical frequency-domain constraints. This includes the study of transmission zeros and the physical limitations imposed by Right Half-Plane (RHP) zeros, which dictate strict bandwidth limits for closed-loop stability. The implementation also verifies Roll-off conditions and sensitivity functions to ensure the system meets modern control engineering standards.
