# Modular Hypercar Aero Package // Digital Twin Pro v7.0

**By** : SAMUELSON G

![Version](https://img.shields.io/badge/Version-7.0.0--LMH-e74c3c?style=for-the-badge)
[![Tech](https://img.shields.io/badge/Tech-Three.js%20%7C%20WebGL-00d2ff?style=for-the-badge)](https://samuelson777.github.io/hypercar-aero-digital-twin/)
[![License](https://img.shields.io/badge/License-MIT-2ecc71?style=for-the-badge)](https://github.com/Samuelson777/hypercar-aero-digital-twin/blob/main/LICENSE)

A browser-based, high-performance digital twin simulating FIA WEC Le Mans Hypercar (LMH) aerodynamics. Built natively in HTML, JavaScript, and Three.js, this application shifts aerodynamic analysis from static, resource-heavy offline solvers into an accessible, real-time visual format.

## Core Architecture & Features

* **Real-Time Physics Solver:** Live telemetry calculating Dynamic Pressure ($q = \frac{1}{2} \rho v^2$), Aerodynamic Downforce ($F_z$), Drag ($F_x$), and Power Loss based on inlet velocity ($v_{\infty}$).
* **Active Aerodynamics (DRS):** Multi-element rear wing assembly with hydraulic kinematic motion that actively reduces total profile drag and modifies the front/rear aero balance.
* **Surfacing Diagnostics:** 
  * Dynamic Pressure Coefficient ($C_p$) scalar mapping to visualize stagnation and suction zones.
  * Curvature Zebra striping for G2 continuity audits.
  * X-Ray topology and wireframe mesh modes.
* **Particle Streamline CFD:** Real-time fluid dynamic visualization using particle velocity integration bounded by the chassis geometry.
* **Procedural Materials:** Custom Canvas API-generated procedural twill carbon fiber weaving and OEM spec automotive paint rendering.
* **Velocity-Synced Kinematics:** Wheel angular rotation ($\omega = \frac{v}{r}$) and ground plane mapping locked directly to the real-time velocity slider.

## Installation & Usage

This project requires zero build steps, bundlers, or dependencies. It is a fully self-contained HTML application.

1. Clone the repository or download the `index.html` file.
2. Open `index.html` in any modern WebGL-compatible browser (Chrome, Edge, Firefox, Safari).
3. **Controls:**
   * **Left Click & Drag:** Orbit camera.
   * **Scroll Wheel:** Zoom in/out.
   * **Right Click & Drag:** Pan camera.
   * **H Key:** Toggle the UI/HUD.

## Conclusion

The Modular Hypercar Aero Package successfully demonstrates the convergence of automotive engineering and real-time web technologies. By leveraging WebGL and procedural geometry, the project transitions aerodynamic analysis into an interactive and immediate visual format. 

The integration of real-world fluid dynamics equations bridges the gap between simple 3D visualization and true digital twin simulation. Furthermore, the inclusion of LMH-compliant parameters, active DRS kinematics, and diagnostic surfacing tools proves that high-fidelity aerospace-grade diagnostics can be engineered natively for the browser. This application serves as a robust foundational framework for rapid prototyping, aerodynamic education, and real-time automotive design reviews.

## Future Enhancements

To elevate the simulation from a conceptual digital twin to a highly accurate engineering tool, the following enhancements are mapped for future iterations:

* **WebGPU-Accelerated Navier-Stokes Solver:** Migrate from standard WebGL to WebGPU compute shaders to run a real-time, grid-based Eulerian fluid simulation. This will allow for accurate representations of turbulent wakes, vortex shedding, and precise boundary layer separation.
* **Dynamic Aero Mapping (Ride Height & Rake):** Introduce suspension kinematics to adjust front and rear ride heights (rake angle). The telemetry engine will dynamically calculate shifts in the center of pressure (CoP) and ground-effect downforce, simulating conditions like porpoising.
* **Modular Component Swapping & Delta Tracking:** Implement a UI system to swap physical aerodynamic components (e.g., high-downforce dive planes vs. low-drag canards). The dashboard will record and display performance deltas (changes in L/D ratio and Aero Balance) between setups.
* **Thermal Flow Diagnostics:** Add thermodynamic particle systems to simulate heat extraction from radiator louvers and brake ducts, visualizing the thermal degradation of aerodynamic efficiency when hot air is rejected over the chassis.
* **WebXR (Virtual Reality) Integration:** Implement WebXR API support, allowing engineers to step into a 1:1 scale virtual wind tunnel to physically inspect Class-A surfacing and walk through CFD streamlines.
* **Session Data Logging & Export:** Build a data-logging module to record telemetry matrices across varying velocities and DRS states, allowing CSV/JSON exports for external ingestion into professional lap-time simulation software (e.g., Bosch LapSim).

## License

This project is licensed under the MIT License. See the [LICENSE](https://github.com/Samuelson777/hypercar-aero-digital-twin/blob/main/LICENSE) file for details.
