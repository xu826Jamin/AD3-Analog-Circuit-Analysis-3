# AD3-Analog-Circuit-Analysis-3
## Part 3: Second-Order RLC Transient Response
**Course:** ELEC ENG 2CI4 - Homework 3
**Objective:** Analyze the transition from overdamped to underdamped states in RLC networks.

### 1. Mathematical Modeling of RLC Systems
- **System ODE**: Derived the second-order homogeneous differential equation:
  $$\frac{d^{2}i(t)}{dt^{2}} + \frac{R}{L}\frac{di(t)}{dt} + \frac{1}{CL}i(t) = 0$$
- **Damping Ratio ($\zeta$)**: Quantified the system's stability using the ratio $\zeta = \frac{R}{2}\sqrt{\frac{C}{L}}$.

### 2. Comparative Analysis of Damping States
| State | Resistance ($R$) | Damping Ratio ($\zeta$) | Observation |
| :--- | :--- | :--- | :--- |
| **Overdamped** | $3\text{ k}\Omega$ | $3.873$ | Smooth rise to steady-state; no oscillation. |
| **Underdamped** | $100\text{ }\Omega$ | $0.129$ | Oscillatory decay stabilizing at steady-state. |
| **Critically Damped**| $774.6\text{ }\Omega$ | $1.000$ | Fastest response without overshoot. |


### 3. Hardware vs. Simulation (Parasitic Effects)
- **Inductor DCR**: Accounted for the 5-10 $\Omega$ DC Resistance of the 1.5 mH inductor.
- **Precision Tuning**: Implemented a series chain ($330\Omega + 220\Omega + 220\Omega$) to approximate critical resistance within $0.7\%$ of the theoretical value.
- **Result**: Proved that total circuit resistance (including breadboard contact) shifts the damping ratio higher, resulting in slightly more "sluggish" behavior in hardware compared to mathematical PSpice models.
