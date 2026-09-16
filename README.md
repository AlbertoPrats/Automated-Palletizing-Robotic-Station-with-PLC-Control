# Automatic-Palletizing-Robotic-Station-with-PLC-Control

<p align="center">
  <img src="img/Title_img.png" alt="Automatic Palletizing Robotic Station" width="600">
</p>

---

## 📊 Project Overview

[![Project Type](https://img.shields.io/badge/Project-Robotic%20Teleoperation-blue.svg)](#)
[![Robot](https://img.shields.io/badge/Robot-UR3-red.svg)](https://www.universal-robots.com/)
[![Unity Version](https://img.shields.io/badge/Unity-6000.2.10f1%20(6.2)-green.svg)](https://unity.com/)
[![Simulation](https://img.shields.io/badge/Simulation-Meta%20XR-orange.svg)](https://developer.oculus.com/)
[![Protocol](https://img.shields.io/badge/Protocol-XML--RPC%20%2F%20TCP%2FIP-yellow.svg)](#)

**OP70** is an automated rejection handling and palletizing cell developed for a ficticious Operation 70 (OP70) on Line 4 at Advance Motors AB's ficticious engine plant in Skövde, Sweden. The system processes engine cylinder heads, automatically extracting rejected units identified in OP60 and transferring them to Euro pallets without manual intervention. 

The cell acts as the final operation on Line 4. Accepted parts pass through directly to the next operation, while rejected engine heads are redirected to an automated palletizing zone.

---

## 🎬 Visual Demonstration
<details>
<summary>📦 <b>Click here to expand the visual demonstration</b></summary>

  Virtual environment painting:
![Virtual Painting Demo](img/painting_showcase.gif)

  Physical environment painting: 
![Physical Painting Demo](img/robot_painting_showcase.gif)

  Physical environment painting 2: 
![Physical Painting Demo2](img/AR_showcase.gif)


</details>

## 🛠️ Technical Specifications & Prerequisites

### 💻 Software Stack
* **CODESYS v3.5 Control System**: Full PLC simulation including HMI/visual panels.
* **RobotStudio**: Full robotic cell simulation including safety integrations and I/O modules.
* **FluidSIM**: Electrical diagrams including PLC and safety integrations.

---

## 📁 Code Architecture & Components

This repository is organized into four distinct development phases tracking the lifecycle of the project from initial scoping to final virtual validation.

