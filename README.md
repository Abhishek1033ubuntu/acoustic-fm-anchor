# acoustic-fm-anchor


[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.22025466.svg)](https://doi.org/10.5281/zenodo.22025466)
![Status](https://img.shields.io/badge/Status-Research_POC-orange)

---
# Parametric FM Spatial Audio System & Automatic Time-Alignment Matrix

## 1. System Abstract & Physical Architecture
This repository contains the official specification, baseline simulation framework, and cryptographic verification anchor for a high-efficiency spatial sound synthesis system. 

The architecture decouples audio delivery into two specialized mediums:
1. **Low-Frequency Subsystem ($< 200\text{ Hz}$):** A dedicated, physically decoupled subwoofer utilizing room boundary loading for high-efficiency bass reproduction.
2. **Mid-to-High Frequency Subsystem ($200\text{ Hz} - 24\text{ kHz}$):** A micro-electro-mechanical systems (MEMS) ultrasonic transducer array ($40\text{ kHz}$ FM carrier) firing directed acoustic columns that undergo non-linear self-demodulation at wall boundary nodes to form virtual speaker sources.

---

## 2. Dynamic 2-User Couch Profile Physics Simulation (PoC)

To guarantee pristine phase alignment across multi-user sitting profiles, the digital signal processor (DSP) dynamically computes path delays between the corner subwoofer and the wall-reflected parametric beams.

The core physics validation model is maintained separately in [`simulation.py`](./simulation.py).

### How to Run the Simulation
Ensure you have `numpy` installed, then run the script directly from your terminal:

```bash
python simulation.py
