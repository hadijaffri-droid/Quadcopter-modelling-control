# Quadcopter Modelling & Control

Full 6-DOF nonlinear quadcopter simulation and control 
designed in MATLAB/Simulink from first principles.

## What's included
- 12-state nonlinear plant (Newton-Euler dynamics)
- Cascaded PID controller (altitude, attitude, position)
- 2D flight animation

## Key concepts
- Newton-Euler equations of motion
- Rotation matrices, Euler angles
- Motor thrust and drag torque modelling
- Cascaded PID architecture
- State-space linearisation around hover

## Results
![euler-angles](https://github.com/user-attachments/assets/de48c3a6-cf2d-4a19-a5c9-4c8a5d774413)
![coordinates](https://github.com/user-attachments/assets/6411aa16-34f8-4f08-9900-4e4cadacc8bf)

## Tuning Methodology
The controllers are tuned sequentially. When tuning a specific PID, all other references are set to zero except for Altitude (z_ref), which remains at the operating setpoint (e.g., 5m) to keep the quadcopter airborne.

## Disclaimer on Performance and simulation results
Note on Visuals: The simulation plots shown below reflect a moderate tuning configuration. These were chosen for the README to clearly demonstrate the system's behavior without excessive noise.

However, the parameters currently set in the controller subsystem  are tuned more aggressively (higher gains) for tighter control. This makes the system "stiffer," which increases the computational load on the ODE solver. Depending on your PC hardware, you may notice longer simulation times. If performance is an issue, consider relaxing the gains to match the moderate settings used in the examples.

```
GitHub: github.com/hadijaffri-droid/Quadcopter-Modelling-Control
