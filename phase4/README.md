**Site Acceptance Test**
---
### OP70_PLC
This file contains the fully developed master PLC project created in Codesys.
  - Control Panel Visualizations: HMI panels for manual overrides, auto-mode execution, station monitoring, and system diagnostic displays.
  - Main Logic Programs (POUs): State machine logic managing cell sequences, station interlocks, safety monitoring, and device drivers.
  - Global Variable Lists (GVL) & Mapping: Hardware mapping, product data manipulation, and OPC-UA node definitions for communication across the cell.

### OP70_Robot_Program
This file is a packed RobotStudio project containing the final finished robot cell, including the 3D cell model, station logic and robot programming.
  - 3D Geometry & Cell Layout: Complete physical layout including the robot, end-effectors, safety fencing, conveyors, and part fixtures.
  - Kinematics & Tooling: Configured robot Tool Center Points (TCP), workobjects, and gripper action mechanisms, with their respective smart components.
  - RAPID Code & Virtual Controller: Robot program modules, motion routines, wait conditions, and integrated OPC-UA communication configuration.

### RobotStudio_OPC_UA_Configuration_File
This file contains the configuration setup used to establish the server-client mapping in RobotStudio for OPC-UA communication.
  - Node Map & Tags: Lists all published and subscribed variables required between the virtual controller and external devices.
  - Data Type Definitions: Standardized definitions mapping standard data types (e.g., Boolean flags, Integers, Reals) across the network interface.
  - Communication Settings: Configured update rates, read/write permissions, and node identifier mappings for the OPC-UA endpoint.
