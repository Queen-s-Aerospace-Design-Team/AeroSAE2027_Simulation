1. Aircraft geometry

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

2. Mass properties

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

3. Aerodynamic data

The simulation needs aircraft-level aerodynamic data, not only component
dimensions. Provide the best available source, such as wind-tunnel data,
DIGITAL DATCOM, XFLR5, AVL, CFD, or documented engineering estimates.

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

4. Propulsion data

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

5. Control surfaces and actuators

- Control surfaces present
- Surface-to-actuator mapping
- Positive-deflection direction for each surface
- Maximum and minimum deflection
- Neutral deflection
- Servo travel or commanded range
- Actuator rate limits
- Actuator delay or time constant, if known
- Throttle command range and direction