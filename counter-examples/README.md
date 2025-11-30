# Counter Examples

This folder contains experiments demonstrating counter-examples in reinforcement learning —  
cases where algorithms behave unexpectedly or fail to converge under specific conditions.

---

## 📁 Structure

```
counter-examples/
├── envs/             # Custom environments designed for counter-examples
├── agents/           # Agents or algorithms that exhibit the issue
├── experiments/      # Scripts reproducing counter-example results
├── utils/            # Helper functions (plotting, logging, analysis)
├── results/          # Plots, logs, and recorded behaviors
├── requirements.txt  # Python dependencies
└── README.md         # This file
```

---

## ⚙️ Setup

1. Install required dependencies:

```bash
pip install -r requirements.txt
```

2. (Optional) Create a virtual environment:

```bash
python -m venv .venv
source .venv/bin/activate     # macOS / Linux
.venv\Scripts\activate       # Windows
```

---

## 🚀 How to Run

Run an experiment to reproduce a counter-example:

```bash
python experiments/run_counter_example.py --episodes 1000
```

Modify parameters such as:

```bash
python experiments/run_counter_example.py --alpha 0.1 --gamma 0.9 --env special_case
```

Results and visualizations will be saved in the `results/` directory.

---

## 🔍 Purpose

These examples highlight edge cases where common RL assumptions fail —  
for example, divergence in off-policy TD learning or instability in function approximation.

Each experiment aims to show **why** the failure happens and provide intuition behind it.

---

## 📄 License

This project is open-source under the **MIT License**.  
See the main repository for details.

---

**Author:** [Hakobyan Spartak](https://github.com/HakobyanSpartak)
