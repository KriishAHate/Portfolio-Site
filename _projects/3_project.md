---
layout: page
title: "Inverted Pendulum Control Systems project"
published: true
group: work
permalink: /projects/inverted-pendulum/
img: /assets/img/projects/pendulum.png
importance: 3
tags: [control systems, robotics, MATLAB, simulation, optimization]

---

## Overview

Designed and compared three control strategies (PID, LQR, and MPC) to stabilize an inverted pendulum on a moving cart under external disturbances. This classic control problem has real-world applications in humanoid robotics, self-balancing vehicles, rocket stabilization, and robotic arms.

**Challenge:** Maintain balance at an inherently unstable equilibrium point while responding to unpredictable forces like vibrations, wind gusts, and impulses.

[View Full Project Report (PDF)](/assets/img/projects/controlsystemsproject.pdf){:target="_blank"}

---

## System Modeling

Created a comprehensive mathematical model of the pendulum-cart system:

- **Physical Simulation:** Developed CAD model in SOLIDWORKS and implemented rigid body dynamics in Simscape
- **Mathematical Framework:** Derived nonlinear equations of motion using Newton's laws, then linearized around equilibrium (θ = π) for controller design
- **State-Space Representation:** Enabled modern optimal control techniques with 4-state model (cart position/velocity, pendulum angle/velocity)

**System Parameters:**

| Parameter | Value |
|-----------|-------|
| Cart Mass | 8.44 kg |
| Pendulum Mass | 0.79 kg |
| Pendulum Length | 0.25 m |
| Max Actuator Force | 40 N |
| Disturbance | 10 N sinusoidal impulse (50ms period) |

---

## Three Controller Approaches

| Controller | Design Approach | Key Strengths | Limitations |
|------------|----------------|---------------|-------------|
| **PID (Cascaded)** | Dual-loop: inner loop stabilizes pendulum, outer loop controls cart position | Simplest design, minimal computation | Time-intensive manual tuning, no constraint handling |
| **LQR** | Optimal state feedback minimizing J = ∫(X^T·Q·X + U^T·R·U)dt<br>Gain Matrix: K = [-10.00, -16.79, 228.09, 35.81] | Best overall performance, intuitive weight-based tuning | High actuator effort (38N peak) |
| **MPC** | Predictive optimization over future horizon with Kalman filter-based state estimation | Lowest actuator effort (28N), guaranteed constraint satisfaction | High computational cost (2.45s vs 0.02s for PID) |

---

## Results & Performance Comparison

| Performance Metric | PID | LQR | MPC | Winner |
|-------------------|-----|-----|-----|--------|
| **Settling Time (θ)** | 3.2s | 1.8s | 2.5s | LQR |
| **Settling Time (x)** | 4.1s | 2.3s | 3.2s | LQR |
| **Overshoot (θ)** | 12% | 5% | 8% | LQR |
| **Overshoot (x)** | 8% | 3% | 6% | LQR |
| **Max Actuator Force** | 35N | 38N | 28N | MPC |
| **Computation Time** | 0.02s | 0.15s | 2.45s | PID |

---

## Key Insights

| Controller | Best Use Case |
|------------|---------------|
| **PID** | Simple, resource-constrained applications requiring basic stabilization |
| **LQR** | Real-time control demanding best performance with moderate computational resources |
| **MPC** | Offline systems requiring minimal actuator effort and strict constraint enforcement |

---

## Technical Skills Demonstrated

- **Control Theory:** PID tuning, optimal control (LQR), predictive control (MPC)
- **System Modeling:** Nonlinear dynamics, linearization, state-space representation
- **Simulation:** MATLAB/Simulink, Simscape multibody dynamics, SOLIDWORKS CAD
- **Analysis:** Performance metrics, comparative evaluation, constraint optimization

---

## Future Directions

- Hardware implementation on physical inverted pendulum system
- Hybrid controller combining PID simplicity with MPC robustness
- Adaptive control for time-varying dynamics

---