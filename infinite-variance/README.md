### **Project 7: Infinite Variance – Off-Policy Monte-Carlo Evaluation**

- **Objective:** Replicate Example 5.5 from Sutton & Barto (RL, 2nd ed.) to show that ordinary importance-sampling (IS) in off-policy Monte-Carlo can yield *infinite variance*.
- **Environment:** Seven-state random walk; episodes are generated under a behaviour policy that moves left with probability *p*.
- **Methodology:**
  - Compute the trajectory-level IS ratio ρ.
  - Update two value estimates for the centre state: one with **ordinary IS**, one with **weighted IS**.
  - Track the mean‐squared error of each estimate across episodes.
- **Implementation:** All logic lives in `infinite_variance.py` (≈50 LOC). Running the script creates a CSV log and a plot in `results/`.
- **Quick start:**
  - `pip install -r requirements.txt` → installs *numpy*, *matplotlib*, *tqdm*.
  - `python infinite_variance.py --episodes 100000` → reproduces the variance explosion.

- **Outputs:**
  - `results/variance_curves.png` – compares the running error/variance of ordinary vs. weighted IS.
  - `results/log.csv` – per-episode data for custom analysis.
- **Key insight:** Weighted IS normalises by cumulative weight, keeping variance bounded; ordinary IS does not, so its estimate can fluctuate without converging.
