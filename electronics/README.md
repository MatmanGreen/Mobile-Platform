# Electronics

## Overview

This section contains the electronic hardware used for the autonomous mobile robot.

The current design focuses on reliable motor control, simple integration with ROS2-compatible hardware, and easy maintenance during development.

---

## Hardware

### Microcontroller

* Arduino Uno

### Motor Drivers

* TMC2209 Stepper Drivers
* UART configuration support
* Microstepping support
* Quiet operation

### Motors

* NEMA17 Stepper Motors

### Power System

* 12 V battery
* 12 V to 5 V buck converter for logic electronics

---

## Design Decisions

### Why TMC2209?

The TMC2209 was selected because it provides:

* Quiet operation
* High microstepping resolution
* UART communication
* Good documentation and community support

### Why NEMA17?

The NEMA17 motors used in this project were recovered from a decommissioned 3D printer.

Since the motors were already available, they provided a cost-effective solution for early prototyping and development. Their torque is sufficient for the current requirements of the robot, allowing development and testing to begin without additional hardware costs.

However, stepper motors are not the optimal choice for a mobile robot. Compared to DC motors with encoder feedback, they generally offer lower maximum speeds and can lose steps under demanding operating conditions. Despite these limitations, the NEMA17 motors are suitable for the current prototype and provide a simple and accessible platform for testing mechanical, electronic, and software concepts.


### Why a Prefboard?

A Prefboard improves reliability compared to breadboard-based solutions.

It also simplifies maintenance and future modifications.


## Problems and Solutions

### Motor Step Loss at Higher Speeds

The motors occasionally lose steps during rapid acceleration or high-speed operation.

* Driver current settings were checked.
* Wiring was verified.
* Mechanical resistance was inspected.

Acceleration and speed profiles are being optimized to improve reliability.

### Power Stability

Stepper motors can generate voltage spikes and supply noise.

A dedicated decoupling capacitor is placed close to each TMC2209 driver.
Additional bulk capacitance is used on the main power rail.

---

## Future Improvements

* Add encoder feedback
* Add battery monitoring
* Improve power protection circuitry
* Integrate additional sensor interfaces
* Design a second PCB revision
* Add RaspberryPi for ROS2 and image processing

---
