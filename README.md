# measurement-error-decision-risk
Simulation study of measurement system variation and decision risk in Pass/Fail testing (GR&R-inspired Monte Carlo analysis).

## Project Overview

This project investigates how measurement system variation influences decision risk in Pass/Fail testing environments.

In many industrial applications (e.g., pressure retention tests, tensile tests, and leakage tests), decisions are made based on measured values compared with a specification limit. However, measurement systems always introduce some level of variation, which may lead to incorrect decisions such as:

- **False Pass** (Type II decision error)  
- **False Fail** (Type I decision error)

This project simulates such testing scenarios and evaluates the probability of incorrect decisions under different levels of measurement system variation.

---

## Objectives

- Model true product variation
- Model measurement system variation (GR&R, MSA, Cpk)
- Simulate repeated measurements
- Quantify decision errors:
  - False Pass Rate
  - False Fail Rate
- Analyze how risk changes with:
  - Tolerance width
  - Measurement noise
  - Process capability (Cp, Cpk)

---

## Mathematical Background

The simulation is based on:

- Normal distribution of true product characteristics:
  
  X_true ~ N(μ_process, σ_process)

- Measurement error model:
  
  X_measured = X_true + ε
  
  where ε ~ N(0, σ_measurement)

- Specification limit model:
  
  Pass if X_measured ≥ LSL

Decision risk is estimated via Monte Carlo simulation.

---

## Methodology

1. Generate synthetic product population
2. Add measurement system noise
3. Apply Pass/Fail decision rule
4. Compare decision vs true condition
5. Estimate error probabilities

---

## Planned Experiments

- Vary measurement system variation (σ_measurement)
- Vary process capability
- Compare narrow vs wide tolerances
- Risk vs %GRR analysis
- Decision boundary sensitivity

---

## Technologies Used

- Python 3.x
- NumPy
- Pandas
- Matplotlib
- Jupyter Notebook

---

## Expected Outcomes

The project aims to demonstrate how even a statistically acceptable measurement system (e.g., %GRR < 30%) may still generate significant decision risk depending on tolerance and process positioning.

The results will provide practical insights into measurement-driven risk in quality control systems.

---

## Author

Simeon Petkov  
Final Exam Project – Math Concepts for Developers
