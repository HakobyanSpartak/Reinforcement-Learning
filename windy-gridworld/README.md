### **Project 9: Windy Gridworld – ε-Greedy Sarsa**

- **Objective:** Solve the Windy Gridworld control problem  using on-policy one-step **Sarsa** with ε-greedy exploration.

- **Environment:** 7 × 10 grid. Columns 3–8 exert an upward “wind” that pushes the agent north by 1 or 2 cells per time-step (standard pattern: 1, 1, 1, 2, 2, 1).  
  Start = (3, 0); Goal = (3, 7). Stepping off the grid leaves the agent unchanged. Reward = –1 per step.

- **Methodology:**
  - Initialise \(Q(s,a) \approx 0\).
  - For each episode:  
    1. Choose action \(a_0\) with ε-greedy over \(Q\).  
    2. For each step, observe \((s,a,r,s')\), choose \(a'\) ε-greedily, then update
  - Track **steps per episode** as the learning curve until an optimal policy emerges.

