# **Grid-World Dynamic Programming (DP)**

This project implements **Dynamic Programming (DP)** methods—specifically **iterative policy evaluation** and **policy improvement**—to solve a **4×4 grid-world Markov Decision Process (MDP)**. The implementation follows the example presented in Sutton & Barto's *Reinforcement Learning: An Introduction* (Example 4.1), demonstrating how DP algorithms converge to optimal value functions and policies in finite MDPs with discrete states and actions.

---

## **Key Components**

- **State Space (S):** 4×4 grid (16 states, indexed 1–14, with 2 terminal states at the corners)
- **Terminal States:** Shaded corners where the episode ends; all actions yield a reward of 0 with no further transitions.
- **Action Space (A):** {↑, ↓, ←, →} (deterministic transitions, except for off-grid moves)
- **Reward Function:** -1 for all transitions until termination
- **Policy (π):** Equiprobable random policy (π(a|s) = 0.25 ∀a)
- **Discount Factor (γ):** 1.0 (undiscounted episodic task)

---

## **Algorithms Implemented**

### **1. Iterative Policy Evaluation**
- **Objective:** Compute the state-value function V(s) for a given policy π.
- **Methodology:**
  - Iteratively apply the Bellman Expectation Equation for Vπ.
  - Update state values until convergence.

### **2. Policy Improvement**
- **Objective:** Derive an improved policy π' based on the computed V(s).
- **Methodology:**
  - For each state, evaluate the expected return for all actions.
  - Select the action that yields the highest expected return.
  - Update the policy accordingly.

---

## **Project Structure**

- 📁 **`notebooks/`**: Jupyter notebooks containing detailed explanations and visualizations of the DP algorithms.
- 📁 **`src/`**: Source code implementing the DP methods.
- 📁 **`generated_images/`**: Visual representations of value functions and policies.
- 📁 **`book_images/`**: Reference images from the textbook for comparison.

---

## **How to Run**

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/VArakelyan/Reinforcement-Learning-projects.git
   cd Reinforcement-Learning-projects/gridworld-dp
