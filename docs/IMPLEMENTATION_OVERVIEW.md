# Implementation Overview

## Purpose

The MATLAB project evaluates a Lyapunov-based Bank-to-Turn proportional-navigation formulation in a three-dimensional point-mass simulation. The implementation compares the BTT method with classical proportional navigation followed by polar conversion and then examines sensitivity to modeled uncertainty.

## Simulation workflow

1. Define the initial relative geometry, vehicle velocities, seeker dynamics, and first-order pitch and roll response parameters.
2. Propagate the target and interceptor states using a fixed-step numerical integration loop.
3. Record relative motion, guidance commands, simulated responses, trajectory histories, and the Lyapunov-function history.
4. Determine the minimum recorded three-dimensional separation and the numerical engagement-termination time.
5. Repeat the simulation for deterministic sensitivity sweeps and randomized Monte Carlo trials.
6. Post-process the stored outputs into trajectory plots, response histories, empirical distributions, percentiles, and input-output scatter plots.

## MATLAB project structure

| Component | Role |
|---|---|
| Nominal comparison | Compares the BTT formulation with classical PNG and polar conversion under one baseline engagement. |
| Seeker-noise study | Sweeps the assumed line-of-sight measurement-noise level and compares the response histories. |
| Autopilot-lag study | Varies the modeled pitch and roll response time constants together. |
| Lateral-disturbance study | Examines sensitivity to the simplified constant lateral wind-drift representation. |
| Monte Carlo campaign | Randomizes multiple modeled inputs simultaneously across 1,000 trials and computes empirical statistics. |
| Live 3D visualization | Animates the target and the two simulated trajectory histories in an altitude-up display. |

## Coordinate convention

The analytical and numerical model uses a downward-positive Z convention. The visualization reverses only the displayed vertical coordinate so that altitude appears positive upward. This display transformation does not change the internal equations of motion.

## Model boundaries

- Three-dimensional point-mass kinematics rather than a full rigid-body 6-DOF model
- First-order seeker and autopilot response models
- Fixed-step Euler integration
- Prescribed target maneuver profile
- Simplified constant lateral velocity disturbance rather than a full aerodynamic wind model
- Numerical stopping condition used to define engagement termination

These assumptions are essential when interpreting the reported results.

## Eden Gadban's portfolio contribution

The public portfolio highlights Eden Gadban's work on the MATLAB implementation, coordinate-convention correction and verification, nominal comparison, deterministic sensitivity studies, Monte Carlo analysis, 3D visualization, interpretation of results, and technical reporting.

## Source availability

This public repository presents the methodology, report, results, and visualization. The complete executable academic guidance-law source is retained in the original course archive and is not distributed through this public portfolio repository.
