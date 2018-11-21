# Collaboration and competition

For this project, you will train a DDPG agent to solve the [Tennis](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Learning-Environment-Examples.md#tennis) environment provided by [Unity-ML Agents](https://github.com/Unity-Technologies/ml-agents), an open-source Unity plugin that enables games and simulations created using the [Unity Editor](https://unity3d.com/) to serve as environments for training intelligent agents. 

## Environment

<center>
    
![ALt text](images/tennis.png)

</center>

In this environment, two agents control rackets to bounce a ball over a net. If an agent hits the ball over the net, it receives a reward of +0.1. If an agent lets a ball hit the ground or hits the ball out of bounds, it receives a reward of -0.01. Thus, the goal of each agent is to keep the ball in play.

The observation space consists of 8 variables corresponding to the position and velocity of the ball and racket. Each agent receives its own, local observation. Two continuous actions are available, corresponding to movement toward (or away from) the net, and jumping.

The task is episodic, and in order to solve the environment, your agents must get an average score of +0.5 (over 100 consecutive episodes, after taking the maximum over both agents). Specifically,

* After each episode, we add up the rewards that each agent received (without discounting), to get a score for each agent. This yields 2 (potentially different) scores. We then take the maximum of these 2 scores.

* This yields a single score for each episode.

The environment is considered solved, when the average (over 100 episodes) of those scores is at least +0.5.

## Getting started

To set up your python environment to run the code in this repository, follow the instructions below.

#### 1. Create a virtual environment. 

Create (and activate) a new environment with Python 3.6.

    Linux or Mac:
    conda create --name navigation python=3.6
    source activate navigation

Windows:

    conda create --name navigation python=3.6 
    activate drlnd
    
Perform a minimal install of OpenAI gym:

    pip install gym

Next, install the classic control environment group by following the instructions [here](https://github.com/openai/gym#classic-control).
Then, install the box2d environment group by following the instructions [here](https://github.com/openai/gym#box2d).

Create an IPython kernel for the drlnd environment.

    python -m ipykernel install --user --name drlnd --display-name "drlnd"

#### 2. Clone this repository. 

Clone the repository, and navigate to the python/ folder. Then, install several dependencies.

    git clone https://github.com/etignone/Reinforcement_Learning.git
    cd python
    pip install .

By following these instructions, you will install PyTorch, the ML-Agents toolkit, and a few more Python packages required to complete the project:

    - tensorflow==1.7.1
    - Pillow>=4.2.1
    - matplotlib
    - numpy>=1.11.0
    - jupyter
    - pytest>=3.2.2
    - docopt
    - pyyaml
    - protobuf==3.5.2
    - grpcio==1.11.0
    - torch==0.4.0
    - pandas
    - scipy
    - ipykernel

*For Windows users*: The ML-Agents toolkit supports Windows 10. While it might be possible to run the ML-Agents toolkit using other
versions of Windows, it has not been tested on other versions. Furthermore, the ML-Agents toolkit has not been tested on a               Windows VM such as Bootcamp or Parallels.

#### 2. Download the environment from one of the links below.  

You need only select the environment that matches your operating system:

- Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Linux.zip)
- Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis.app.zip)
- Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Windows_x86.zip)
- Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Windows_x86_64.zip)

Place the environment in the same folder where you put the notebooks and the python files and unzip (or decompress) it

## Instructions

Enter the cloned repository and start the jupyter notebook server with the command line:

    jupyter notebook
    
Once the web page is loaded, open the jupyter notebook Tennis.ipynb. Before running code in the notebook, change the kernel to match the tennis environment by using the drop-down Kernel menu.

### Resources

[Continuous control with deep reinforcement learning](https://arxiv.org/abs/1509.02971)
