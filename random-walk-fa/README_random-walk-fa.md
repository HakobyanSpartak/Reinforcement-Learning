# Random Walk (Function Approximation)

This folder contains code for implementing and analyzing the **Random Walk** problem in reinforcement learning using **function approximation** techniques.

The goal is to study how agents learn value estimation and policy behavior when the state space is approximated using features or basis functions instead of exact tabular methods.

---

## 📁 Structure

```
random-walk-fa/
├── envs/             # Environment implementation (Random Walk dynamics)
├── agents/           # Agent classes with function approximation (e.g., linear, polynomial)
├── experiments/      # Training and evaluation scripts
├── utils/            # Helper functions for plotting, logging, and analysis
├── results/          # Saved results, metrics, plots, or model checkpoints
├── requirements.txt  # Python dependencies
└── README.md         # This file
```

---

## ⚙️ Setup

1. Install dependencies:

```bash
pip install -r requirements.txt
```

2. (Optional) Create a virtual environment:

```bash
python -m venv .venv
source .venv/bin/activate   # on macOS/Linux
.venv\Scripts\activate      # on Windows
```

---

## 🚀 How to Run

To train an agent on the Random Walk environment:

```bash
python experiments/train_random_walk.py --episodes 1000 --alpha 0.1 --gamma 0.9
```

To test or evaluate a trained model:

```bash
python experiments/evaluate_random_walk.py --model_path results/best_model.pth
```

You can modify hyperparameters such as:
- `--episodes` → number of training episodes  
- `--alpha` → learning rate  
- `--gamma` → discount factor  
- `--basis` → type of feature representation (e.g., polynomial, tile coding)

---

## 📊 Visualization

After training, visualize learning progress or prediction accuracy:

```bash
python utils/plot_results.py --input_dir results/ --output_fig random_walk_plot.png
```

This generates plots showing:
- Mean squared value error over time  
- Comparison between true and estimated value functions  
- Learning curves for different function approximators

---

## 🧠 Concept

The **Random Walk** problem is a simple benchmark in reinforcement learning used to illustrate value prediction and generalization.  
With **function approximation**, the agent estimates the value function using parameterized models (such as linear or polynomial features), allowing generalization across similar states.

---

## 🧩 Extending

You can:
- Implement new basis functions (e.g., radial, Fourier) in `agents/`
- Adjust environment difficulty in `envs/`
- Add new experiments under `experiments/` to compare methods (e.g., TD(0), Monte Carlo)


**Author:** [Hakobyan Spartak](https://github.com/HakobyanSpartak)
