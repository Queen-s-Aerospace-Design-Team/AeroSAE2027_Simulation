# MathWorks SAE Aero Design Simulation Challenge rules summary

This document summarizes the key concepts the team needs when developing and
testing the simulation. It is a practical reference, not a replacement for
the [official challenge rules PDF](../MathWorks_SAE_Aero_Design_Simulation_Challenge_27.pdf).
The official PDF is authoritative if this summary and the rules differ.

## Challenge purpose and score

The challenge evaluates both the virtual flight and the technical quality of
the submitted model and report. The total score is 100 points:

| Component | Points |
| --- | ---: |
| Two virtual flight missions | 50 |
| Engineering Report and submitted model | 50 |

Each mission is worth 25 points:

| Mission step | Points |
| --- | ---: |
| Takeoff and climb | 5 |
| First 180-degree turn | 5 |
| Second 180-degree turn | 5 |
| Final approach / return to departure sector | 5 |
| Landing, rollout, and stop | 5 |

Only the first 360-degree circuit attempted during a mission is scored.
Circuit steps are scored in order, so an invalid earlier step prevents later
dependent steps from scoring.

## Required missions

The team must complete one manually flown 240-second mission in each of:

1. Sea Level Standard.
2. The applicable competition-site environment:
   - Aero Design East: Lakeland, Florida.
   - Aero Design West: Van Nuys, California.

The aircraft must be controlled with an RC transmitter or joystick. Scored
missions must not use an autopilot or scripted control inputs. The project
must use calibrated RC commands recorded before actuator dynamics, and the
selected flight must be replayable by the judges through the submitted model.

## Mission behavior

### Takeoff and climb

The aircraft must:

- Start from rest.
- Leave the ground.
- Reach at least 0.5 m AGL for at least 0.5 seconds.
- Complete takeoff within the applicable class limit.
- Climb to approximately 30 m AGL.

Takeoff limits are:

| Class | Takeoff limit |
| --- | --- |
| Regular | Under 100 ft / 30.48 m |
| Micro | Under 50 ft / 15.24 m |
| Advanced | No upper limit |

### Circuit

The aircraft must continue in the takeoff direction, reach the required
first-turn distance, complete a 180-degree turn, pass the origin in the
opposite direction, reach the required distance on the opposite side, and
complete a second 180-degree turn in the same direction. It must then return
on runway heading to the departure sector.

For Advanced Class, the first-turn distance is 400 ft / 121.92 m. During the
circuit, altitude must remain between 25 m and 35 m AGL, or 30 +/- 5 m AGL.
Leaving this band can invalidate the circuit.

### Landing

The aircraft must return on runway heading, descend, touch down, remain below
0.5 m AGL, and stop with horizontal ground speed below 0.5 m/s for at least
1 second.

For Advanced Class, the simulation challenge table has no upper landing
distance limit.

## Model requirements and restrictions

The submitted model should represent the aircraft the team is designing. It
should include aircraft-specific values where applicable:

- Geometry and reference dimensions
- Mass, center of gravity, and inertia
- Aerodynamic coefficients and stability derivatives
- Motor, propeller, and battery assumptions
- Control-surface limits and actuator dynamics
- Initial or trim assumptions

Estimated or analytical values are acceptable during preliminary design when
the team documents their source, assumptions, verification method, and
limitations.

The required common environment and calibrated-input path must be preserved.
Do not modify the Environment subsystem, the Calibrated Fixed-Wing input
subsystem, or related supporting functions without a technically justified
reason and appropriate documentation. Aircraft parameters, aircraft-specific
data, internal Aircraft Dynamics architecture, and visualization may be
changed when required interfaces are retained.

## Submission contents

Each team may submit once. The submission must include:

- The complete MATLAB project.
- The selected flight-data file from each required environment.
- The required pre-actuator RC command data.
- An Engineering Report PDF.

The report is limited to four pages, including figures and tables. The rules
specify:

- 12-point proportional font
- Double line spacing
- Two-column layout
- ANSI A / 8.5 x 11 inch page size
- Required margins
- PDF format
- Header identifying team, school/university, class, and competition

The report should explain the technical problem, why MATLAB/Simulink was
selected, the aircraft model and simulation setup, design insights, test and
verification evidence, assumptions, limitations, and what did or did not
work. Important files and model paths should be identified so the judges can
reproduce the work.

## Evidence and reproducibility

For important model values and results, record:

- Units
- Source
- Revision or date
- Confidence level
- Coordinate system and sign convention where relevant
- Simulation release
- Team commit
- Aircraft-data revision
- Environment
- Controller calibration
- Simulation duration
- Test objective

Useful independent evidence includes hand calculations, CAD mass properties,
supplier motor/propeller data, thrust-stand data, bench tests, ground tests,
wind-tunnel results, and physical flight tests. For each verification activity,
record the prediction, independent result, acceptance criterion, difference,
and whether the difference affects the model's intended use.

## Team checklist

- [ ] Confirm the aircraft class.
- [ ] Confirm the applicable competition site.
- [ ] Confirm the MATLAB release and required toolboxes.
- [ ] Complete and document the aircraft-specific model data.
- [ ] Calibrate and test the pilot input device.
- [ ] Run a 240-second Sea Level Standard mission.
- [ ] Run a 240-second competition-site mission.
- [ ] Confirm both missions use calibrated pre-actuator RC commands.
- [ ] Save selected flight data and command recordings.
- [ ] Verify takeoff, circuit altitude, turns, landing, rollout, and stop.
- [ ] Prepare the four-page Engineering Report.
- [ ] Use the project submission workflow to export the final package.
- [ ] Verify the final download link works without sign-in or approval.
- [ ] Do not change the final package or link after submission.
