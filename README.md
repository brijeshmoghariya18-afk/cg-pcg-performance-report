# cg-pcg-performance-report

# CG vs PCG: Reproducible Performance Benchmark (Micro-Portfolio)

## Problem
Iterative Krylov solvers such as Conjugate Gradient (CG) are widely used for large sparse symmetric positive definite (SPD) linear systems arising in scientific computing (e.g., elliptic PDE discretizations). However, their practical performance depends strongly on conditioning and memory behavior. This repository provides a reproducible benchmark to compare CG against Preconditioned CG (PCG) on representative SPD systems, focusing on iteration counts and wall-clock runtime under controlled experimental settings.

## What I implemented
- Implemented a reproducible benchmarking pipeline for CG and PCG (fixed problem generators, fixed random seeds, consistent stopping criteria).
- Evaluated solver behavior across problem sizes and parameter settings, recording runtime, iterations, and residual norms.
- Automated result logging and plotting to support transparent, report-ready comparisons (tables/plots saved in `results/` and `report/`).

## How to run
### 1) Create environment and install dependencies
```bash
python -m venv .venv
# Windows: .venv\Scripts\activate
source .venv/bin/activate
pip install -r requirements.txt
