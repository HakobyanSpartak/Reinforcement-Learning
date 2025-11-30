# Random Walk (Eligibility Traces / TD(λ))

This folder contains code for the Random Walk problem using **eligibility traces** (TD(λ)) in reinforcement learning.

The goal is to study how the trace decay parameter **λ** blends n‑step returns and affects learning speed, bias–variance, and stability.

---

## 📁 Structure

```
random-walk-et/
├── envs/             # Random Walk environment
├── agents/           # TD(λ) / eligibility trace agents
├── experiments/      # Training and evaluation scripts
├── utils/            # Plotting, logging, analysis helpers
├── results/          # Saved runs, metrics, figures
├── requirements.txt  # Dependencies
└── README.md         # This file
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
source .venv/bin/activate     # macOS / Linux
.venv\Scripts\activate       # Windows
```

---

## 🚀 How to Run

Train an agent with TD(λ):

```bash
python experiments/train_et.py --episodes 1000 --alpha 0.1 --gamma 0.9 --lambda 0.8
```

Evaluate a trained model:

```bash
python experiments/evaluate_et.py --model_path results/best_model.pth
```

Plot learning curves / value error:

```bash
python utils/plot_results.py --input_dir results/ --output_fig et_learning.png
```

Common hyperparameters:
- `--alpha`  learning rate
- `--gamma`  discount factor
- `--lambda` trace‑decay parameter (0 ≤ λ ≤ 1)
- `--episodes` number of training episodes

---

## 🔍 Notes

- TD(λ) unifies one‑step TD (λ=0) and Monte Carlo (λ→1) via **eligibility traces**.
- Useful for faster learning and improved credit assignment compared to pure TD(0) or MC in Random Walk.

---

## 📄 License

Open‑source under the **MIT License** (see repository root).

---

**Author:** [Hakobyan Spartak](https://github.com/HakobyanSpartak)
