# Adaptive-Pricing-in-Imperfect-Competitive-Markets-A-Reinforcement-Learning-Approach
This project explores the pricing dynamics of differentiated goods (such as coffee capsules) within imperfectly competitive markets using Reinforcement Learning (RL). By replicating duopoly and discrete oligopoly models, the study analyzes how strategic agents adjust prices in response to competitors' actions and market demand.
Authors: Chiara Pizzetti, Karina Trelles
Project overview
This project simulates a duopoly market where two competing agents (sellers of coffee capsules) aim to maximize their profits by dynamically adjusting their prices. We explore and compare two different Reinforcement Learning approaches:

Independent Q-learning
Deep Q-Networks (DQN) The environment is build using the Gymnasium framework, simulating a linear demand model where profit is influenced by both the agent's own price and the competitor's price.
Market Environment
The simulation includes:

Agents: 2 competing sellers.
Action Space: Discrete price choices from a predefined list (e.g., [2.99, 3.48, ..., 5.99]).
State Space: Each agent observes its own previous price and the competitor's previous price.
Reward: Calculated as the total profit: Profit = (Price - Cost) * Demand.
Demand Model: Demand = a - b * own_price + c * (competitor_price - own_price).
Algorithms Implemented
1. Independent Q-learning
In this approach, each agent maintains its own Q-table. Agents learn to find the optimal price index by interacting with the environment simultaneously using an epsilon-greedy strategy for exploration.

2. Deep Q-Network
We implement a deep learning approach where the Q-function is approximated using a Neural Network. This method includes:

Experience Replay: To break correlation between consecutive samples.
Target Network: To stabilize training.
Epsilon Decay: For gradual transition from exploration to exploitation.
Results and Comparison
The project includes a detailed evaluation section comparing the average rewards per step and the learned pricing policies for both methods. Visualizations include:

Rolling average rewards over episodes.
Greedy policy evaluation (Optimal price indices learned).
Requirements
To run this notebook, you will need the following libraries:

numpy
gymnasium
matplotlib
torch (for the DQN implementation)
How to Run
Clone the repository.
Install dependencies: pip install gymnasium numpy matplotlib torch.
Open RL Project.ipynb in Jupyter Notebook or Google Colab.
Run all cells to see the training process and the final performance comparison.
