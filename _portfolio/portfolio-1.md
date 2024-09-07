---
title: "Non-stationary RL"
excerpt: "My first note on RL"
---

### Non-Stationary RL    
Usually we consider optimizing an objective under a stationary MDP with a fixed transition and reward function. We can learn the optimal policy through policy evaluation and policy improvement steps. However, in a constantly-changing environment where the transition kernal and the reward functions may be unkown, it's crucial for our learners to adapt itself to the environment through interaction and sampling.   

#### Existing Literature On Continual Learning
1. [Towards Continual Reinforcement Learning: A Review and Perspectives](https://jair.org/index.php/jair/article/view/13673)
2. [A Comprehensive Survey of Continual Learning: Theory, Method and Application](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=10444954)
3. [Reinforcement learning algorithm for non-stationary environments](https://link.springer.com/article/10.1007/s10489-020-01758-5)

Now I'm trying to understand the big picture of the field in Non-stationary RL. Here is the collection of papers I'm planning to read.   

- [Black Box Multi-Agent System](https://iclr.cc/virtual/2024/poster/18862)
- [Memory-Based Meta-Learning](https://icml.cc/virtual/2023/poster/23662)
- [Debiased Offline Representation Learning](https://icml.cc/virtual/2024/poster/34708)
- [Adaptive Deep RL for Piecewise Context](https://neurips.cc/virtual/2022/poster/53528)
- [Factored Adaptation](https://neurips.cc/virtual/2022/poster/55118)
- [Goal Oriented Shortest Path](https://neurips.cc/virtual/2022/poster/53545)
- [Counterfactual Off-Policy](https://neurips.cc/virtual/2022/poster/54093)
- [Inverse Online Learning](https://iclr.cc/virtual/2022/poster/7211)
- [RestartQ-UCB](https://icml.cc/virtual/2021/poster/8427)
- [Sliding Window Upper-Confidence](https://icml.cc/virtual/2020/poster/5829)
- [Optimizing for the Future](https://icml.cc/virtual/2020/poster/6316)
- [Safe Policy Improvement ](https://neurips.cc/virtual/2020/poster/17861)
- [Dynamic Regret](https://neurips.cc/virtual/2020/poster/18121)  
Usually, the numerical experiemnts are tested on the Grid World and the [MuJoCo](https://ieeexplore.ieee.org/document/6386109) environments to show the efficiency of the algorithm.

