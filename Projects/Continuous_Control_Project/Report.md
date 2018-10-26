# Report


### Hyperparameters

**1. Actor network**

The neural network has three fully connected layers with uniform weight initialization. As an input it takes a state of the agent in the environment and outputs the best possible possible action given that the agent is in that very specific state (a.k.a. deterministic opitmal policy). The dimensions of the layers are:

  1st layer:
  
    - input: 33 (i.e. the dimension of the state space) 
    - activation function: rectified linear unit
    - output: 400
  
  2nd layer:
  
    - input: 400 
    - activation function: rectified linear unit
    - output 300
  
  3rd layer: 
  
    - input: 300
    - activation function: none
    - output: 4 (i.e. the dimension of the action space) 
    
**1. Critic network**

The neural network has three fully connected layers with uniform weight initialization. As an input it takes a state of the agent in the environment and outputs the optimal action value function by using the Actor best belevied action. The dimensions of the layers are:

  1st layer:
  
    - input: 33 (i.e. the dimension of the state space) 
    - activation function: rectified linear unit
    - output: 400
  
  2nd layer:
  
    - input: 404 (its a concatenation of the output of the 1st layer and the Actor best belevied action) 
    - activation function: rectified linear unit
    - output 300
  
  3rd layer: 
  
    - input: 300
    - activation function: hyperbolic tangent
    - output: 1 

**2. Learning phase** 

    replay buffer size: int(1e6) 
    minibatch size: 256      
    discount factor: 0.99      
    tau = 1e-3  (for soft update of target parameters)
    learning rate of the Actor = 1e-4
    learning rate of the Critic = 3e-4
    L2 weights decay = 1e-4
    The network is updated ten times in a row after every 20 timesteps episodes

### Performance

The trend of the average scores over all 20 agents is illustrated in the plot below:

![alt text](images/avg_scores.png)

### Ideas for Future Work

Further hyperparameters optimizations could lead to better performances. Moreover, possible alternative algorithm could be 
[PPO](https://arxiv.org/abs/1707.06347), [A3C](https://arxiv.org/abs/1602.01783), and [D4PG](https://arxiv.org/abs/1804.08617) 
that use multiple (non-interacting, parallel) copies of the same agent to distribute the task of gathering experience.
