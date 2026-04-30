<div align="center">

# 🌬️ Adaptive Control of Wind Turbine System

### MATLAB/Simulink wind turbine control model using fuzzy self-tuning PID gain adjustment

![MATLAB](https://img.shields.io/badge/MATLAB-Simulink-orange?style=for-the-badge&logo=mathworks)
![Fuzzy Logic](https://img.shields.io/badge/Fuzzy%20Logic-Control-blueviolet?style=for-the-badge)
![Control Systems](https://img.shields.io/badge/Control%20Systems-Wind%20Turbine-success?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge)

</div>

---

## 📌 Overview

This project presents the **modeling, simulation, and control of a wind turbine system** using **MATLAB/Simulink**.  
The main goal is to improve the dynamic response of the turbine by applying an **adaptive fuzzy PID control strategy**, where the PID parameters are tuned through fuzzy inference systems.

The repository includes:

- A complete **Simulink wind turbine control model**
- Separate fuzzy inference system files for **Kp**, **Ki**, and **Kd**
- A final project report in PDF format
- A presentation file summarizing the project

---

## 🎯 Project Objective

Wind turbine systems are nonlinear and strongly affected by changing wind conditions.  
A fixed-parameter PID controller may not always provide an optimal response under different operating points.

This project focuses on designing a controller that can:

- Regulate the wind turbine system response
- Improve stability and transient performance
- Adapt controller gains based on error behavior
- Reduce overshoot and improve settling behavior
- Demonstrate the control strategy through MATLAB/Simulink simulation

---

## 🧠 Control Strategy

The control architecture is based on a **fuzzy self-tuning PID controller**.

Instead of using fixed PID values, the controller adjusts:

| Gain | Purpose |
|---|---|
| `Kp` | Improves response speed and reduces error |
| `Ki` | Reduces steady-state error |
| `Kd` | Improves damping and reduces overshoot |

The fuzzy controller uses two main inputs:

| Input | Meaning |
|---|---|
| `e` | Error signal |
| `ec` | Change of error |

Each fuzzy inference system uses linguistic membership functions such as:

- `NB` — Negative Big
- `NM` — Negative Medium
- `NS` — Negative Small
- `ZO` — Zero
- `PS` — Positive Small
- `PM` — Positive Medium
- `PB` — Positive Big

The output of each fuzzy inference system determines the corresponding PID gain adjustment.

---

## ⚙️ Main Components

### 1. Wind Turbine Simulation Model

The file `windTurbinSimulationController.slx` contains the Simulink model used to simulate the wind turbine system and its controller.

It represents the main environment where the turbine dynamics, controller blocks, and system response are evaluated.

### 2. Fuzzy PID Gain Tuning

The fuzzy inference files are used to tune the PID controller gains:

- `kp.fis` → proportional gain tuning
- `ki.fis` → integral gain tuning
- `kd.fis` → derivative gain tuning

Each `.fis` file is implemented as a **Mamdani fuzzy inference system** with:

- 2 inputs: error and change of error
- 1 output: corresponding PID gain
- 49 fuzzy rules
- Gaussian membership functions
- Centroid defuzzification

### 3. Report and Presentation

The project also includes documentation files:

- `windTurbine_final.pdf` — detailed final report
- `Wind_Turbine_final.pptx` — presentation slides

These files summarize the modeling process, controller design, simulation setup, and final results.

---

## 📊 Expected Simulation Outputs

Depending on the model configuration, the simulation can be used to analyze:

- Wind turbine output response
- Error and change of error behavior
- Controller gain adaptation
- Dynamic response improvement
- Overshoot and settling-time behavior
- Stability of the controlled system

---

## 🧩 Why Fuzzy PID Control?

A classical PID controller is simple and effective, but its performance depends heavily on fixed gain values.  
For nonlinear systems such as wind turbines, fixed gains may not perform well under all conditions.

Fuzzy PID control provides an adaptive solution by using rule-based reasoning to tune the controller gains according to the system behavior.

### Advantages

- Better adaptability to nonlinear dynamics
- Reduced need for manual PID tuning
- Improved transient response
- Better disturbance handling
- Suitable for simulation-based renewable energy control studies

---

## 📚 Learning Outcomes

Through this project, the following topics are demonstrated:

- Wind turbine system modeling
- Feedback control design
- PID controller tuning
- Fuzzy logic control
- Mamdani fuzzy inference systems
- MATLAB/Simulink simulation workflow
- Renewable energy control system analysis

---

## 👨‍💻 Author

**Mohammad Barabadi**  
GitHub: [@mohammadbrd](https://github.com/mohammadbrd)

---

## 📄 License

This repository does not currently specify a license.  
If you plan to reuse or distribute this project, please add an appropriate open-source license.

---

<div align="center">

### ⭐ If this project was useful, consider giving the repository a star!

</div>
