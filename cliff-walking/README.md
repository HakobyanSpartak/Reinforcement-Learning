### **Project 10: Cliff Walking — SARSA, Expected SARSA & Q-Learning**

- **Objective:** Recreate the classic Cliff Walking control task and compare three TD control methods:
  - **SARSA** (on-policy)
  - **Expected SARSA**
  - **Q-Learning** (off-policy)

- **Environment:** 4 × 12 grid  
  Start = (3, 0), Goal = (3, 11)  
  Cells from (3, 1) to (3, 10) are the **cliff** — stepping into them sends the agent back to Start with a **reward of –100**.  
  All other non-terminal steps give a **reward of –1**. Discount factor γ = 1.

- **Methodology:**
  1. Initialize `Q(s,a) ≈ 0`
  2. Run episodes using an ε-greedy policy (with fixed ε)
  3. After each step, update Q using one of the following:

     - **SARSA**
       ```
       Q[s,a] ← Q[s,a] + α * ( r + γ * Q[s',a'] - Q[s,a] )
       ```

     - **Expected SARSA**
       ```
       Q[s,a] ← Q[s,a] + α * ( r + γ * E_{a'}[Q[s',a']] - Q[s,a] )
       ```

     - **Q-Learning**
       ```
       Q[s,a] ← Q[s,a] + α * ( r + γ * max_{a'} Q[s',a'] - Q[s,a] )
       ```
