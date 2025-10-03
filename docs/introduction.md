# 🧭 Introduction to Ballistic Missile Guidance, Navigation, and Control (GNC)

## 1. Overview

A **ballistic missile** is a weapon system that follows a **predetermined ballistic trajectory** after an initial powered boost phase. Once the propulsion phase ends, the missile coasts under the influence of gravity and atmospheric forces until it reaches its target. Achieving **accuracy**, **stability**, and **reliability** in this process requires a sophisticated **Guidance, Navigation, and Control (GNC)** system.

The **GNC system** ensures that the missile:
- **Follows the desired trajectory**
- **Maintains stable flight**
- **Reaches the intended target** with high precision

This documentation introduces the principles, architecture, and mathematical models of a **Ballistic Missile GNC system**.

---

## 2. What is GNC?

The **GNC** system is a crucial subsystem in any aerospace vehicle (missile, rocket, spacecraft). It is composed of three tightly coupled elements:

| Component | Function |
|-----------|-----------|
| **Guidance** | Determines the desired path to reach the target. |
| **Navigation** | Estimates the missile’s current position, velocity, and attitude. |
| **Control** | Generates actuator commands (e.g., fin deflections) to follow the guidance commands. |

Together, these elements ensure the missile remains on the correct flight path despite disturbances like atmospheric drag, wind, and model uncertainties.

---

## 3. Phases of Missile Flight

A typical **ballistic missile trajectory** is divided into three main phases:

1. **Boost Phase**  
   - Powered flight using rocket propulsion  
   - GNC commands thrust vectoring and attitude control  
   - Objective: achieve correct velocity and orientation for trajectory insertion

2. **Midcourse Phase**  
   - Unpowered flight (coasting) outside dense atmosphere  
   - Guidance updates trajectory if navigation data available (e.g., via INS/GPS)  
   - Control maintains stability and correct attitude

3. **Terminal Phase**  
   - Re-entry into atmosphere  
   - High aerodynamic forces  
   - Final guidance adjustments for precision targeting

---
## 4. Importance of GNC in Ballistic Missiles

Without an accurate GNC system, a missile can **miss the target by kilometers** due to small initial errors. The GNC system must:
- Minimize trajectory errors
- Ensure attitude stability
- Handle uncertainties and external disturbances
- Optimize fuel and control effort


+-----------------+ +------------------+ +------------------+
| Guidance Law | ---> | Control System | ---> | Missile Dynamics |
+-----------------+ +------------------+ +------------------+
↑ | |
| ↓ ↓
| Actuator Commands Position/Velocity
| Feedback
+-----------------+------------------+------------------+
↑
Navigation System
(INS / GPS Sensors)



This repository aims to:

- Model the **missile dynamics** (3-DOF and 6-DOF)
- Implement **guidance laws** (e.g., Proportional Navigation)
- Simulate **navigation systems** (INS, GPS)
- Design **control laws** (PID / LQR)
- Combine all into a **full GNC simulation**
- Document the **mathematical background** and **simulation results**