# CP-SAT Optimization for Hospital Room Assignment
Dissertation project on Hospital Room Assignment using **Google OR-Tools CP-SAT solver**. This repository contains the dissertation report, the academic poster, the code, the datasets, the experiment CSV and the results for a patient scheduling optimization framework. The project adresses the **Patient Admission Scheduling (PAS)** problem using both hard and soft constraints and also incorporating fairness and uncertainty mechanisms.

---

## Project Overview
This project aims for the development of a constraint-based model to optimise allocation of hospital rooms to patients with the use of:
-**Rolling horizon approach**: Solving the allocation problem day-by-day
-**Hard constraints**: Room Capacity, Conditional Equipment Constraint, Room Assignment
-**Soft constraints**: Preferred Room Capacity, Gender Mismatch, Missing Preferred Equipment, Missing Required Equipment, Patient Movement, Age Policy, Specialism Compatibility
-**Fairness**: reducing disparities: Historical Bias Penalty, First-Come-First-Served Priority
-**Uncertainty mechanism**: Delayed Admission, Early Arrival, Late Discharge, Early Release

---

## Repository Structure

```plaintext
.
├── Benchmark 3, 7, 9, 12, 15/    # Results from different benchmark instances
│   ├── Basic/                    # Model 1 - Basic model results
│   ├── Basic-FCFS/               # Mode2 - Incorporating Historical Bias and First-Come-First-Served 
│   ├── Basic-Fairness/           # Model 3 - Incorporating Historical Bias 
│   ├── Uncertainty/              # Model 4 - Basic model with uncertainty 
│   ├── Uncertainty-FCFS/         # Model 5 - Incorporating Historical Bias and First-Come-First-Served with uncertainty
│   ├── Uncertainty-Fairness/     # Model 6 - Incorporating Historical Bias with uncertainty
│   └── Plots & Reports           # PNG of plots, CSV of statistics, PDF Report of allocations
│
├── Data/                         # Benchmark datasets
│   ├── Csv Starting/             # Converted datasets
│   ├── Csv Cleaned/              # Preprocessed datasets
│   ├── Txt Files/                # Original TXT files
│
├── Code/                         # Full working implementation
│   ├── Data Handling Final.ipynb # Converting into CSV files and preprocessing
│   ├── Final Models.ipynb        # CP-SAT models (Model 1-6) and their execution
│   ├── Plots for Feasible.ipynb  # Visualization scripts
│   ├── Tuning-Experiments.ipynb  # Weight tuning experimenting procedure
│   ├── Tuning-Results.ipynb      # Regression model and Run the optimisation model with optimised weights
│
├── Tuning/                       # Weight tuning experiments & results
│   ├── Experiments/              # CSV files of Weight Tuning Experimenting results
│   ├── Results/                  # PNG of plots, CSV of statistics, PDF Report of allocations
│
├── Report & Poster/              # Written report and academic poster
│
└── README.md                     # Project documentation
