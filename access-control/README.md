# Access Control Queue

## Description

This project implements a reinforcement learning solution for the access control queuing problem. The implementation demonstrates how an RL agent learns to make optimal decisions about accepting or rejecting incoming tasks based on the current server state and expected rewards. The problem involves managing a server with limited capacity where the agent must decide whether to accept new tasks or save capacity for higher-priority tasks.

## Project Structure

```
access-control/
├── main.py
├── agent.py
├── environment.py
├── utils.py
└── results/
    └── plots/
```

## Problem Overview

The access control problem is a classic reinforcement learning task where:
- A server has finite capacity for processing tasks
- Tasks arrive with different priorities and rewards
- The agent must decide to accept or reject each arriving task
- The goal is to maximize total reward over time

## Requirements

- Python 3.x
- NumPy
- Matplotlib

Install dependencies:
```bash
pip install numpy matplotlib
```

## How to Run

### Training the Agent

Run the main script to train the RL agent:
```bash
python main.py
```

### Key Parameters

The following hyperparameters can be adjusted in the code:
- `alpha`: Learning rate for value function updates (default: 0.1)
- `gamma`: Discount factor for future rewards (default: 0.9)
- `epsilon`: Exploration rate for epsilon-greedy policy
- `n_episodes`: Number of training episodes (default: 1000000)
- `max_steps`: Maximum steps per episode

### Server Configuration

- `n_servers`: Number of free servers available
- `priorities`: Array of task priority levels
- `rewards`: Corresponding reward values for each priority

## Algorithm

The implementation uses:
- **Differential Semi-Gradient SARSA**: An on-policy temporal difference learning algorithm
- **Average reward formulation**: Suitable for continuing (non-episodic) tasks
- **Epsilon-greedy exploration**: Balances exploration and exploitation

## Results

Training results and performance metrics are displayed during execution:
- Average reward over time
- Learning curves
- Policy convergence analysis

## Concepts

This project explores:
- Average reward reinforcement learning
- Continuing (non-episodic) tasks
- On-policy temporal difference methods
- Resource allocation and scheduling problems
- Trade-offs between immediate and future rewards

## Author

Spartak Hakobyan
