# Industrial Robotic Cell Simulation and Automation

A 3D simulation and control program for an automated robotic cell, made at the Robotics Summer School at Politehnica University of Bucharest (UPB). Several robots do pick-and-place work, synchronized with a conveyor belt, on parts that are moving.

## Technologies
- **Environment:** Omron Adept ACE
- **Robot programming:** V+
- **3D scene logic:** C# (.NET)

## What it does
- **Two synchronized controllers:** separate SmartControllers (Cobra and Viper robots) coordinate so that parts are handed over without collisions.
- **Conveyor control:** V+ programs use digital I/O signals (`WAIT SIG`, `SIGNAL`) to start and stop the belt based on the sensors and on whether a part is present.
- **C# scripts in ACE:** read configuration parameters, compute 3D intersections between objects (bounding boxes) and manage parent-child links, so that moving and gripped parts are shown correctly.
- **Palletizing and sorting:** pick-and-place routines with Z-axis indexing, coordinate transformations and gripper (pneumatic) control.

## Project structure
```text
├── Project/                    # Omron Adept ACE project (.awp)
├── ACE Scripts/                # exported V+ programs
├── C# Visualisation Script/    # C# script
├── Configuration Parameters/   # belt, sensor and gripper parameters
└── README.md
```
