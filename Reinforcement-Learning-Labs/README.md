
# Reinforcement Learning Labs

A hands-on introduction to Reinforcement Learning, progressing from
**tabular Q-Learning** to **Deep RL with PPO**.

##  Contents

| # | Notebook | Topic | Environment |
|---|----------|-------|-------------|
| 1 | `01_Tabular_Q_Learning/RL_lab_Qlearning.ipynb` | Tabular Q-Learning (Bellman equation, ε-greedy) | FrozenLake-v1 |
| 2 | `02_Deep_RL_PPO/RL_PPO.ipynb` | Proximal Policy Optimization (PPO) | LunarLander-v3 |

##  Learning Objectives

- Understand the **agent–environment loop**
- Implement the **Bellman update** by hand
- Balance **exploration vs. exploitation** (ε-greedy)
- Train a **neural-network policy** with Stable-Baselines3
- Evaluate and visualize trained agents

##  Requirements

```bash
pip install gymnasium[box2d] stable-baselines3 shimmy matplotlib numpy
sudo apt-get install swig   # required for Box2D
