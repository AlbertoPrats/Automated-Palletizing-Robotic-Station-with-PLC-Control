# Automated Palletizing Robotic Station with PLC Control

<p align="center">
  <img src="images/OP70.png" alt="Automatic Palletizing Robotic Station" width="800">
</p>

---

## 📊 Project Overview

[![Project Type](https://img.shields.io/badge/Project-Industrial%20Automation-blue.svg)](#)
[![Robot](https://img.shields.io/badge/Robot-ABB-red.svg)](https://www.abb.com/global/en/)
[![Unity Version](https://img.shields.io/badge/CODESYS-v3.5-green.svg)](https://us.codesys.com//)
[![Simulation](https://img.shields.io/badge/Simulation-ABB%20RobotStudio-orange.svg)](#)
[![Protocol](https://img.shields.io/badge/Protocol-OPC--UA-yellow.svg)](#)

**OP70** is an automated rejection handling and palletizing cell developed for a fictitious Operation 70 (OP70) on Line 4 at Advance Motors AB's ficticious engine plant. The system processes engine cylinder heads, automatically extracting rejected units identified in OP60 and transferring them to Euro pallets without manual intervention. 

The cell acts as the final operation on Line 4. Accepted parts pass through directly to the next operation, while rejected engine heads are redirected to an automated palletizing zone.

---

## 🎬 Visual Demonstration
<details>
<summary>📦 <b>Click here to expand the visual demonstration</b></summary>
  
---

<details>
<summary>🎬 <b>Click here to expand the execution videos</b></summary>

---

Full automatic execution part 1:

![Full auto execution 1](videos/fullauto1.gif)

---

Full automatic execution part 2:

![Full auto execution 2](videos/fullauto2.gif)

---

Full automatic execution part 3:

![Full auto execution 3](videos/fullauto3.gif)

---

  Full manual execution part 1:
  
![Full manual execution 1](videos/fullmanual1.gif)

---

  Full manual execution part 2:
  
![Full manual execution 2](videos/fullmanual2.gif)

---

  Full manual execution part 3:
  
![Full manual execution 3](videos/fullmanual3.gif)

---

  Full execution with production data part 1:
  
![Full execution with production data 1](videos/productiondata1.gif)

---

  Full execution with production data part 2:
  
![Full execution with production data 2](videos/productiondata2.gif)

---

  Pallet dispenser showcase:
  
![Pallet dispenser showcase](videos/dispenser.gif)

---

  General safety simulation showcase:
  
![Safety showcase](videos/safety.gif)

---

  Pallet conveyor simulated error showcase:
  
![Pallet conveyor error](videos/palletconveyorerror.gif)

---

  Product conveyor simulated error showcase:
  
![Product conveyor error](videos/producconveyorerror.gif)
  
</details>

---

<details>
<summary>🖼️ <b>Click here to expand the robotic cell images</b></summary>

---

  General cell layout:
  
![General cell layout](images/celllayout.png)

---
  
  Close-up of the robot operation area:
  
![Robot closeup](images/robotclose.png)

---
  
  Safety gate 1 with outer light gate muted:
  
![safety gate 1-1](images/safetygate1-1.png)

---
  
  Safety gate 1 with inner light gate muted:
  
![safety gate 1-2](images/safetygate1-2.png)

---

  Safety gate 2 with outer light gate muted:
  
![safety gate 2-2](images/safetygate2-2.png)

---

  Safety gate 2 with inner light gate muted:
  
![safety gate 2-1](images/safetygate2-1.png)

</details>

---

<details>
<summary>🖼️ <b>Click here to expand the PLC panel images</b></summary>

---
  
  Operator panel 1:
  
![Operator panel 1](images/operatorpanel1.png)

---
  
  Operator panel 2:
  
![Operator panel 2](images/operatorpanel2.png)

---
  
  Operator panel 3:
  
![Operator panel 3](images/operatorpanel3.png)

---
  
  Disgnostic panel:
  
![Diagnostic panel](images/diagnosticpanel.png)

---
  
  Production panel:
  
![Production panel](images/productionpanel.png)
 
---
 
  Manual operation panel 3 (SOP714 to SOP717):
  
![Manual operation panel 3](images/manualpanel1.png)

---
  
  Manual operation panel 4 (SOP720):
  
![Manual operation panel 4](images/manualpanel2.png)

---
  
  Process panel:
  
![Process panel](images/processpanel.png)

---

  Overview panel:
  
![Overview panel](images/overviewpanel.png)
  
</details>

---

</details>

## 🛠️ Technical Specifications

### 💻 Software Stack
* **CODESYS v3.5 Control System**: Full PLC simulation including HMI/visual panels.
* **RobotStudio**: Full robotic cell simulation including safety integrations and I/O modules.
* **FluidSIM**: Electrical diagrams including PLC and safety integrations.

---

## 📁 Project Structure & Code Architecture

This repository is organized into four distinct development phases tracking the lifecycle of the project from initial scoping to final virtual validation.

- Phase 1: Project Scope & Architecture Setup
  - Definition of functional requirements, station operational sequences, and hardware/software selection.
  - Initial mapping of control interfaces and cell safety boundaries.

- Phase 2: Design Review - Base System Design & Cell Layout
  - Early 3D layout of the OP70 station in ABB RobotStudio.
  - Preliminary electrical schematics and basic PLC POU structures in CODESYS.

- Phase 3: FAT - Deep Refinement & Detailed Schematics
  - Complete electrical schematic sets (.prj), detailed I/O signal lists (.xlsx), and packed RobotStudio functional station assets (.rspag).
  - Safety system integration (E-Stops, light curtains, interlocks) and signal mapping.

- Phase 4: SAT - Final Integration & Functional Execution
  - Production-ready OP70 Robot Program with motion paths and handshake logic.
  - Complete OP70 PLC Project in CODESYS including full HMI/Visualization Control Panels.
  - RobotStudio OPC-UA Configuration (.csv) mapping node addresses for virtual hardware communication.

### 🧠 Subsystem Breakdown & Simulation Architecture

Because this project serves as a comprehensive fictitious case study, physical hardware is entirely modeled through digital twin techniques. The cell relies on software-in-the-loop (SIL) co-simulation between CODESYS (acting as the master PLC) and ABB RobotStudio (acting as the robotic workstation and physical cell physics simulator).

<details>
<summary>📦 <b>Click here to expand the detailed architecture</b></summary>

```mermaid
  graph TD
      %% Styling
      classDef plc fill:#1f77b4,stroke:#0d3b66,stroke-width:2px,color:#ffffff;
      classDef robot fill:#ff7f0e,stroke:#a34800,stroke-width:2px,color:#ffffff;
      classDef opc fill:#2ca02c,stroke:#135213,stroke-width:2px,color:#ffffff;
      classDef inner fill:#f4f4f6,stroke:#cccccc,stroke-width:1px,color:#333333;
  
      %% Subsystem: CODESYS PLC
      subgraph CODESYS["CODESYS V3.5 (Master PLC)"]
          HMI["Control Visualizations<br/>(HMI Panels)"]:::inner
          POU["Main Control POUs &<br/>Safety Logic"]:::inner
      end
      class CODESYS plc;
  
      %% Subsystem: OPC-UA Connection
      OPC["<b>OPC-UA Communication Interface</b><br/>(Nodes & Tags defined via CSV)"]:::opc
  
      %% Subsystem: ABB RobotStudio
      subgraph RS["ABB RobotStudio (Robot Cell Simulation)"]
          VC["Virtual Controller<br/>(RAPID Code & TCP)"]:::inner
          UA_Server["OPC-UA Server Module<br/>& Node Mapping"]:::inner
          SIM["3D Physical Simulation & Cell Kinematics"]:::inner
      end
      class RS robot;
  
      %% Connections
      CODESYS <==>|"Data Exchange (Booleans, Integers, Reals)"| OPC
      OPC <==>|"Read / Write Signals"| RS
  
      %% Internal Visual Groupings
      HMI --- POU
      VC --- UA_Server
      UA_Server --- SIM
```
---

1. Master Control Subsystem (CODESYS PLC & Visualizations)

- PLC Logic (POUs): Runs the main state machines, station cycle timing, fault management, and safety interlocks.
- HMI Visualizations: Includes multiple interactive control panels for manual operation, automatic mode execution, sensor feedback monitoring, and alarms.

2. Robotic & Physical Cell Subsystem (ABB RobotStudio)
- Virtual Controller & Kinematics: Executes the finished RAPID code, controlling robot paths, tool center points (TCP), and station actuators (grippers, fixtures, conveyors).
- Physics & Smart Components: Simulates part presence sensors, pneumatic clamp movements, and physical part collisions.

3. Inter-System Connectivity (OPC-UA Data Exchange)
The link between CODESYS and RobotStudio is handled seamlessly via OPC-UA:
- OPC-UA Server: RobotStudio hosts a built-in virtual OPC-UA server node.
- Tag Configuration: The uploaded RobotStudio OPC UA Configuration File (.csv) registers the tags, data types (Booleans, Integers, Reals), and directionality.
- CODESYS Client Integration: CODESYS connects to the RobotStudio OPC-UA endpoint using configured Global Variable Lists (GVL). Signals such as Start_Cycle, Robot_In_Home, Gripper_Close, and Safety_Ok are exchanged deterministically in real time to synchronize the station.


</details>

---

## 🚀 Quick Start & Execution Guide

1. Configure RobotStudio Station & OPC-UA Server
   - Open ABB RobotStudio and open or import the OP70_Robot_Program.
   - Navigate to the *Controller* tab $\rightarrow$ *OPC-UA Configuration*.
   - Import the RobotStudio_OPC_UA_Configuration_File.csv to register all published I/O tags, nodes, and data types.
   - Start the Virtual Controller and verify the OPC-UA Server status shows Active.
2. Configure CODESYS PLC & Communication
   - Open CODESYS and open the OP70_PLC project.
   - Go to *Device Tree* $\rightarrow$ *Symbol Configuration / OPC UA Client Manager*.
   - Verify the endpoint URI matches your local RobotStudio OPC-UA server address.
   - Build the project to ensure there are no compilation errors or missing tag references.
3. Launch Simulation & Co-Simulation
   - In RobotStudio, click *Play* on the simulation ribbon to start physical cell physics and station monitoring.
   - In CODESYS, click *Login* to connect to the active PLC runtime, then click *Start*.
   - Open the *Control Panel Visualizations* in CODESYS to trigger system execution.
---

This system has been developed as a project in collaboration with Aitor Sagarna Zabala, Paula Bolívar Pérez and Selene Delgado Pastor.
