# Mazes

This folder contains code for training reinforcement learning agents to solve maze environments.

## Structure

```
mazes/
├── envs/           # maze environment definitions
├── agents/         # agent algorithms and models
├── experiments/    # training & evaluation scripts
├── utils/          # helper functions (plotting, logging, etc.)
├── results/        # saved models, logs, output data
└── README.md        # this file
```

## How to run

1. Install dependencies:

```bash
pip install -r requirements.txt
```

2. Train an agent:

```bash
python experiments/train_maze.py --maze_size 10 --episodes 1000
```

3. Evaluate a trained agent:

```bash
python experiments/evaluate_maze.py --model_path results/best_model.pth
```

4. Plot results:

```bash
python utils/plot_results.py --input_dir results/ --output_fig maze_plot.png
```

## Notes

- You can change hyperparameters (learning rate, discount factor, etc.) via command-line arguments.  
- Add new maze layouts or agent types by extending `envs/` or `agents/`.
