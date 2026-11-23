# LED Circuit PCB — First PCB Design

## Project Overview

This project documents my first printed circuit board (PCB) design using KiCad 10.

The objective was to learn the complete PCB design workflow, starting from a simple LED circuit and progressing through schematic capture, component footprint selection, PCB layout, copper routing, design rule verification, and 3D visualization.

The project was completed virtually to develop practical electronics design skills without requiring physical components.

## Final PCB Design

![3D PCB Design](images/3d-view.png)

## Tools Used

- KiCad 10 — Schematic capture and PCB design
- Tinkercad Circuits — Basic circuit simulation
- GitHub — Project documentation and version control

## Components

| Component | Description |
|---|---|
| J1 | 2-pin power connector |
| R1 | 470 Ω resistor |
| D1 | 5 mm through-hole LED |
| Power supply | 9 V DC input |

## Circuit Operation

The circuit uses a current-limiting resistor connected in series with an LED.

When a suitable 9 V DC power supply is connected with the correct polarity, current flows through the resistor and LED.

The resistor limits the current to protect the LED.

Assuming an LED forward voltage of approximately 2 V:

\[
I = \frac{V_s - V_{LED}}{R}
\]

\[
I = \frac{9 - 2}{470} \approx 14.9\text{ mA}
\]

This is a theoretical estimate. The actual current depends on the LED characteristics.

## Design Process

### 1. Circuit Simulation

I first explored a basic LED circuit using Tinkercad, learning about component connections, resistor selection and voltage measurement.

![Tinkercad Simulation](images/tinkercad-simulation.png)

The initial simulation was a learning prototype. The final PCB design uses a 470 Ω resistor.

### 2. Schematic Design

I created an electrical schematic in KiCad consisting of a power connector, resistor and LED.

I connected the components and used KiCad's Electrical Rules Checker (ERC) to verify the schematic.

![KiCad Schematic](images/schematic.png)

### 3. PCB Layout

I assigned through-hole footprints, transferred the schematic into the PCB Editor and arranged the components on the board.

I created a rectangular board outline on the Edge.Cuts layer and routed the electrical connections using front-copper traces.

![PCB Layout](images/pcb-layout.png)

### 4. Design Verification

I performed the following checks:

- Electrical Rules Check (ERC)
- Design Rules Check (DRC)
- PCB-to-schematic parity verification
- Unrouted connection inspection

The completed design reported zero errors in the performed checks.

### 5. 3D Visualization

I used KiCad's 3D Viewer to inspect component placement and the board's appearance.

I also added silkscreen labels and the project title, "LED CIRCUIT V1.0".

## What I Learned

Through this project, I gained introductory experience with:

- KiCad schematic capture
- Electronic component symbols and footprints
- Through-hole PCB design
- Copper trace routing
- PCB design layers and board outlines
- ERC and DRC verification
- 3D PCB visualization
- Engineering project documentation

## Project Status

**Completed: Virtual PCB Design**

The schematic and PCB layout have been created, and KiCad design checks were performed successfully.

The PCB has not been physically manufactured, assembled or tested. A physical prototype and hardware measurements would be necessary to validate its real-world performance.

## Future Improvements

- Fabricate and assemble the PCB
- Measure LED voltage and operating current
- Add clearer power polarity markings
- Reduce unnecessary board space
- Develop more advanced PCB projects involving sensors and microcontrollers
