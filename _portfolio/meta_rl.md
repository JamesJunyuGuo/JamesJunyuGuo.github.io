---
title: "Meta RL"
excerpt: "RL Notes 2"
---
<p style="font-family: 'Times New Roman', Times, serif;">


Different from Non-stationary RL setting, in meta learning we try to solve a series of tasks using the learned knowledge, which is essentially formulated as 'learning to learn'.    
For example, in a grid world model where the robot tries to find the target point with a reward starting from different starting points. When the robot learns to execute the task starting from the bottom left corner, in the next task we let it start from the top left corner, but the two tasks share some similarities and we don't want the robot to start learning from scratch. That's where meta-learning works, we can actually let the past knowledge facilitates the current task execution.     

But in the current meta RL field we normally suffer from the three main difficulties.    

- OOD problems. In the meta-testing stage, the learner fails to adapt the meta-training results to adapt itself to the environment at the meta-testing ones.  We need to let the model capture the essential shared structures across different tasks. I think to solve this problem we usually need good assumptions about the similarity between different tasks.

- Catastrophic Forgetting. Start from the simpliest case, suppose there are only two tasks in total $A,B$ and we let the environment oscillates between $A$ and $B$. We hope that after we have learned $A$ (or $B$), the next time we encounter $A$ we can solve it using the learned model without treating it as a new model without any prior knowledge. Promising exploration directions could be first classifying the tasks, and learn the tasks in a classified cluster using meta learning methods.    

- Exploiting and exploration. These two concepts can acutally be compared to a 'egg-chicken problem'. Without good exploration we cannot exploit meaningful features from the environment (see [Decoupling Exploration and Exploitation](https://arxiv.org/abs/2008.02790)). We need to examine whether the data sampling from trajectories actually contain the desired information we need. To solve that we either need some good initialization (especially for task representation method using transformer which are sensitive to initalization, see [Transformer are good meta-learners](https://arxiv.org/abs/2206.06614)).       

</p>

