# Sustainable UV-C Hygiene Chamber

![Hardware Project](https://img.shields.io/badge/Project-Hardware-blue)
![Electronics](https://img.shields.io/badge/Field-Electronics-green)
![Timer IC](https://img.shields.io/badge/IC-NE555-orange)
![License](https://img.shields.io/badge/License-MIT-lightgrey)

A low-cost UV-C sterilization chamber designed to promote the hygienic reuse of glass cups and reduce disposable plastic waste in institutions and workplaces.

## Problem

Disposable plastic cups are widely used in colleges, offices, and cafeterias due to convenience. However, they contribute significantly to non-biodegradable waste and environmental pollution.

Although reusable glass cups are environmentally friendly, hygiene concerns discourage their widespread use.

## Solution

This project presents a **UV-C Hygiene Chamber** that disinfects reusable glassware using germicidal UV-C light. The system ensures safe operation using a **door safety interlock and hardware-based timing control**.

The chamber automatically activates only when the door is closed and provides a buzzer alert after the sterilization cycle is completed.

---

## System Architecture

The system consists of the following functional blocks:

- 12V DC Power Supply
- Door Limit Switch (Safety Interlock)
- Timer A (UV Exposure Timer)
- Relay Driver
- UV-C Lamp
- Timer B (Completion Indicator)
- Buzzer Notification

---

# Block Diagram

![Block Diagram](images/block_diagram.png)

---

# Circuit Diagram

![Circuit Diagram](images/circuit_diagram.png)

---


# Working Principle

1. When the chamber door closes, the **limit switch triggers Timer A**.
2. Timer A operates in **monostable mode** and activates the UV-C lamp for approximately **11 seconds**.
3. The UV-C light disinfects the glassware placed inside the chamber.
4. When the timing cycle finishes, **Timer B is triggered**.
5. Timer B activates the **buzzer for 1–2 seconds**, indicating that sterilization is complete.

---

# Advantages

- Environmentally friendly alternative to disposable cups
- Fully automated operation
- Safe operation using door interlock
- Low-cost hardware design
- No microcontroller required

---

# Applications

- College cafeterias
- Office pantries
- Small food outlets
- Household sterilization of glassware

---

# Limitations

- UV-C only disinfects surfaces directly exposed to light
- Chamber size limits object size
- Fixed timing due to hardware design

---

# Future Improvements

Possible enhancements include:

- Microcontroller-based timing control
- LCD status display
- IoT monitoring
- UV leakage detection
- Multi-object sterilization chamber

---
## Engineering Challenges

### Timer B Incorrect Triggering
Timer B initially stayed active due to a constant LOW signal.

Solution:
A coupling capacitor and pull-up resistor were added to convert the signal into a falling-edge trigger.

### Noise on Trigger Pins
Mechanical bounce from the limit switch caused false triggering.

Solution:
Debounce capacitors and pull-up resistors were added.

### Safety Concerns
Initial prototype lacked reliable UV safety cutoff.

Solution:
A door limit switch was integrated to ensure the UV lamp activates only when the chamber is closed.

---

# Prototype

![Prototype](images/prototype_2.png)

![Prototype](images/prototype_3.png)

---

# Project Report

Full project documentation is available here:

[Project Report](docs/UV_C_Hygiene_Chamber_Project_Report.pdf)

---

# Authors

Pratham Patel  
Harit Patel  

Electronics and Communication Engineering  
Dharmsinh Desai University
