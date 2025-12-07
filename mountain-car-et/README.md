# Mountain Car (Eligibility Traces / TD(λ))

This folder contains code for solving **MountainCar** using reinforcement learning with **eligibility traces** (TD(λ)), typically combined with **tile coding** for function approximation over the continuous state space.

---

## 📁 Structure

```
mountain-car-et/
├── src/
│   ├── tile_coding.py     # IHT / tiles implementation for state features
│   └── __init__.py
├── agents/                # TD(λ) / SARSA(λ) / Expected SARSA(λ) agents
├── experiments/           # Training & evaluation scripts
├── utils/                 # Plotting, logging, helpers
├── results/               # Saved runs, metrics, figures
├── requirements.txt
└── README.md
```

---

## ⚙️ Setup

Install dependencies:

```bash
pip install -r requirements.txt
```

(Optional) create a virtual environment:

```bash
python -m venv .venv
source .venv/bin/activate   # macOS/Linux
.venv\Scripts\activate     # Windows
```

---

## 🚀 How to Run

Train an agent with eligibility traces:

```bash
python experiments/train_mountain_car_et.py   --env MountainCar-v0   --episodes 800   --alpha 0.1   --gamma 0.99   --lambda 0.8   --epsilon 0.1   --n-tiles 8   --n-tilings 8
```

Evaluate a trained model:

```bash
python experiments/evaluate_mountain_car_et.py --model_path results/best_model.pth
```

Plot learning curves / returns:

```bash
python utils/plot_results.py --input_dir results/ --output_fig mountain_car_et.png
```

Common hyperparameters:
- `--alpha`   learning rate
- `--gamma`   discount factor
- `--lambda`  trace‑decay parameter (0 ≤ λ ≤ 1)
- `--epsilon` ε‑greedy exploration
- `--n-tiles`, `--n-tilings` tile‑coding resolution

---

## 🔍 Notes

- **Eligibility traces (TD(λ))** bridge one‑step TD (λ=0) and Monte Carlo (λ→1), enabling faster credit assignment.
- **Tile coding** projects continuous `(position, velocity)` into sparse binary features for linear value function approximation.
- Results (logs, metrics, plots) are saved under `results/`.

---

## 📄 License

Open‑source under the **MIT License** (see repository root).

---

**Author:** [Hakobyan Spartak](https://github.com/HakobyanSpartak)
