# Mechanical Design

## Overview

### Software

* **Solid Edge** was used for the mechanical design and assembly of all components.

### File Types

* **.par** – Individual CAD part files.
* **.asm** – Assembly files containing multiple CAD parts.
* **.3mf** – 3D printing files exported from Solid Edge and prepared for slicing and manufacturing.

---

## Goals

* Modular design
* Minimize material usage and printing time
* Easy maintenance and replacement of components
* Suitable for rapid prototyping using 3D printing

---

## Problems and Solutions

### Weight Distribution and Stability

Keeping the robot compact and well-balanced is important for stable movement and maneuverability.

To achieve a low center of gravity, the heaviest components, such as the motors and battery, are mounted as low as possible in the chassis. Lighter components, including the Arduino Uno and the custom PCB, are positioned above the base plate.

This arrangement improves stability, reduces the risk of tipping, and contributes to more predictable driving behavior.

### Material Usage

3D printing large components can require significant amounts of filament and long print times.

To reduce both material consumption and printing time, the base plate was designed with only the structurally necessary regions remaining solid. Non-essential material was removed wherever possible while maintaining sufficient rigidity.

The modular design further reduces material waste, as individual components can be reprinted and improved without replacing the entire assembly.

### Modularity

A modular design simplifies maintenance, repairs, and future upgrades.

To achieve this, threaded inserts were integrated wherever repeated assembly and disassembly is expected. This provides stronger and more reliable connections than directly threading into plastic components.

### Surface Quality of Circular Features

Circular features in CAD models can appear faceted after export, resulting in a visibly polygonal surface on printed parts.

To improve the appearance of round objects, the CAD models are exported using the dedicated 3D printing export settings. The following parameters are used in Solid Edge:

* Conversion tolerance: **0.001 mm**
* Maximum facet angle: **1.0°**

These settings significantly increase the mesh resolution and improve the visual quality of curved surfaces.

---

## Future Improvements

* Improved cable management
* Printable sensor mounts
* Weight reduction of non-critical components
* Additional mounting points for future hardware
