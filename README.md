# Quantum-WalKs-and-MC-WISER-2025 by Abhipsa Acharya

# Quantum Galton Board – WISER 2025 Final Submission

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
- Creates a text-based **final submission report** (`wiser_final_submission.txt`).
- Prints executive summary, key achievements, technical specs, and conclusions.

### **Block 2: Visualization Creation**
- Generates a **6-panel figure** showing:
  1. Theoretical vs Quantum probabilities (5-Level board)
  2. Residual errors
  3. Quantum speedup factor across board sizes
  4. JS Distance comparison (noiseless vs noisy)
  5. Computational complexity scaling (classical vs quantum)
  6. Summary metrics box
- Saves figure to `wiser_2025_final_results.png`.

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
- python wiser_2025_submission.py

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

## License
[MIT License](LICENSE)

---

## Acknowledgements
Developed as part of the **WISER 2025 Quantum Computing Challenge**.

