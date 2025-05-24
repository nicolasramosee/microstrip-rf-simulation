# Microstrip RF Interconnect Simulation Using `scikit-rf`

**Author**: Nicolas Ramos  
**Tools**: Python, `scikit-rf`, `matplotlib`, `numpy`, Jupyter Notebook

## Overview

This project models a high-frequency PCB interconnect using a symmetric transmission line with a central open-circuited stub. The simulation is implemented in Python using the [`scikit-rf`](https://scikit-rf.readthedocs.io/en/latest/) library and visualized in a Jupyter Notebook. 

The design reflects the behavior of **lossless microstrip traces**, commonly found in RF and microwave PCB layouts. The project explores **S-parameter analysis** across a 1–10 GHz frequency sweep to evaluate return loss, insertion loss, and the effectiveness of the stub as an impedance tuning element.

---

## Goals

- Simulate a high-frequency transmission line with a center-mounted open stub.
- Analyze how stub length affects impedance matching across frequency.
- Interpret return loss and insertion loss using S-parameter plots.
- Demonstrate symmetry and reciprocity in a matched passive network.

---

## System Description

The simulated system consists of:
- Two 1.5 cm transmission line segments
- One 1 cm open-circuited stub (shunt branch)
- An ideal 3-port T-junction
- A synthetic lossless transmission medium using a custom-defined propagation constant

The model is not geometry-specific, but abstracted to behave similarly to a **microstrip transmission line**.

---

## Results Summary

- **S-parameter sweep**: 1 to 10 GHz (201 points)
- **Best match**: ~1.00 GHz, where return loss reaches –30 dB
- **Network symmetry**:
  - S11 = S22 (input/output reflections)
  - S21 = S12 (forward/reverse transmission)
- **Return loss** increases with frequency as the stub contributes increasing mismatch outside its design point

---

## Key Outputs

![Example S-parameter plot](/Users/nicol/Desktop/Screenshot 2025-05-24 at 3.24.22 AM.png) 

- **S11 / S22**: Input/output return loss (reflection)
- **S21 / S12**: Insertion loss and reverse transmission
- Visual confirmation of minimal reflection at matched frequency and symmetry across ports

---

## Conclusion
This simulation demonstrates foundational concepts in RF PCB modeling, including transmission line behavior, impedance matching, and S-parameter analysis. It highlights the practical impact of discontinuities like stubs in signal reflection and shows how symmetry and reciprocity influence network performance. The approach provides a lightweight, flexible way to explore high-frequency behavior in planar interconnects using Python.

---

## Contact
Feel free to connect or reach out if you’d like to collaborate or ask questions!
Nicolas Ramos
Electrical Engineering Student – University of Miami
- Email: nmree25@gmail.com
- Mobile: (786) 380-1981
- LinkedIn: www.linkedin.com/in/nicolas-ramos-503056344
