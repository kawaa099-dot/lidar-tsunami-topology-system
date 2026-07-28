# LiDAR System for Tsunami Damage Control Topology Mapping

A research and system-design study proposing a UAV-mounted LiDAR photonic system capable of generating high-resolution terrain topologies (±30 cm accuracy) for tsunami flood simulation and evacuation planning.

# Project Overview

Tsunamis are rare but catastrophic — the 2004 Banda Aceh event alone caused ~230,000 deaths — and response windows can be as short as 15 minutes. Accurate terrain topology is essential to simulate flood extent and issue timely evacuation warnings, but pre-LiDAR methods carried multi-meter height errors, too imprecise for reliable simulation.

This study designs a complete photonic LiDAR system — from component-level laser/photodiode selection through circuit-level pulse driver and receiver design — aimed at achieving centimeter-level topology accuracy, mounted on a UAV for rapid aerial deployment to at-risk coastal areas.

# Report Structure

1. **Introduction** — Tsunami risk, motivation for accurate topology mapping, LiDAR vs. RADAR trade-offs
2. **Motivations & Goals** — Target application, point-cloud density requirements, existing UAV-LiDAR systems (e.g. Leica BLK2FLY) as benchmarks
3. **Physical Principles** — Pulse-laser ranging, reflectivity vs. wavelength, atmospheric absorption trade-offs
4. **Photonic System Design** — Component selection: VCSEL laser array, pulse driver, photodiode, optical amplifier; power budget and link analysis
5. **System Implementation** — Full emitter/receiver circuit design (pulse driver, transimpedance receiver), MEMS beam-steering, signal-to-noise ratio calculation
6. **Conclusions & Future Development** — Real-time processing (edge/FPGA), multisensor fusion for weather robustness, cost reduction, autonomous flight path optimization

# Key Design Outcomes

- **Target resolution:** ±30 cm horizontal / ±15 cm vertical (required for reliable tsunami simulation)
- **Laser:** Lumentum M52-100 VCSEL array (905 nm), driven by EPC9179 pulse driver (2–3 ns pulses, 75 A peak current)
- **Photodetector:** Hamamatsu S5971/S5973 Si PIN photodiode (300 ps rise/fall time)
- **Optical amplification:** ThorLabs BOA9305 booster amplifier to recover extremely weak return signal (link budget shows ~3×10⁻¹⁵ transmit-to-receive power ratio)
- **Platform:** CHCNAV X500 UAV (5 kg payload, 50 min flight time, dual-GNSS positioning)
- **Achieved SNR:** ~115 (after bandwidth reduction via transimpedance amplifier tuning)

# Contents

- [`Report_LIDARsystem.pdf`](./Report_LIDARsystem.pdf) — Full report (theory, system design, circuit analysis, calculations, and references)
- [`Presentation_LIDARsystem_tsunamiDamage.pdf`](./Presentation_LIDARsystem_tsunamiDamage.pdf)

# Domain & Methods

- **Domain:** Photonics, optoelectronics, remote sensing, disaster risk mitigation
- **Techniques:** Link budget analysis, pulse-laser ranging (time-of-flight), transimpedance amplifier design, MEMS beam steering, digital surface/elevation modeling (DSM/DEM)

# Future Development

- Real-time onboard processing via edge computing / FPGA for faster warning issuance
- Integration with dynamic tsunami/flood simulation models
- Multisensor fusion (LiDAR + RADAR/thermal) for all-weather reliability
- Cost-effective, open-source hardware alternatives for wider accessibility
- AI-driven autonomous flight path optimization

# Authors

Kawtharul Jannah Mohd Sukki · Nur Ain Afiqah Shabudin
