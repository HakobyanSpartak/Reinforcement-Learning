# Trajectory Sampling

This module implements trajectory sampling techniques in reinforcement learning.  
The goal is to generate and use full trajectories (sequences of states, actions, rewards) in learning or evaluation, instead of only individual transitions.

---

## 📁 Structure

```
trajectory-sampling/
├── envs/             # Environment definitions for trajectory experiments
├── agents/           # Agent implementations using trajectory-based updates
├── experiments/      # Scripts to run sampling-based experiments
├── utils/            # Utilities: plotting, logging, trajectory helpers
├── results/          # Saved trajectories, models, metrics, plots
├── requirements.txt  # Dependency list
└── README.md         # This file
```

---

## ⚙️ Requirements & Setup

1. Install dependencies:

```bash
pip install -r requirements.txt
```

2. (Optional) Use a virtual environment:

```bash
python -m venv .venv
source .venv/bin/activate     # macOS / Linux  
.venv\Scripts\activate       # Windows
```

---

## 🚀 How to Run / Usage

To train an agent with trajectory sampling:

```bash
python experiments/train_sampling.py --episodes 500 --trajectory_length 20 --alpha 0.1
```

To evaluate or analyze trajectories:

```bash
python experiments/evaluate_sampling.py --model_path results/best_model.pth
```

To plot and visualize sampled trajectories or learning curves:

```bash
python utils/plot_trajectories.py --input_dir results/ --output_fig sampling_plot.png
```

You may adjust hyperparameters through flags:
- `--trajectory_length` — length of sampled trajectories  
- `--episodes` — number of training episodes  
- `--alpha` — learning rate  
- `--gamma` — discount factor  
- etc.

---

## 🔍 Concepts & Notes

- Trajectory sampling involves collecting **complete episodes or trajectories** rather than only single-step transitions, which can allow better temporal credit assignment and richer learning updates.  
- This approach may help with variance reduction or more stable updates in some RL settings.  
- You can extend this module by using different trajectory sampling policies, off-policy corrections, or combining with importance sampling.

---

## 🧩 Extending & Customization

- Add new sampling strategies in `agents/` (e.g. importance-weighted trajectory sampling)  
- Experiment with different environment setups in `envs/`  
- Create comparative experiments in `experiments/`  
- Add visualization tools in `utils/`


**Author / Maintainer:** [Hakobyan Spartak](https://github.com/HakobyanSpartak)
