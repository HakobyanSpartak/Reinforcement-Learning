# Random Walk (N‑TD)

This folder contains code for the **Random Walk** problem using **n‑step Temporal Difference (N‑TD)** methods in reinforcement learning.

The purpose is to explore how different *n* steps in TD methods affect learning speed, bias–variance tradeoff, and prediction accuracy.

---

## 📁 Structure

```
random-walk-ntd/
├── envs/             # Environment implementation (random walk dynamics)
├── agents/           # Agent algorithms implementing n‑step TD
├── experiments/      # Scripts to train and evaluate agents with various n
├── utils/            # Helper functions: plotting, monitoring, logging
├── results/          # Outputs: metrics, saved models, plots
├── requirements.txt  # Python dependencies
└── README.md         # This file
```

---

## ⚙️ Setup & Requirements

1. Install dependencies:

```bash
pip install -r requirements.txt
```

2. (Optional) Use a virtual environment to isolate dependencies:

```bash
python -m venv .venv
source .venv/bin/activate     # macOS / Linux
.venv\Scripts\activate       # Windows
```

---

## 🚀 How to Run / Usage

To train an agent using n‑step TD:

```bash
python experiments/train_ntd.py --n 3 --episodes 1000 --alpha 0.1 --gamma 0.9
```

To evaluate a trained model:

```bash
python experiments/evaluate_ntd.py --model_path results/best_model.pth
```

You can adjust hyperparameters via flags:

- `--n` — number of steps in N‑TD
- `--episodes` — number of training episodes
- `--alpha` — learning rate
- `--gamma` — discount factor

---

## 📊 Visualization

After training, use utility scripts to plot learning curves, error vs. episodes, or compare different-step results:

```bash
python utils/plot_results.py --input_dir results/ --output_fig ntd_comparison.png
```

---

## 🎯 Purpose & Notes

The **n‑step TD** method generalizes between Monte Carlo (large n) and one-step TD (n = 1).
This project studies how choosing different *n* values influences:

- Convergence speed
- Bias and variance of value estimates
- Stability in training

You can add experiments for new *n* values or compare with other methods (e.g. TD(λ)) by extending `experiments/` or `agents/`.


**Author / Maintainer:** [Hakobyan Spartak](https://github.com/HakobyanSpartak)
