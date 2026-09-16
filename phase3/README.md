**Factory Acceptance Test**
---
### IO List OP70
  This file outlines the communication tags and variable mapping between the PLC and the robot's OPC-UA server.
  - Variable Name & List: Identifies the global variable and tag names used within the PLC program and OPC-UA node structure (GVL or IO).
  - Memory Address & Data Type: Specifies the hardware mapping addresses and data formats (e.g., BOOL, INT, REAL).
  - Signal Direction: Defines signal flow parameters (Input vs. Output / Read vs. Write) between the controller and the robot.
  - Functional Comments: Describes the intended purpose of each IO tag (e.g., gripper control, cycle start, status feedback).

### OP70_elec_drawings
  This file contains the complete schematic diagrams for all electrical connections within the cell.
  - Power Distribution & PLC Wiring: Detail diagrams for main power supply, PLC controller power, digital/analog I/O modules, and field devices.
  - Robot Controller & Interfacing: Schematic diagrams for robot controller power, communication links, and server/PLC hardware interfaces.
  - Safety & E-Stop System: Wiring configurations for safety relays, Emergency Stop circuits, light curtains, and safety gate interlocks.
  - Clamp & Motor Connections: Electrical connections for pneumatic valves, double-acting cylinders and conveyor motors.

## OP70_robot_cell
  This file is a packed RobotStudio project containing the 3D cell model, station logic and robot programming.
  - 3D Geometry & Cell Layout: Complete physical layout including the robot, end-effectors, safety fencing, conveyors, and part fixtures.
  - Kinematics & Tooling: Configured robot Tool Center Points (TCP), workobjects, and gripper action mechanisms, with their respective smart components.
  - RAPID Code & Virtual Controller: Robot program modules, motion routines, wait conditions, and integrated OPC-UA communication configuration.
