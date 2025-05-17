### **Project 8: Random Walk – TD(0) Learning**

- **Environment:** Linear chain of 5 non-terminal states with terminal states at both ends; the agent starts in the centre and moves left / right with equal probability.
- **Methodology:**
  - Run episodes under the equiprobable policy.
  - After each transition apply the TD(0) update  

  - Track root-mean-squared error (RMSE) between the learned values and the true values of each non-terminal state.
- **Config flags:** `--episodes`, `--alpha`, `--seed` (for reproducibility).
- **Key insight:** TD(0) updates after every step, enabling faster, lower-variance convergence than waiting until episode end.
