# measurement-error-decision-risk
Simulation study of measurement system variation and decision risk in pass/fail testing (GRR-inspired Monte Carlo analysis).

## Project Overview

This project investigates how measurement system variation influences decision risk in pass/fail testing environments.

In many industrial applications (e.g., pressure tests, tensile tests, leakage tests), decisions are made based on measured values compared to a specification limit. However, measurement systems introduce variation, which may lead to:

- False Pass (Type II decision error)
- False Fail (Type I decision error)

This project simulates such scenarios and evaluates the probability of incorrect decisions under different measurement system characteristics.

---

## Objectives

- Model true product variation
- Model measurement system variation (GRR-inspired)
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
3. Apply pass/fail decision rule
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

## Repository Structure

```
measurement-error-decision-risk/
│
├── README.md
├── requirements.txt
├── notebook/
│   └── measurement_error_analysis.ipynb
├── src/
│   ├── simulation.py
│   ├── decision.py
│   └── utils.py
├── figures/
└── data/
```

---

## How to Run

1. Clone the repository:

```
git clone https://github.com/YOUR_USERNAME/measurement-error-decision-risk.git
```

2. Create virtual environment:

```
python -m venv venv
```

3. Activate it:

Windows:
```
venv\Scripts\activate
```

Mac/Linux:
```
source venv/bin/activate
```

4. Install dependencies:

```
pip install -r requirements.txt
```

5. Run Jupyter Notebook:

```
jupyter notebook
```

---

## Expected Outcomes

The project aims to demonstrate how even a statistically acceptable measurement system (e.g., %GRR < 30%) may still generate significant decision risk depending on tolerance and process positioning.

The results will provide practical insights into measurement-driven risk in quality control systems.

---

## Author

Simeon Petkov  
Final Exam Project – Math Concepts for Developers
