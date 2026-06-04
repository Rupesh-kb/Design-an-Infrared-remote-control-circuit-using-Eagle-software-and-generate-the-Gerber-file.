# Design an Infrared remote control circuit using Eagle software

## AIM:
To design the schematic and PCB layout diagram of an Infrared remote control circuit using Eagle software.

## EQUIPMENT REQUIRED:
● Hardware: Personal Computer (PC)
● Software: Eagle

## PROCEDURE:
```
 Create a New Project:
o Launch EAGLE and start a new project for your PCB design.
o Within the project, create a new schematic file.
 Add Components:
o Utilize the built-in libraries in EAGLE or create custom libraries if needed.
o Use the 'Add' tool to place the required components onto the schematic sheet.
 Make Connections:
o Connect the components using the 'Net' tool.
o Label the nets clearly to maintain clarity and organization in your design.
 Check for Errors:
o Once the schematic design is complete, perform an Electrical Rule Check (ERC) to identify and correct any errors.
o Save the schematic after confirming that no errors are present.
 Switch to Board Layout:
o Click on the 'Generate/Switch to Board' button to create the PCB layout from the schematic.
 Arrange Components and Route Traces:
o In the board layout editor, arrange the components to optimize space and reduce signal interference.
o Use the 'Route' tool to connect the components based on the schematic design.
o Ensure proper routing by utilizing the available editing tools in EAGLE to avoid design rule violations.
 Design Rule Check (DRC):
o Perform a Design Rule Check (DRC) to ensure that the routing and layout comply with design standards and that there are no issues.
o Save the board layout after resolving any errors.
 Generate Gerber Files:
o Go to File > CAM Processor and configure the CAM jobs to generate Gerber files for all PCB layers, such as copper layers, silkscreen, solder mask, and drill files.
o Verify the generated files to ensure they contain all necessary information for manufacturing.
 Save Manufacturing Files:
o Save the Gerber files and any other required manufacturing files to send to your PCB manufacturer for fabrication.
```

## THEORY:
The Infrared Remote Control Switch is a simple electronic circuit that uses an infrared (IR) receiver to detect signals from a standard TV remote and control an electrical load, such as a lamp or appliance, through a relay. At the heart of the circuit lies the CD4027 IC, which is a dual JK flip-flop. JK flip-flops are bistable multivibrators capable of storing one bit of data and toggling their state with every pulse input. In this circuit, the TSOP1738 IR receiver module is used to detect IR pulses sent by a remote control. The TSOP1738 is designed to receive 38kHz modulated infrared signals and output a demodulated digital signal that can be read by a microcontroller or logic circuit. The 2N4403 PNP transistor is used to amplify and condition the signal from the TSOP1738, ensuring a reliable trigger for the flip-flop. This type of system demonstrates the fundamental concept of remote-controlled electronics using modulated IR signals, logic circuitry, and electromechanical switching components like relays.

## Working:
When a button on the IR remote is pressed, it sends a modulated 38kHz IR signal which is received by the TSOP1738. The TSOP demodulates the signal and produces a low pulse which is fed into the base of the first 2N4403 transistor, acting as an amplifier. This transistor then provides a strong triggering signal to the CD4027 flip-flop IC, which is wired to toggle its output state with each pulse received. The output from the flip-flop then controls the base of a second 2N4403 transistor, which functions as a switch to drive a 5V relay. When the flip-flop output goes high, the transistor conducts and energizes the relay coil, turning ON the connected load. On receiving the next IR pulse, the output toggles low, deactivating the relay and turning OFF the load. An LED indicator connected in parallel with the relay provides a visual cue of the ON/OFF status. The 1N4007 diode across the relay protects the circuit from voltage spikes due to back EMF when the relay is switched OFF. This toggling operation continues every time a button on the IR remote is pressed, making it suitable for simple wireless control applications.

## CIRCUIT DIAGRAM:
<img width="500" height="254" alt="WhatsApp Image 2026-04-28 at 8 37 05 AM" src="https://github.com/user-attachments/assets/b8a96b4d-9cc8-42c3-98a0-02c18ba0eef7" />

## EXPECTED OUTPUT:

### Schematic diagram
<img width="1600" height="851" alt="image" src="https://github.com/user-attachments/assets/ccd1f61f-5ca0-4156-881c-6bbd6edb1d19" />

### Layout diagram
<img width="1600" height="818" alt="image" src="https://github.com/user-attachments/assets/185d2b94-6b10-48be-9bf2-f4dd54db334e" />

## RESULT:
Thus, the schematic and PCB layout for the Infrared remote control circuit has been successfully designed using Eagle software.







