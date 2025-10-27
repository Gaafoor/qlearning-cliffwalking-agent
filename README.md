# qlearning-cliffwalking-agent
# CliffWalking Tabular Q-Learning (Robotics – Spring 2023)

This repository contains an implementation of **Tabular Q-Learning** applied to the
`CliffWalking-v0` environment from OpenAI Gym.  
The goal is to train an agent to learn optimal navigation from a start state to a goal state
while avoiding the cliff, which resets the agent and yields a large negative penalty.

This assignment implements and compares **two** learning strategies:

1. **Pure greedy action selection (no epsilon)**
2. **Epsilon-greedy exploration with linear decay**

---

## 🧠 Problem Description

CliffWalking is a classic reinforcement learning task:

- Grid size: **4x12**
- Start: bottom-left cell
- Goal: bottom-right cell
- Cliff: the cells between start and goal on the bottom row

At each time step:
- The agent receives **-1** reward
- Falling into the cliff gives **-100** and restarts at the start state

The objective is to reach the goal **while minimizing total punishment**.

---

## 🗺️ CliffWalking Map

Below is a visual representation of the environment:
