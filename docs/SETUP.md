# Setup guide

This guide covers the initial setup of the MATLAB/Simulink project in this
repository. Read the [repository README](../README.md) and the
[challenge rules](../MathWorks_SAE_Aero_Design_Simulation_Challenge_27.pdf)
before beginning work.

## Requirements

The current project documentation lists:

- MATLAB R2056b
- Simulink
- Aerospace Blockset
- Aerospace Toolbox
- UAV Toolbox
- Simulink 3D Animation

## Open the project

1. Clone or download this repository.
2. Start 
3. Open `simulation/RC_Demo.prj`.
4. Confirm that MATLAB has added the `simulation/` directory as the project
   root.
5. Check the MATLAB release and installed products before running a model.

Do not move `RC_Demo.prj` or separate it from `Core/`, `Simulation/`, and
`Support/`. The project relies on this directory structure.

## Configure aircraft data

Choose one of the setup workflows in `simulation/SETUP/`:

- `setupData_Excel_Template.mlx` for manually prepared or experimentally
  derived data.
- `setupData_DATCOM.mlx` for DIGITAL DATCOM aerodynamic coefficients and
  Excel propulsion data.

Use the provided templates in `simulation/Template/` where applicable. Before
running the setup, collect and document:

- Geometry and reference dimensions
- Mass, center of gravity, and inertia
- Aerodynamic coefficients and stability derivatives
- Motor, propeller, battery, and propulsion data
- Control-surface limits and actuator assumptions

For every important value, record its units, source, revision or date,
confidence, coordinate system, and sign convention. Label estimates clearly
and replace them with better CAD, analytical, supplier, bench-test, or flight
data as the design matures.

Run setup sections from top to bottom. Review import messages, warnings, units,
and dimensions before opening the simulation.

## Validate and calibrate

1. Run the available design validation.
2. Connect the RC transmitter, joystick, or flying-stick input device.
3. Open the calibration workflow from the MATLAB project shortcuts.
4. Map channels and verify channel directions, neutral values, limits, servo
   travel, throttle mapping, and actuator dynamics.
5. Save the calibration configuration.
6. Run the calibrated-output test and confirm every actuator response.

The challenge requires manual control with calibrated RC commands recorded
before actuator dynamics. Do not use an autopilot or scripted control inputs
for scored missions.

## Run a simulation

1. Launch the simulation through the MATLAB project shortcut.
2. Load the tested calibrated pilot input.
3. Select Sea Level Standard or the applicable competition-site environment.
4. Select a visualization option as needed.
5. Enable flight-parameter plots when the scopes are required.
6. Run the model and fly manually.
7. Review the `out` variable and Simulation Data Inspector.
8. Preserve the selected flight-data file and command recording.

For a competition baseline, run a 240-second mission in each required
environment. Record the simulation release, team commit, aircraft-data
revision, environment, controller calibration, duration, and test objective.

## Change boundaries

Do not casually edit the Environment subsystem, the Calibrated Fixed-Wing
input subsystem, or their supporting functions. Aircraft parameters, data,
the internal Aircraft Dynamics architecture, and visualization may be
changed when the required interfaces are retained and the changes are
technically justified.

## Troubleshooting

- If setup data does not import, check units, dimensions, file paths, and
  coordinate/sign conventions first.
- If actuator responses are reversed or offset, repeat calibration and the
  calibrated-output test before flying.
- If the project cannot find files, reopen `simulation/RC_Demo.prj` and
  confirm that MATLAB is using `simulation/` as the project root.
- If a toolbox or release is missing, resolve the MATLAB installation
  requirement before modifying project files.

Document unresolved setup problems in [TODO](TODO.md).
