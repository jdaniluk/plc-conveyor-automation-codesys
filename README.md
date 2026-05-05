# plc-conveyor-automation-codesys
PLC-based conveyor automation system using CODESYS ladder logic and Factory I/O simulation.
# PLC Conveyor Automation System

## Overview
This project demonstrates a PLC-based conveyor automation system developed using CODESYS ladder logic and Factory I/O simulation. The system models a manufacturing-style conveyor process using start/stop control, emergency-stop behavior, sensor-based stopping, and part-counting logic.

The purpose of the project was to analyze how programmable logic controllers are used in industrial automation to coordinate operator inputs, sensors, motor outputs, and machine sequencing.

## Demo / Report
- Final report PDF: `PLC_Conveyor_Automation_Report.pdf`
- Demo video: https://youtu.be/NjD3blgmhTs?si=GTT_wQP5m68gaec7

## Tools and Technologies
- CODESYS
- Factory I/O
- Ladder logic
- PLC simulation
- Digital input/output logic
- Discrete-event control
- Virtual commissioning

## System Description
The system is organized as a closed automation loop:

1. Operator inputs are sent to the PLC logic.
2. CODESYS executes the ladder logic program.
3. The conveyor motor output is sent to the Factory I/O simulation.
4. The simulated conveyor moves or stops.
5. Sensor feedback is returned to the PLC.

The project uses this structure to demonstrate how industrial automation systems connect control logic with plant behavior.

## Inputs and Outputs
Main inputs:
- Start button
- Stop button
- Emergency stop
- Reflective sensor
- Entry sensor
- Exit sensor

Main outputs:
- Conveyor motor
- Buffer conveyor
- Start/run indicator light

## Control Modes
### Manual Conveyor Control
The first mode uses a start button, stop button, and emergency stop input. A latching rung keeps the conveyor running after the start button is released, while the stop button and emergency stop remove the run condition.

### Sensor-Based Automatic Control
The second mode adds a reflective sensor that detects a box on the conveyor. When the sensor detects the object, the PLC logic changes the output state and stops the conveyor automatically.

### Counter and Buffer Logic
The third mode expands the system using counter instructions and comparison logic. This allows the conveyor system to track parts entering and leaving sections of the conveyor and manage buffered part flow.

## Engineering Concepts Demonstrated
- PLC scan cycle behavior
- Ladder logic programming
- Start/stop latching
- Emergency-stop interlocking
- Sensor-based feedback
- Discrete-event control
- Counter instructions
- Comparison logic
- Virtual commissioning
- Industrial automation sequencing

## Results
The simulation successfully demonstrated multiple levels of conveyor automation. The project began with basic start/stop control, expanded into sensor-based stopping, and then added counter-based logic for part tracking and buffer control.

The project showed how ladder logic can start with simple machine control and grow into a more structured automation sequence.

## Limitations
This project was tested in simulation only. A physical conveyor system would introduce additional issues such as wiring errors, sensor alignment, electrical noise, motor delay, mechanical wear, and real-world timing variation.

## Future Improvements
- Implement the logic on a physical PLC
- Add fault detection and alarm handling
- Add motor speed control using a VFD
- Add HMI screen control
- Add industrial network communication
- Expand the system into a multi-station production line
