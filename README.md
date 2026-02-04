# RoBeG: A Knowledge-Driven and Geometrically Constrained Generative Framework for Robust End-to-End Autonomous Driving

<div align="center">

[![Paper](https://img.shields.io/badge/Paper-arXiv-b31b1b.svg)](http://arxiv.org/) &nbsp;
[![Conference](https://img.shields.io/badge/Target-TR__C-4b44ce.svg)](https://www.journals.elsevier.com/transportation-research-part-c-emerging-technologies) &nbsp;
[![NavSim](https://img.shields.io/badge/Benchmark-NavSim-brightgreen)](https://github.com/autonomousvision/navsim) &nbsp;  
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](LICENSE)

**Rui Zhao**$^{1}$, **Ziguo Chen**$^{2}$, ...

$^{1}$[College of Automotive Engineering, Jilin University], $^{2}$[College of Automotive Engineering, Jilin University]

</div>

## 📢 Abstract
While end-to-end autonomous driving holds compelling promise, its robustness is often compromised by temporal feature drift and geometric discontinuity. We present **RoBeG**, a robust perception and generative planning framework. 
1.  **Anti-Drift Perception**: A **Short-Term Error Truncation (STET)** mechanism acts as a temporal firewall against cumulative localization noise.
2.  **Bezier Planning**: A probabilistic head on **Bezier Manifolds** guarantees kinematic feasibility and smoothness.
3.  **Semantic Alignment**: A **Flow-Enhanced Prior** aligned with expert knowledge via contrastive learning ensures generalization.

Extensive experiments on **NavSim** demonstrate that RoBeG achieves state-of-the-art performance (**86.8 EPDMS**), significantly outperforming existing methods in planning accuracy and robustness against severe localization noise.

---

## ✨ Qualitative Results

### 1. Robustness under Severe Noise
Even under severe localization noise ($\sigma_{pos}=1.0m, \sigma_{rot}=1.0^\circ$), RoBeG maintains stable feature representations and safe planning, whereas baselines often suffer from feature drift.

![Robustness](image/robustness_vis_selected.png)
*(Replace with your Figure 8 or the selected robustness comparison)*

### 2. Diverse Driving Scenarios
RoBeG generates smooth, human-like, and rule-compliant trajectories across diverse scenarios, including complex intersections, dense traffic, and geometric maneuvers.

![Qualitative](image/eval.png)
*(Replace with your Figure 5 - the 5-column qualitative result)*

---

## 🏆 State-of-the-Art Performance

We validate RoBeG on the challenging **NavSim** benchmark.

| Method | Sensors | PDMS (v1) $\uparrow$ | **EPDMS (v2)** $\uparrow$ |
| :--- | :---: | :---: | :---: |
| TransFuser | C+L | 84.0 | 76.7 |
| HydraMDP++ | C+L | 86.5 | 81.4 |
| DriveSuprem | C | - | 83.1 |
| DiffusionDrive | C | 84.5 | 84.5 |
| **RoBeG (Ours)** | **C** | **87.9** | **86.8** |

> **Note**: RoBeG (Camera-only) outperforms both Camera-based and LiDAR-based SOTA methods.

---

## 🛠️ Roadmap

- [ ] Release inference code and model definition.
- [ ] Release pretrained weights (RoBeG-Base & RoBeG-Tiny).
- [ ] Release training scripts and configuration files.
- [ ] Provide a tutorial for running on custom data.
