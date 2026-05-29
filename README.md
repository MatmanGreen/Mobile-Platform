# Autonomous Mobile Robot

## Project Goal

Development of an autonomous mobile robot using:

* ROS2
* Computer Vision
* NEMA17 + TMC2209
* Gazebo Simulation
* SLAM

The goal is autonomous navigation in simple indoor environments.

---

## Current Status

### Completed

* [x] Selection of electronic components
* [x] Motor control board using TMC2209 drivers

### Work in Progress

* [ ] 3D-printable chassis model
* [ ] Gazebo simulation
* [ ] Basic publisher/subscriber communication
* [ ] Camera integration
* [ ] SLAM
* [ ] Path planning

### Current Challenges

* Unstable motor control at high speeds
* No encoder feedback on the NEMA17 motors

---

## Technologies

### Hardware

* Arduino Uno
* NEMA17 Stepper Motors
* TMC2209 Stepper Drivers
* Prefboard

### Software

* C++
* ROS2 Jazzy
* Gazebo
* OpenCV (planned)

---

## Repository Structure

```text
Autonomous-Mobile-Robot/
├── mechanical/
├── electronics/
└── software/
```

### Mechanical

Contains CAD models, assemblies, and 3D-printable parts.

### Electronics

Prefboard designs and hardware documentation.

---

## Roadmap

* [ ] Complete mechanical design
* [ ] Assemble first prototype
* [ ] Integrate ROS2 communication
* [ ] Add camera system
* [ ] Implement SLAM
* [ ] Implement autonomous navigation

---

## Project Status

This project is currently under active development.
Updates will be added as new milestones are reached.
