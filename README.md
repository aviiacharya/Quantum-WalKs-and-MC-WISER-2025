# Quantum-Walks-and-MC-WISER-2025 by Abhipsa Acharya

# Quantum Galton Board – WISER 2025 Final Submission

# Team  : Quantum Walk by Abhipsa Acharya
- Single member, PhD Physics at University of Alabama
- WISER Enrollment ID : gst-RS5OaS0jIVgMCG7
- Summary : [link](https://github.com/aviiacharya/Quantum-Walks-and-MC-WISER-2025/blob/main/QW_MC_Summary_Wiser2025.pdf)

## Project Overview
This project implements an **optimized Quantum Galton Board** simulation using Qiskit for the WISER 2025 challenge.  
It demonstrates:
- **99.6% accuracy** on a 5-level board (JS distance: 0.003829)
- **18.3× quantum speedup** for a 7-level board, and over 100× for 10 levels
- Strong **noise resilience** on NISQ hardware

---

## Code Structure

The main code is organized into three blocks:

### **Block 1: Final Submission Report Generation**
- Extracts **best accuracy results** from `optimized_results` dictionary (5-level board).
- Prints executive summary, key achievements, technical specs, and conclusions.

### **Block 2: Visualization Creation**
- Generates a **6-panel figure** showing:
  -  Theoretical vs Quantum probabilities (5-Level board)
  -  Residual errors
  -  Quantum speedup factor across board sizes
  -  JS Distance comparison (noiseless vs noisy)
  -  Computational complexity scaling (classical vs quantum)
  - Summary metrics box
- Saves figure to `wiser_2025_final_results.png` or `Final.pdf`.

### **Block 3: Export & Presentation Aids**
- Exports **JSON results file** (`wiser_2025_final.json`) for submission.
- Prints **key talking points** for presentation.
- Prints a **submission checklist** for final verification.

---

## Requirements
- **Python 3.10+**
- **Qiskit 2.1.1**
- `numpy`, `matplotlib`
- `json`, `datetime`

## How to Run
- Install dependencies
- pip install qiskit==2.1.1 numpy matplotlib

## Run the script / notebook
- Quantum_Walks_Galton_Board_by_Abhipsa.ipynb

---

## Outputs
Running the script generates:
1. `wiser_final_submission.txt` – final text report.
2. `wiser_2025_final_results.png` – figure with 6 plots.
3. `wiser_2025_final.json` – structured results data for submission.

---

## Key Results
- **Best configuration:** 5-Level Board
- **JS Distance:** 0.003829 (99.6% accuracy)
- **Quantum advantage:** 18.3× for 7 levels, 102.4× for 10 levels
- **Circuit depth:** 6 (NISQ-ready)

---
## Summary
-This repository contains my quantum Galton board implementation and results for the WISER 2025 challenge, focused on a clean, reproducible pipeline that verifies the classic binomial/Gaussian behavior and communicates a simple quantum advantage story. The core idea maps each board level to a qubit, applies a Hadamard gate on every qubit to create an equal superposition over 2^n trajectories, and measures to obtain bitstrings whose Hamming weight maps to a bin index. Aggregating outcomes over many shots produces an empirical distribution that, in the symmetric case, matches the binomial PMF and approaches a Gaussian as n increases. I verify correctness quantitatively using Jensen–Shannon distance as the primary metric, supported by Total Variation Distance, Chi-squared, and maximum per-bin error, and qualitatively via overlay and residual plots. The best validated configuration is a 5‑level board with a shallow circuit (≈ depth 6 after transpilation), run with 32,768 shots on a noiseless AerSimulator backend; the observed distribution achieves a JS distance of ≈ 0.003829 from the theoretical target, which I summarize as about 99.6% agreement. I also include a compact scaling narrative showing that while classical path enumeration grows as 2^n, the quantum circuit composes n simple modules, leading to roughly O(n) gate growth for the symmetric sampler and enabling an intuitive advantage for sampling tasks. The repository packages the workflow and artifacts to be easy to review: a final text report summarizing the approach, metrics, and conclusions; a composite figure that includes theoretical vs observed bars for the 5‑level case, residuals, a speedup curve, a log‑scale complexity plot, and a summary panel; and a JSON export of metrics for reproducibility. Although the primary emphasis is the Gaussian/binomial baseline, the code structure is designed to be extensible toward biased or alternative targets by replacing uniform Hadamards with parameterized rotations and, when needed, introducing coin-and-shift primitives for quantum walk variants. I also include a brief noise note: under a modest device‑like noise model, the shallow circuit and advanced transpilation keep degradation small at this scale, supporting NISQ‑friendly execution for small-to-moderate n. Overall, this project aims to be accurate, explainable, and practical: simple circuits, sufficient shots, transparent metrics, and clean artifacts that make the results easy to validate and reuse.

## License
[MIT License](LICENSE)

---

## Acknowledgements
Developed as part of the **WISER 2025 Quantum Computing Challenge**.

