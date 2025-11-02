# Mountain Car

This folder contains code for solving the **MountainCar** control task using reinforcement learning (e.g., SARSA/Q‑Learning) with **tile coding** function approximation.

## 📁 Structure

```
mountain-car/
├── src/
│   ├── tile_coding.py     # IHT / tiles implementation
│   └── __init__.py
├── agents/                # SARSA / Q-Learning agents (tile-coded value function)
├── experiments/           # Training & evaluation scripts
├── utils/                 # Plotting, logging, helpers
├── results/               # Saved runs, metrics, figures
├── requirements.txt
└── README.md
```

## ⚙️ Setup

1) Install dependencies:

```bash
pip install -r requirements.txt
```

2) (Optional) Create a virtual environment:

```bash
python -m venv .venv
source .venv/bin/activate   # macOS/Linux
.venv\Scripts\activate     # Windows
```

## 🚀 How to Run

Train an agent on MountainCar‑v0:

```bash
python experiments/train_mountain_car.py   --env MountainCar-v0   --episodes 500   --alpha 0.1   --gamma 0.99   --epsilon 0.0   --n-tiles 8   --n-tilings 8
```

Evaluate a trained model:

```bash
python experiments/evaluate_mountain_car.py --model_path results/best_model.pth
```

Plot learning curves / returns:

```bash
python utils/plot_results.py --input_dir results/ --output_fig mountain_car.png
```

## 🔧 Notes

- Uses **tile coding** (`src/tile_coding.py`) to approximate the value function over continuous state (position, velocity).
- Supports standard control updates: **SARSA**, **Q‑Learning**, **Expected SARSA** (if implemented in `agents/`).
- Typical hyperparameters:
  - `--alpha` (learning rate), `--gamma` (discount), `--epsilon` (ε‑greedy)
  - `--n-tiles`, `--n-tilings` (tile coding resolution)
- Results (logs, metrics, plots) are stored in `results/`.

