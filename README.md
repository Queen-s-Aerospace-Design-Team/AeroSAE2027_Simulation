# AeroSAE2027 Simulation

This repository contains the Queen's Aerospace Design Team's MATLAB and
Simulink work for the **MathWorks SAE Aero Design Simulation Challenge**.
The simulation is intended to become a reproducible, pilot-in-the-loop
digital model of the team's aircraft.

## Documentation

- [Setup guide](docs/SETUP.md) - software requirements, project setup, and
  the recommended workflow for preparing and running the simulation.
- [Challenge rules summary](docs/RULES.md) - the key mission, model, scoring,
  and submission concepts summarized from the official rules PDF.
- [TODO](docs/TODO.md) - work that still needs to be completed.
- [Simulation project README](simulation/README.md) - upstream documentation
  for the MATLAB/Simulink virtual environment.

## Repository layout

```text
.
├── docs/                         # Team-maintained documentation
├── simulation/                   # MATLAB and Simulink project
│   ├── Core/                     # Shared initialization and environment code
│   ├── SETUP/                    # Aircraft-data setup workflows
│   ├── Simulation/               # Main simulation models
│   ├── Support/                  # Imports, calibration, scoring, and startup
│   ├── Template/                 # Aircraft-data templates
│   └── RC_Demo.prj               # MATLAB project entry point
├── MathWorks_SAE_Aero_...pdf     # Challenge rules
├── PROJECT_GUIDE.md              # Detailed projec
```

The `simulation/` folder is a copy of the MATLAB simulation environment provided for this competition (Repo: https://github.com/mathworks-robotics/Virtual-Environment-for-SAE-Aero-Design-). Keep this folder structure intact.

## Quick start

1. Install the MATLAB release and toolboxes listed in the [setup guide](docs/SETUP.md).
2. Open `simulation/RC_Demo.prj` in MATLAB.
3. Configure aircraft data using the Excel-template or DIGITAL DATCOM setup
   workflow.
4. Run design validation and review import warnings, units, and dimensions.
5. Connect and calibrate the pilot input device, then test the calibrated
   actuator output.
6. Launch the simulation and select the required environment.
7. Run a manual mission and review the `out` variable and Simulation Data
   Inspector results.

Do not use flight results for design decisions until the aircraft data,
controller calibration, and model behavior have been checked. Record the
data revision, environment, controller calibration, simulation duration, and
repository commit for important results.

## Project status

This repository is at the initial documentation and project-integration
stage. Aircraft-specific data, repeatable baseline tests, verification
evidence, and submission artifacts are tracked in [TODO](docs/TODO.md).

## Contributing

When changing the model or aircraft data:

- Keep units, coordinate systems, and sign conventions explicit.
- Record the source, revision/date, and confidence of important values.
- Preserve required challenge interfaces unless a change is justified in the
  Engineering Report.
- Add or update verification evidence for behavior affected by the change.
- Update the relevant documentation and [TODO](docs/TODO.md).

## License and upstream project

The MATLAB/Simulink project includes its own
[license](simulation/license.txt). The simulation originated from MathWorks'
Virtual Environment for SAE Aero Design project; see
[simulation/README.md](simulation/README.md) for upstream details and support
information.
