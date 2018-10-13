# Continuous Control

For this project, you will train a DDPG agent to solve the [Reacher](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Learning-Environment-Examples.md#reacher) environment provided by [Unity-ML Agents](https://github.com/Unity-Technologies/ml-agents), an open-source Unity plugin that enables games and simulations created using the [Unity Editor](https://unity3d.com/) to serve as environments for training intelligent agents. 

## Environment

In this environment, a double-jointed arm can move to target locations. A reward of +0.1 is provided for each step that the agent's hand is in the goal location. Thus, the goal of your agent is to maintain its position at the target location for as many time steps as possible.

The observation space consists of 33 variables corresponding to position, rotation, velocity, and angular velocities of the arm. Each action is a vector with four numbers, corresponding to torque applicable to two joints. Every entry in the action vector should be a number between -1 and 1.

<center>
    
![ALt text](images/reacher.gif)

</center>

The task is episodic, and in order to solve the environment, your agent must get an average score of +30 over 100 consecutive episodes.
