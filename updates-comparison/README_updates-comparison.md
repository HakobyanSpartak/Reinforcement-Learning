# Updates Comparison

This module contains experiments comparing different **update methods** in reinforcement learning algorithms.

The goal is to analyze how various update strategies (e.g., TD, MC, n-step TD) affect convergence speed, learning stability, and overall performance.

---

## 📁 Structure

```
updates-comparison/
├── envs/             # Environments for running experiments
├── agents/           # Agent implementations (TD, MC, N-TD, etc.)
├── experiments/      # Scripts to train and compare update methods
├── utils/            # Helper functions for plotting, evaluation, and logging
├── results/          # Saved results, metrics, and visualizations
├── requirements.txt  # Python dependencies
└── README.md         # This file
```

---

## ⚙️ Setup

1. Install required dependencies:

```bash
pip install -r requirements.txt
```

2. (Optional) Create and activate a virtual environment:

```bash
python -m venv .venv
source .venv/bin/activate   # macOS/Linux
.venv\Scripts\activate     # Windows
```

---

## 🚀 How to Run

Train and compare update algorithms:

```bash
python experiments/compare_updates.py --env CartPole-v1 --episodes 500
```

You can specify which update methods to test:

```bash
python experiments/compare_updates.py --methods td mc ntd
```

or adjust hyperparameters:

```bash
python experiments/compare_updates.py --alpha 0.1 --gamma 0.95
```

Results (plots, logs, metrics) will be stored in the `results/` directory.

---

## 📊 Visualization

After training, generate comparison plots using:

```bash
python utils/plot_results.py --input_dir results/ --output_fig updates_comparison.png
```

This script visualizes performance differences between various update methods across episodes.

---

## 🧠 Concept

Reinforcement learning agents update their value estimates based on experience.  
This project compares the effects of different update rules, including:

- **Monte Carlo (MC)** — updates after complete episodes  
- **Temporal Difference (TD)** — updates after each step  
- **n-step TD** — a trade-off between MC and TD  

The goal is to study how the parameter *n* and update mechanisms influence performance and stability.


**Author / Maintainer:** [Hakobyan Spartak](https://github.com/HakobyanSpartak)
