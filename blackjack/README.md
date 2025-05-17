# Blackjack — Monte Carlo Methods (Based on Sutton & Barto, Ch. 5)

This project replicates and extends the Blackjack example from *Reinforcement Learning: An Introduction* by Sutton & Barto (2nd Edition, Chapter 5).

It focuses on applying Monte Carlo methods for prediction and control in a model-free reinforcement learning setting. 
The environment models an episodic version of Blackjack, as described in the book, using an infinite deck and simplified rules. 
The goal is to allow an agent to learn an optimal policy through sampled episodes of play.

## Implemented Methods

The following Monte Carlo techniques are implemented and compared:

- **Monte Carlo Exploring Starts (MC-ES)**  
  A method that ensures sufficient exploration by starting episodes with randomly chosen state-action pairs.
  
- **On-Policy Monte Carlo Control with ε-greedy policy**  
  A strategy that improves the policy while following the same ε-greedy behavior policy.
  
- **Off-Policy Monte Carlo Prediction via Importance Sampling**  
  Allows evaluation of a target policy while sampling from a different behavior policy, using importance sampling for correction.
