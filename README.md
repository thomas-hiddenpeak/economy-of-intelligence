# The Economy of Intelligence

**Decoding Holographic Information and the Emergence of Homomorphic World Models under Resource Constraints**

*智能的经济学：资源受限下的全息信息解码与世界模型涌现*

**Author:** Yunfeng Tang &nbsp;|&nbsp; **Date:** February 2026

> **Paper:** The full paper will be published on [arXiv](https://arxiv.org/) — link forthcoming.

---

## Overview

This repository provides the **complete experimental code, reports, and figures** for the paper *"The Economy of Intelligence"*.

We propose a theoretical framework proving that **general intelligence is not the product of design, but the inevitable outcome of holographic noise and finite resources**. Using metric entropy and approximation theory, we show that under the holographic limit ($d \to \infty$), any mimicry strategy that memorizes noise encounters a curse of dimensionality, violating physical resource constraints. Constructing a **homomorphic world model** becomes the only economically feasible solution.

### Key Results

- **Resource boundary phase transition** at intrinsic dimension $k_{\text{eff}}$ (paired t-test $p < 10^{-8}$, Cohen's $d > 3.0$)
- **Rank collapse** of effective rank toward $k_{\text{eff}}$ under over-parameterization
- **Architecture invariance** confirmed across MLP and Transformer ($|\Delta \text{ER}| = 0.01$)
- **Dimension independence** — homomorphic advantage increases monotonically with observation dimension $d$
- **Cross-system generality** validated on both Lorenz and Rössler chaotic attractors
- **10/10 experiments passed** across 506 training jobs, independently verified on two hardware platforms

---

## Repository Structure

```
├── README.md                          # This file
├── requirements.txt                   # Python dependencies
├── holographic_experiments.ipynb      # Core experiments (Exp 1–5)
├── extended_experiments.ipynb         # Extended experiments (Exp 6–7, S1–S3)
├── future_experiments.ipynb           # Exploratory / future-direction experiments
├── 实验报告.md                         # Full experiment report (Chinese)
└── figures/                           # All generated figures
    ├── exp1_resource_boundary.png
    ├── exp2_rank_collapse.png
    ├── exp3_noise_invariance.png
    ├── exp4_dimension_independence.png
    ├── exp5_rossler.png
    ├── future_f1_architecture.png
    ├── future_f1_svd_evolution.png
    ├── future_f2_*.png
    ├── future_f3_*.png
    ├── future_f4_*.png
    └── future_f5_*.png
```

---

## Experiments

All experiments use synthetic holographic observations generated from chaotic attractors:

$$x = As + \xi, \quad A \in \mathbb{R}^{d \times k},\; \xi \sim \mathcal{N}(0, \sigma_\xi^2 I_d)$$

| Experiment | Section | Core Validation | Scale | Result |
|:----------:|:-------:|-----------------|:-----:|:------:|
| **Exp 1** | §5.2 | Resource boundary phase transition | 35 jobs | ✓ PASS |
| **Exp 2** | §5.3 | Rank collapse dynamics | 28 jobs | ✓ PASS |
| **Exp 3** | §5.4 | Tool AI vs. Holographic AI | 14 jobs | ✓ PASS |
| **Exp 4** | §5.5 | Dimension independence | 18 jobs | ✓ PASS |
| **Exp 5** | §5.6 | Rössler system generalization | 15 jobs | ✓ PASS |
| **Exp 6** | §5.8.1 | Architecture invariance (MLP vs Transformer) | 50 jobs | ✓ PASS |
| **Exp 7** | §5.8.2 | i.i.d. noise assumption boundary | 99 jobs | ✓ PASS |
| **S1** | Supp. | Rank collapse existence + λ dependency | 63 jobs | ✓ PASS |
| **S2** | Supp. | Continuous-time generalization (MLP vs Neural ODE) | 50 jobs | ✓ PASS |
| **S3** | Supp. | Transformer structural compression ablation | 50 jobs | ✓ PASS |

---

## Reproducibility

All 10 experiments have been independently verified on **two separate hardware environments** with consistent results:

| | Environment A | Environment B |
|---|---|---|
| **Hardware** | Dual NVIDIA RTX A6000 NVLink (48 GB × 2) | RM-01 Portable AI Supercomputer (Blackwell iGPU 128 GB) |
| **Python** | 3.12 | 3.12 |
| **PyTorch** | 2.10.0+cu128 | 2.10.0 |
| **CUDA** | 12.8 | 13.0 |

---

## Getting Started

### Prerequisites

- Python ≥ 3.10
- PyTorch ≥ 2.0.0 (CUDA recommended)

### Installation

```bash
git clone https://github.com/thomas-hiddenpeak/economy-of-intelligence.git
cd economy-of-intelligence
pip install -r requirements.txt
```

### Running the Experiments

Open the notebooks in Jupyter and run all cells sequentially:

```bash
jupyter notebook holographic_experiments.ipynb      # Core experiments (Exp 1–5, ~47 min on A6000)
jupyter notebook extended_experiments.ipynb         # Extended experiments (Exp 6–7, S1–S3, ~2 h on A6000)
```

> **Note:** Runtime estimates are based on dual RTX A6000. Actual times may vary depending on hardware.

---

## Citation

If you find this work useful, please cite:

```bibtex
@article{tang2026economy,
  title   = {The Economy of Intelligence: Decoding Holographic Information and the Emergence of Homomorphic World Models under Resource Constraints},
  author  = {Tang, Yunfeng},
  year    = {2026},
  note    = {Preprint available on arXiv (forthcoming)}
}
```

---

## License

This project is released under the [MIT License](LICENSE).

---

## Acknowledgments

The author would like to thank **Jie Zhu (朱杰)**, **Yi Shi (石一)**, and **Zijing Xu (徐子景)**, co-founders of **Hiddenpeak Inc.**, and **Remy**, Board Secretary of **Hiddenpeak Inc.**, for their steadfast support throughout this research. Their assistance in shielding the author from external distractions was invaluable, allowing full concentration on the research and experiments.

Experimental verification was performed on dual NVIDIA RTX A6000 and RM-01 portable AI supercomputer platforms.
