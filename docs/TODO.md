# TODO

This list tracks work needed to turn the initial repository snapshot into a
reproducible, aircraft-specific simulation and submission package. Update it
as work is completed; link commits, test results, and data revisions where
useful.

## Repository and project baseline

- [ ] Record the MathWorks release/version, source URL, and download date.
- [ ] Confirm the supported MATLAB release and toolbox versions.
- [ ] Create a clean baseline commit or tag for the imported simulation.
- [ ] Confirm that `simulation/RC_Demo.prj` opens successfully on a clean
      MATLAB installation.
- [ ] Document any team-specific changes to the upstream simulation.

## Aircraft data

- [ ] Create the team aircraft-data package and select the active setup
      workflow.
- [ ] Add geometry, reference dimensions, coordinate axes, and datum.
- [ ] Add mass, center of gravity, and inertia properties.
- [ ] Add aerodynamic coefficients and stability/control derivatives over the
      expected operating range.
- [ ] Add propulsion data, including motor, propeller, battery, thrust,
      current, and power assumptions.
- [ ] Document control-channel assignments, directions, limits, and actuator
      dynamics.
- [ ] Label each value as measured, CAD-derived, analytical,
      supplier-provided, Gazebo-derived, or estimated.

## Verification and testing

- [ ] Run aircraft-data import without unexpected warnings, `NaN`, or `Inf`
      values.
- [ ] Run design validation and resolve or document its findings.
- [ ] Calibrate the pilot input device and test every actuator direction.
- [ ] Create a repeatable Sea Level Standard baseline run.
- [ ] Create a repeatable applicable competition-site baseline run.
- [ ] Verify takeoff, circuit altitude, turn timing, landing, rollout, and
      stopping behavior against the official rules.
- [ ] Compare important predictions with independent evidence such as CAD,
      hand calculations, supplier data, bench tests, or physical tests.
- [ ] Save selected flight data and pre-actuator command recordings for both
      required environments.

## Analysis and submission

- [ ] Record design decisions supported by simulation results.
- [ ] Prepare plots, metrics, trade studies, and sensitivity analyses for the
      Engineering Report.
- [ ] Document model assumptions, limitations, and verification evidence.
- [ ] Write the four-page Engineering Report in the format required by the
      [official challenge rules](../MathWorks_SAE_Aero_Design_Simulation_Challenge_27.pdf).
- [ ] Use the MATLAB project submission workflow to prepare the final package.
- [ ] Verify that the final download link works without sign-in or approval.
- [ ] Freeze and archive the final model, data, report, and command recordings.

## Open questions

- [ ] Confirm whether the team will compete in Aero Design East or West.
- [ ] Confirm the aircraft class and the applicable mission limits.
- [ ] Decide where team-owned aircraft, analysis, test, and submission files
      will live as the repository grows.
