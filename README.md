# Physics-Informed Neural Networks for Implicit Time-Stepping Operators

This repository contains the implementation for the study:

**"Physics-Informed Neural Networks for Learning Implicit Time-Stepping Operators"**

---

## Overview

This work investigates whether neural networks can learn **implicit time-stepping operators** for nonlinear partial differential equations (PDEs), using the inviscid Burgers’ equation as a benchmark problem.

Instead of solving a nonlinear system at each time step using traditional numerical methods (e.g., Newton iterations), we train neural networks to directly approximate the mapping between consecutive time steps.

We compare four training paradigms:

* **Case A — Data-driven:** Supervised learning using solver-generated targets
* **Case B — Physics-only:** Residual minimization without supervision
* **Case C — Hybrid:** Combined data and physics constraints
* **Case D — Hybrid + Newton:** Hybrid model with Newton-based correction

---

## Requirements

Recommended environment:

* Python ≥ 3.9
* TensorFlow ≥ 2.x

Install dependencies:

```bash
pip install numpy scipy tensorflow matplotlib jupyter
```

---

## How to Run

1. Clone the repository:

```bash
git clone https://github.com/rakeshprok/pinn-implicit-operators.git
cd pinn-implicit-operators
```

2. Launch Jupyter Notebook:

```bash
jupyter notebook
```

3. Run the notebooks corresponding to each case:

* `caseA_data_driven.ipynb`
* `caseB_physics_only.ipynb`
* `caseC_hybrid.ipynb`
* `caseD_hybrid_newton.ipynb`

Run all cells sequentially from top to bottom.

---

## Outputs

Each notebook generates:

* Residual metrics (L∞ and mean)
* Solution comparison plots
* Residual visualization
* Multi-step rollout comparisons

These outputs correspond directly to the results reported in the paper.

---

## Reproducibility

* Random seeds are fixed for reproducibility
* All experiments are self-contained within the notebooks
* No external datasets are required
* Results may vary slightly depending on hardware and TensorFlow version

---

## Repository Structure

```
caseA_data_driven.ipynb
caseB_physics_only.ipynb
caseC_hybrid.ipynb
caseD_hybrid_newton.ipynb
README.md
LICENSE
```

---

## License

This project is licensed under the MIT License.

---

## Notes

This repository accompanies a research study on physics-informed learning for implicit numerical methods.
It is intended for academic and research use.

---

## Author

Rakesh Kumar
M.S. Data Science
University of Massachusetts Dartmouth
