# Comparative Study: Beta vs. Gamma Distributions

> **Statistical Learning & Data Analysis Assignment**  
> *Università degli Studi di Napoli Federico II*  
> **Author:** Ammar Gharaf  
> **Supervisors:** Prof. Roberta Siciliano, Prof. Emiliano Del Gobbo

---

### Tech Stack & Tools

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![SciPy](https://img.shields.io/badge/SciPy-8CAAE6?style=for-the-badge&logo=scipy&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557c?style=for-the-badge&logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)

---

## Overview

This repository explores the mathematical structures, parametric behaviors, empirical simulations, and real-world applications of the **Beta** and **Gamma** probability distributions. Additionally, it analyzes their convergence to the **Gaussian (Normal)** distribution under Central Limit Theorem (CLT) conditions.

---

## Theoretical Summary

| Property | Beta Distribution | Gamma Distribution |
| :--- | :--- | :--- |
| **Support** | Bounded: **x in [0, 1]** | Positive Unbounded: **y in (0, ∞)** |
| **Parameters** | Shape parameters **α > 0**, **β > 0** | Shape **k > 0**, Scale **θ > 0** |
| **Mean E[X]** | **α / (α + β)** | **k * θ** |
| **Variance Var(X)** | **(α * β) / ((α + β)^2 * (α + β + 1))** | **k * θ^2** |
| **Gaussian Limit** | As **α, β → ∞** with **α = β** | As **k → ∞** |

---

## Empirical Simulation (N = 1000)

Empirical validations were conducted to confirm consistency with the Law of Large Numbers:

* **Beta Distribution (α = 2, β = 5)**:
  * **Sample Mean:** `0.29` | **Theoretical Mean:** `0.29`
  * **Sample Variance:** `0.0241` | **Theoretical Variance:** `0.0255`

* **Gamma Distribution (k = 2, θ = 2)**:
  * **Sample Mean:** `3.92` | **Theoretical Mean:** `4.00`
  * **Sample Variance:** `7.33` | **Theoretical Variance:** `8.00`

---

## Real-World Application Scenario

The study analyzes user behavior metrics on a digital advertising platform:

1. **Conversion Rate — Beta(α = 2, β = 5)**: Bounded proportion modeling user click conversion rates, reflecting low average conversions with a heavy skew toward non-converters.
2. **Time Until Purchase — Gamma(k = 2, θ = 3)**: Unbounded continuous duration modeling time elapsed between initial click and completed order.

---

## Setup & Execution

```bash
# Clone the repository
git clone [https://github.com/your-username/beta-vs-gamma-statistical-analysis.git](https://github.com/your-username/beta-vs-gamma-statistical-analysis.git)

# Navigate to directory
cd beta-vs-gamma-statistical-analysis

# Install requirements
pip install numpy scipy matplotlib

# Run simulation script
python main.py
