# **Tic‑Tac‑Toe Reinforcement Learning Project**

This is an RL-based implementation of the classic **Tic‑Tac‑Toe** game, developed at **NPUA** (National Polytechnic University of Armenia). The aim is to train an agent to play optimally and then let it face off against another RL agent or a human.

---

## **Features**

- **RLPlayer**  
  - Learns state values with **Temporal‑Difference Learning**  
  - Uses an **ε‑greedy** policy for exploration  
  - Can **save/load** learned value tables or policies  

- **Human Player**  
  - Play against the trained RL agent via the console  

- **Game Manager**  
  - Orchestrates games between RL vs. RL or RL vs. Human  

- **State Handling**  
  - Encodes each board as a unique **hash**  
  - Detects game outcomes (win/lose/draw)  

---

## **Modes**

- **Training**  
  - Two RLPlayers compete for N epochs  
  - Tracks and logs win rates over time  

- **Evaluation**  
  - Pit two trained agents against each other to compare policies  

- **Play**  
  - Human vs. RLPlayer showdown  

---

## **Quick Start**

1. **Clone the repo**  
   ```bash
   git clone https://github.com/VArakelyan/Reinforcement-Learning-projects
   cd Reinforcement-Learning-projects/tic-tac-toe
   ```
2. **Install dependencies**  
   ```bash
   pip install -r requirements.txt
   ```
3. **Run**  
   - **Training:**  
     ```bash
     python play.py --mode train --epochs 5000
     ```
   - **Evaluation:**  
     ```bash
     python play.py --mode eval
     ```
   - **Play vs. Human:**  
     ```bash
     python play.py --mode human
     ```
