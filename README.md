# Design and PID Control of a Stacked Interleaved Buck Converter for Green Hydrogen Production

This repository contains the MATLAB/Simulink models, simulation scripts, and technical documentation developed for the research project:

**“Diseño y control PID de un convertidor Stacked Interleaved Buck para la producción de hidrógeno verde”**

## 📝 Project Overview
This project focuses on the development of a high-performance power electronics stage to interface renewable energy sources with an alkaline/PEM electrolyzer. The core of the system is a **Stacked Interleaved Buck Converter (SIBC)**, designed to provide high currents with extremely low ripple to extend the electrolyzer's operational lifespan.

The repository includes a comparative analysis between a simplified **equivalent electrical model** and a high-fidelity **physicochemical model** to validate the robustness of the PID control strategy.

## 💻 System Requirements
* **MATLAB/Simulink:** Version R2021a or later
* **Toolboxes:** Simscape™, Control System Toolbox™
* **Operating System:** Windows 10/11 (64-bit)

## 🚀 Key Features
* **SIBC Topology:** Two-phase interleaved configuration achieving a current ripple of **2.25%**, surpassing the 5% design requirement.
* **PID Control:** Optimized current-loop regulation ($K_p = 7.85$, $K_i = 261.8$) for precise tracking of variable references.
* **Dual Modeling Approach:**
    * **Electrical Model:** RC network emulating double-layer capacitance and activation dynamics.
    * **Physicochemical Model:** Integration of Nernst potential, Butler-Volmer kinetics, Ohmic losses, and Faraday's Law.

## 🛠 Simulation Flow
1. **Initialization:** Load component parameters ($L = 299.6 \mu H$, $C = 21.55 \mu F$) and electrolyzer constants.
2. **Input:** Variable current reference profile (0–40 A) simulating renewable energy intermittency.
3. **Power Stage:** SIBC operation with $180^\circ$ phase-shifting between inductors.
4. **Electrochemical Response:** Calculation of cell voltage ($V_{cell}$) and hydrogen flow rate ($L/min$).
5. **Visualization:** Comparative plots of current ripple, voltage stability, and $H_2$ yield.

## 📊 Main Results
* **Current Stability:** The SIBC effectively minimizes harmonic content, ensuring membrane integrity.
* **Production Rate:** Stable hydrogen production reaching up to **1.5 L/min** at nominal current (40 A).
* **Control Robustness:** Zero steady-state error and minimal settling time during abrupt setpoint changes.

## 📄 License
This project is licensed under the **Creative Commons Attribution 4.0 International (CC BY 4.0)**.
