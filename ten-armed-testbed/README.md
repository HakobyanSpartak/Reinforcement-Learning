# **Multi-Armed Bandit Reinforcement Learning Project**

This project simulates the **multi-armed bandit problem** using **epsilon-greedy strategies**.  
It generates plots to show how the **average reward** and **percentage of optimal actions** change over time for different **epsilon values**.

---

## **Features**

- Simulates multi-armed bandit problems with configurable **epsilon** values  
- Supports both **sample-average** and **constant step-size** methods for updating action values  
- Plots:
  - Average reward over time
  - Percentage of optimal actions

---

## **How It Works**

### **Bandit Class**

- Implements epsilon-greedy action selection  
- Tracks estimated values for each action and updates them based on rewards  

### **Simulation**

- Runs multiple independent runs for each epsilon value  
- Computes average performance metrics over all runs  

### **Plotting**

- Uses Matplotlib to create performance plots  
- Saves output figures in high resolution

---

## **Requirements**

Make sure required packages are installed:

```bash
pip install -r requirements.txt
