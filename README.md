# Industrial Robotic Cell Simulation & Automation

## Overview
This project provides a complete 3D simulation and control implementation of an automated industrial robotic cell, developed during the Summer School of Robotics at Politehnica University of Bucharest (UPB). It features a multi-robot pick-and-place system with real-time conveyor belt synchronization and dynamic object handling.

## Technologies Used
* **Environment:** Omron Adept ACE (Automation Control Environment)
* **Robotics Programming:** V+ Language
* **3D Scene & Logic Scripting:** C# (.NET)

## Key Features & Implemented Logic
* **Multi-Controller Synchronization:** Coordinated logic between multiple SmartControllers (e.g., Cobra and Viper industrial robots) to ensure seamless handovers and collision-free operation.
* **Automated Conveyor Tracking:** V+ programs manage digital I/O signals (`WAIT SIG`, `SIGNAL`) to control conveyor belt states based on real-time sensor feedback and part presence.
* **Custom C# Visualization Scripts:** Custom C# scripts executed within the ACE runtime to monitor configuration parameters, calculate dynamic 3D object intersections (bounding boxes), and manage parent-child object relations for accurate real-time rendering of moving parts.
* **Palletizing & Sorting Routines:** Automated pick-and-place routines featuring Z-axis indexing, coordinate transformation, and end-effector (pneumatic gripper) state management.

## Project Structure
```text
├── project/             # Omron Adept ACE workspace and project files (.awp)
├── ACE Scripts             # Exported V+ programs
├── C# Visualisation Script    #  C# scripts
│ Configuration Parameters
└── README.md
