# Reproduction of Quantum Optics Papers from Changchun Universities

## 📖 Project Overview
This repository contains the reproduction code for **two research papers** from **Prof. Xuexi Yi's Group** (Northeast Normal University), focusing on open quantum systems and quantum feedback control.

All simulations are implemented in **Python** using the **QuTiP** library.

---

## 📑 Project 1: Emergent Non-Markovian Gain
**Target Paper:**
> **Title:** Emergent Non-Markovian Gain in Open Quantum Systems
> **Authors:** H. Z. Shen, Cheng Shang, Yan-Hui Zhou, X. X. Yi*
> **Reference:** arXiv:2503.21739 (2025)

In this project, I reproduced the exact non-Markovian dynamics (CRW) and compared them with the standard Markovian approximation (RWA) to highlight the unique "Emergent Gain" phenomenon reported in the paper.

### 📊 1. Population Dynamics (Figure 2)
Comparison of the amplitude $|\mathcal{U}(t)|$ evolution.

| **Exact Model (CRW)** | **Markovian Approx. (RWA)** |
|:---:|:---:|
| <img src="https://raw.githubusercontent.com/2287584788lty-create/Reproduction-of-Quantum-Optics-papers-from-Changchun-universities-using-QuTiP/main/Quantum_Reproduction/1/fig2_exact.png" width="400" alt="Fig2 Exact"/> | <img src="https://raw.githubusercontent.com/2287584788lty-create/Reproduction-of-Quantum-Optics-papers-from-Changchun-universities-using-QuTiP/main/Quantum_Reproduction/1/fig2_rwa.png" width="400" alt="Fig2 RWA"/> |
| *Reproduction of Fig. 2(a)* | *Simulation under RWA* |

> **Observation:** The exact model (Left) shows **population trapping** and gain ($>1$), verifying the formation of bound states. The RWA (Right) falsely predicts a monotonic decay to zero.

### 📉 2. Decay Rate Analysis (Figure 3)
Comparison of the time-dependent decay rate $\gamma_1(t)$.

| **Exact Model (CRW)** | **Markovian Approx. (RWA)** |
|:---:|:---:|
| <img src="https://raw.githubusercontent.com/2287584788lty-create/Reproduction-of-Quantum-Optics-papers-from-Changchun-universities-using-QuTiP/main/Quantum_Reproduction/1/fig3_exact.png" width="400" alt="Fig3 Exact"/> | <img src="https://raw.githubusercontent.com/2287584788lty-create/Reproduction-of-Quantum-Optics-papers-from-Changchun-universities-using-QuTiP/main/Quantum_Reproduction/1/fig3_rwa.png" width="400" alt="Fig3 RWA"/> |
| *Reproduction of Fig. 3(a)* | *Simulation under RWA* |

> **Observation:** The exact decay rate oscillates and becomes **negative** (Left), indicating information backflow. The RWA prediction (Right) remains positive and constant.

---

## 📑 Project 2: Dissipative Entanglement Preparation
**Target Paper:**
> **Title:** Dissipative preparation of tripartite singlet state in coupled arrays of cavities via quantum feedback control
> **Authors:** Xiao-Qiang Shao, Z. H. Wang, Hao-Di Liu, X. X. Yi*
> **Reference:** *Phys. Rev. A* 94, 032307 (2016)
》**introduction:** The primary goal of this paper is to prepare a specific tripartite entangled state, known as the tripartite singlet state, in a robust and deterministic manner.
I simulated the quantum feedback master equation to prepare the tripartite singlet state $|S_3\rangle$, investigating robustness against detection inefficiency ($\eta$).

### 📊 1. Robustness against Detection Efficiency
Comparison of fidelity evolution under Non-local vs. Local feedback.

<div align="center">
  <img src="https://raw.githubusercontent.com/2287584788lty-create/Reproduction-of-Quantum-Optics-papers-from-Changchun-universities-using-QuTiP/main/Quantum_Reproduction/2/paper2_grid.png" width="800" alt="Fidelity Grid"/>
  <br>
  <em>Fig: Fidelity evolution for Non-local (Top) and Local (Bottom) feedback with $\eta=1.0$ (Left) and $\eta=0.5$ (Right).</em>
</div>

> **Observation:** The scheme successfully prepares the target state ($F \to 1$). Even with lower detection efficiency ($\eta=0.5$), the system remains robust.

### 📉 2. Strategy Comparison
<div align="center">
  <img src="https://raw.githubusercontent.com/2287584788lty-create/Reproduction-of-Quantum-Optics-papers-from-Changchun-universities-using-QuTiP/main/Quantum_Reproduction/2/paper2_compare.png" width="600" alt="Strategy Comparison"/>
  <br>
  <em>Fig: Effective Non-local vs. Local Feedback.</em>
</div>

> **Observation:** Non-local feedback (Blue) generally converges faster than local feedback (Green) under optimized conditions.

---

## 🛠️ Environment & Dependencies
*   **Python**: 3.12.9
*   **QuTiP**: 5.2.2
*   **SciPy** ：1.16.3


## 🧑‍💻 Author
*   **Name:** [noname9612[
*   **Note:** This project is for educational purposes and internship application.
