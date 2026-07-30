# AuraMEMS-Thruster1# Toroidal MEMS Electrospray Thruster Array Simulation
**Advanced Solid-State Space Propulsion Architecture**
**Intellectual Property of: Mohamed Talal Kadri (C) 2026. All Rights Reserved. Patent Pending.**

## Official Warning
Unauthorized copying, reproduction, or use of this solid-state micro-propulsion architecture without express written permission is strictly prohibited and subject to legal action under international patent laws.

## Overview
This high-fidelity simulation models an advanced solid-state electrospray thruster array arranged in a 3D toroidal ring configuration. The system leverages pure iodine propellant operating via thermal sublimation. 

### Advanced Material Architecture
To withstand the highly corrosive nature of iodine gas ($I_2$) and reactive iodine ions, the system features a robust, physically validated multi-layer material protection scheme:
* **Structural Substrate Core:** Aluminum-Magnesium Alloy (Al-Mg) providing excellent mechanical rigidity and thermal conductivity.
* **Passivation Dielectric Layer:** Silicon Dioxide ($SiO_2$) deposited via Atomic Layer Deposition (ALD) with a precise nanometric thickness of 15.0 nm.
* **Chemical Protection Mechanism:** This ultra-conformal $SiO_2$ layer functions as an anti-corrosive, high-dielectric barrier. It completely isolates the Al-Mg metallic core and the inner silicon capillary micro-needle emitters from direct chemical contact with the iodine vapor, preventing any chemical reactions, structural degradation, or electrical breakdown.

## Features
* **Stiff EHD Differential Solver:** Utilizes an implicit Radau IIA integration scheme to resolve severe localized electric field gradients at the emitter tips.
* **Toroidal Array Geometry:** Arranges 5,000 emitters uniformly over a three-dimensional torus to provide gimbal-less, multi-axis vectoring control.
* **Electrostatic Crosstalk Mitigation:** Dynamically computes field reduction penalties caused by neighboring emitter proximity using an analytical electrostatic superposition model.
* **Hertz-Knudsen Sublimation Model:** Simulates vapor mass transport of solid iodine at an 80°C thermal setpoint.

## Usage
Ensure you have `numpy` and `scipy` installed:
```bash
pip install numpy scipy
```
Run the high-fidelity simulation script:
```bash## Appendix: Mitigation Strategies for Physical Hardware Implementation

To transition this high-fidelity simulation into a physical micro-propulsion prototype, the following engineering mitigations are proposed to address known micro-scale phenomena:

1. **Sputtering & Dielectric Erosion Mitigation:**
   - *Issue:* The 15 nm $SiO_2$ layer may undergo ion-bombardment degradation over extended operational lifespans.
   - *Solution:* Implement a multi-layer atomic layer deposition (ALD) heterostructure ($Al_2O_3$ / $SiO_2$) or a Diamond-Like Carbon (DLC) coating to absorb high-energy ion impacts without degrading the core substrate.

2. **Propellant Condensation & Capillary Clogging:**
   - *Issue:* Cold spots within the micro-channels could trigger solid iodine resublimation.
   - *Solution:* Integrate a micro-machined active thermal gradient (95°C at the emitter tips vs. 80°C at the sublimator tank) using on-chip platinum (Pt) micro-heaters.

3. **Voltage & Power Optimization:**
   - *Issue:* High extraction voltages strain small-satellite power systems.
   - *Solution:* Optimize emitter tip curvature radii to sub-micron scales to maximize local electric field gradients, combined with high-efficiency Piezoelectric Transformers (PTs)
python toroidal_mems_thruster.py
```
## License & Intellectual Property

Copyright (c) 2026 Mohamed Talal Kadri. All Rights Reserved. 
This architecture and simulator are protected under strict non-commercial terms. Please refer to the [LICENSE](LICENSE) file for full legal details regarding evaluation and usage permissions.
"The source code is strictly proprietary and maintained in a private repository for patent protection. Access for academic review or clinical validation can be requested via email or GitHub collaboration."
