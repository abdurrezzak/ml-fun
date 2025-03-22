# RL GridWorld Explorer

A visual reinforcement learning project to master foundational algorithms.

## 🧩 Problem Statement

We're building a 2D grid world where an agent must learn to navigate through:

- Starting at a fixed (or random) position
- Learning to reach a goal
- Avoiding walls and traps
- Optimizing for speed (minimizing steps)

The environment is unknown to the agent—it learns entirely through experience, making this a classic sequential decision-making task under uncertainty.

## 🌍 Environment Description

```
S  .  .  .  G
.  X  X  .  .
.  .  .  T  .
```

| Symbol | Meaning |
|--------|---------|
| S | Start position |
| G | Goal (+10 reward) |
| T | Trap (-5 or -1 reward) |
| X | Wall (impassable) |
| . | Empty space (-0.1 reward per step) |

## 💡 Reinforcement Learning Aspects

- Agent has no prior knowledge of the grid layout
- Learning happens through trial and error
- Rewards are delayed (requires long-term strategy)
- Agent must balance exploration and exploitation

## 🛠️ Implementation Approach

We'll train an agent to:

1. Explore the environment
2. Learn value functions (Q-table)
3. Derive optimal policies
4. Improve through repeated episodes
5. Visualize learning progress

## 📚 Algorithms to Implement

### 1. Q-Learning (Off-policy)
- Learns optimal action values
- Update rule: $Q(s,a) \leftarrow Q(s,a) + \alpha[r + \gamma \max_{a'} Q(s',a') - Q(s,a)]$

### 2. SARSA (On-policy)
- Learns values of the current policy
- Update rule: $Q(s,a) \leftarrow Q(s,a) + \alpha[r + \gamma Q(s',a') - Q(s,a)]$

### 3. TD(λ)
- Uses eligibility traces to credit previous states
- Combines bootstrapping and Monte Carlo methods
- Accelerates learning through memory of visited states

### Advanced Extensions (Optional)
- Value/Policy Iteration
- Monte Carlo methods
- Double Q-learning
- Dyna-Q (model-based approach)

## 🔍 Learning Objectives

- Master RL agent learning from scratch
- Understand on-policy vs off-policy approaches
- Observe exploration/exploitation tradeoffs
- Compare algorithm performance
- Build modular, visual code for portfolio

## 📈 Visualization Plans

We'll create:
- Live episode rendering (agent navigating the maze)
- Q-value and visit frequency heatmaps
- Reward and step count plots
- Policy visualization (directional arrows)

## 🚀 Implementation Roadmap

1. `environment.py` (GridWorld class)
2. Rendering functions (terminal and matplotlib)
3. OpenAI Gym-like API (reset, step methods)
4. Agent implementations
5. Training and visualization scripts
