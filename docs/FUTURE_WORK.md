# Future Work

The present point-mass simulation is a useful first evaluation of the guidance formulation, but it intentionally simplifies several physical effects. The following extensions would improve fidelity and strengthen the validation process.

## Higher-fidelity dynamic model

Extend the point-mass representation to a general six-degree-of-freedom rigid-body research model with translational and rotational equations of motion, mass properties, aerodynamic forces and moments, and body angular rates. This would allow the interaction between guidance commands, attitude dynamics, and vehicle response to be studied explicitly.

## Physical actuator and sensor constraints

Introduce actuator saturation and rate limits, seeker field-of-view constraints, measurement bias, and sensor bandwidth limitations. These additions would make the simulated control and measurement chains more representative of physical hardware.

## Propulsion and atmosphere

Model thrust variation, fuel consumption, drag, and altitude-dependent atmospheric density. This would replace the constant-speed approximation with an energy-aware flight model.

## Numerical verification and model validation

Perform time-step convergence studies, verify implementation consistency against independent calculations, and compare selected cases with published reference results. Clearly separate code verification from physical validation.

## Quantitative global sensitivity analysis

Complement the existing one-factor-at-a-time sweeps and qualitative Monte Carlo scatter plots with rank correlation, multivariable regression, or variance-based sensitivity methods. This would provide a numerical ranking of uncertain inputs while accounting for simultaneous variation.

## Additional prescribed scenarios

Evaluate a controlled set of distinct initial geometries and maneuver profiles rather than relying only on one prescribed maneuver schedule with randomized parameters. Results should continue to be reported within the assumptions of each modeled scenario.
