# Report


### Hyperparameters

**1. Network**

The neural network has three fully connected layers. The dimension of the layers are:

  1st layer:
  
    - input: 37 (i.e. the dimension of the state space) 
    - output: 64
  
  2nd layer:
  
    - input: 64 
    - output 64
  
  3rd layer: 
  
    - input: 64 
    - output: 4 (i.e. the dimension of the action space)

**2. Learning phase** 

    breplay uffer size: int(1e5) 
    minibatch size: 64       
    discount factor: 0.99      
    tau = 1e-3  (for soft update of target parameters)
    learning rate = 5e-4               
    The network is updated after every 4 episodes

**3. Agent greediness**

    Starting epsilion: 1.0
    Ending epsilion: 0.01
    Epsilon decay rate: 0.999

### Performance

The model was trained over 2000 episodes. The trand of the average scores is illustrated in the plot below:



### Ideas for Future Work

Having said that further hyperparameters optimizations could lead to better performances, possible extension and improvement of the vanilla Deep Q Network, can be:

- [Double Deep Q Networks](https://arxiv.org/pdf/1509.06461.pdf)
- [Prioritized Experience Replay](https://arxiv.org/pdf/1511.05952.pdf)
- [Dueling Deep Q Networks](https://arxiv.org/pdf/1511.06581.pdf)
- [Distributional DQN](https://arxiv.org/pdf/1707.06887.pdf)
- [Noisy DQN](https://arxiv.org/pdf/1706.10295.pdf)
- [RAINBOW Paper](https://arxiv.org/pdf/1710.02298.pdf)

