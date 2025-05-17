# **Grid-World MDP**

This project explores the implementation of **Markov Decision Process (MDP)** solution methods within a **5×5 grid-world environment**, inspired by Sutton & Barto's *Reinforcement Learning: An Introduction*. It demonstrates the application of **policy evaluation** and **value iteration** to achieve optimal value functions and policies in a finite MDP with discrete states and actions.

---

## **Key Components**

- **State Space (S):** 5×5 grid (25 discrete states)
- **Action Space (A):** {↑, ↓, ←, →}
- **Transition Model:** Deterministic (with exceptions for edge collisions)
- **Reward Function:**
  - Special states: A = +10, B = +5
  - Edge collisions: -1
  - All other states: 0
- **Discount Factor (γ):** 0.9

---

## **Algorithms Implemented**

### **1. Policy Evaluation**
- **Objective:** Solve the Bellman Expectation Equation for a fixed policy π.
- **Methodology:**
  - Input: Uniform random policy (π(a|s) = 0.25 ∀a)
  - Output: Converged value function

### **2. Value Iteration**
- **Objective:** Compute the optimal value function and derive the optimal policy.
- **Methodology:**
  - Iteratively apply the Bellman Optimality Equation
  - Update value functions and extract optimal policy

---

## **Project Structure**

- 📁 **`notebooks/`**: Jupyter notebooks containing detailed explanations and visualizations of the algorithms.
- 📁 **`src/`**: Source code implementing the MDP algorithms.
- 📁 **`generated_images/`**: Visual representations of value functions and policies.
- 📁 **`book_images/`**: Reference images from the textbook for comparison.

---

## **How to Run**

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/VArakelyan/Reinforcement-Learning-projects.git
   cd Reinforcement-Learning-projects/gridworld-mdp