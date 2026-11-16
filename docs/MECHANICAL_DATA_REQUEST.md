# Mechanical team data request

This document lists the aircraft information the simulation team needs from
the mechanical team. The goal is to represent the aircraft as it is already
being designed and built. The simulation is not being used to determine the
aircraft's overall design, so design alternatives and optimization studies
are not required for the initial handoff.

Please provide the data in a spreadsheet, CAD export, test report, or other
source file where appropriate. For every value, include the unit, source,
revision/date, and any assumptions. If a value is not known yet, mark it as
estimated rather than leaving its status unclear.

## Required for the first working model

### 1. Aircraft geometry

Provide the dimensions needed to define the aircraft and its reference
frames:

- Wingspan
- Wing planform and total wing area
- Mean aerodynamic chord
- Fuselage length and major reference dimensions
- Horizontal-tail and vertical-tail geometry
- Control-surface geometry and hinge locations
- Propeller diameter and location
- Motor location and thrust-line angle
- Landing gear or wheel locations, if modeled
- The aircraft datum and body-axis definition

If available, provide a CAD drawing or export showing the origin, reference
axes, component locations, and dimensions. State whether dimensions are
measured from the nose, a CAD origin, or another datum.

### 2. Mass properties

Provide the aircraft mass properties for the configuration that will be
simulated:

- Empty mass
- Payload or competition payload mass
- Battery mass and battery location
- Gross or takeoff mass
- Center-of-gravity location in body coordinates
- Moments of inertia:
  - `Ixx`
  - `Iyy`
  - `Izz`
- Products of inertia, if available

Please identify the configuration for each set of values. For example, state
whether the values include the battery, payload, landing gear, and
electronics. A CAD-derived inertia report or measured mass-balance result is
preferred.

### 3. Aerodynamic data

The simulation needs aircraft-level aerodynamic data, not only component
dimensions. Provide the best available source, such as wind-tunnel data,
DIGITAL DATCOM, XFLR5, AVL, CFD, or documented engineering estimates.

At minimum, provide:

- Lift coefficient (`CL`)
- Drag coefficient (`CD`)
- Pitching-moment coefficient (`Cm`)
- Side-force coefficient (`CY`), if available
- Rolling-moment coefficient (`Cl`), if available
- Yawing-moment coefficient (`Cn`), if available
- Control-surface effectiveness
- Stability derivatives, if available

For each data set, identify the independent variables and ranges, such as
angle of attack, sideslip angle, airspeed, and control deflection. Also
provide the reference area, reference chord, reference span, Reynolds-number
assumptions, and sign conventions.

If aerodynamic data is not available yet, provide the planned source and a
first estimate so the simulation team can identify the missing inputs.

### 4. Propulsion data

Provide the actual motor, propeller, and battery configuration:

- Motor make/model or motor specification
- Propeller make/model, diameter, pitch, and blade count
- Motor and propeller rotation direction
- Battery cell count, nominal voltage, capacity, and mass
- Maximum throttle or motor limits
- Thrust versus throttle or RPM
- Current versus throttle or RPM
- Power versus throttle or RPM
- Motor response time or spool-up assumption, if known
- Propeller and motor position relative to the aircraft datum

A thrust-stand test is preferred. Manufacturer data or a documented estimate
is acceptable for the first model. State whether the data is static or
forward-flight data and identify the test conditions.

### 5. Control surfaces and actuators

Provide the physical control configuration:

- Control surfaces present
- Surface-to-actuator mapping
- Positive-deflection direction for each surface
- Maximum and minimum deflection
- Neutral deflection
- Servo travel or commanded range
- Actuator rate limits
- Actuator delay or time constant, if known
- Throttle command range and direction

Include a simple diagram or table if the mapping is not obvious. The
simulation team also needs the RC channel mapping and a confirmation of the
expected direction of each aircraft response. The final channel calibration
will be performed by the simulation team, but the mechanical team should
confirm the physical directions and limits.

## Useful follow-up information

These items are not required to get the first model running, but they improve
the quality of the simulation and its verification:

- Measured propeller thrust, current, and power at multiple throttle points
- Measured aircraft mass and center of gravity
- Updated CAD mass-property exports
- Control-surface hinge moments or measured actuator loads
- Landing-gear geometry, wheel diameter, and rolling/braking assumptions
- Structural or component deflection that changes control geometry
- Motor thrust-line misalignment
- Aircraft trim condition and expected cruise speed
- Stall speed or other measured performance points
- Ground-test or flight-test observations
- Known limitations in any aerodynamic or propulsion data

## Data format and handoff requirements

For each file or table, include:

| Field | Example |
| --- | --- |
| Data name | Takeoff configuration mass properties |
| Configuration | Battery installed, competition payload installed |
| Units | SI units preferred |
| Coordinate system | Body axes and origin definition |
| Source | CAD, test, supplier, analysis, or estimate |
| Revision/date | Drawing or test revision and date |
| Confidence | Measured, calculated, estimated, or unknown |
| Contact | Person who can clarify the data |

Use SI units where possible. If another unit system is used, provide the
conversion and do not mix unit systems within a table. Keep the original
source files; do not provide only screenshots or manually retyped values when
an export is available.

## Minimum handoff checklist

- [ ] Aircraft reference frame and datum defined
- [ ] Geometry and reference dimensions provided
- [ ] Simulated mass configuration identified
- [ ] Center of gravity provided
- [ ] Inertia properties provided or explicitly marked unavailable
- [ ] Motor, propeller, and battery configuration provided
- [ ] Aerodynamic data source identified
- [ ] Control-surface directions and limits confirmed
- [ ] Units, sign conventions, and data revision recorded
- [ ] Missing values and planned follow-up sources listed
