# Continuous Control

For this project, you will train a DDPG agent to solve the [Reacher](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Learning-Environment-Examples.md#reacher) environment provided by [Unity-ML Agents](https://github.com/Unity-Technologies/ml-agents), an open-source Unity plugin that enables games and simulations created using the [Unity Editor](https://unity3d.com/) to serve as environments for training intelligent agents. 

## Environment

In this environment, a double-jointed arm can move to target locations. A reward of +0.1 is provided for each step that the agent's hand is in the goal location. Thus, the goal of your agent is to maintain its position at the target location for as many time steps as possible.

The observation space consists of 33 variables corresponding to position, rotation, velocity, and angular velocities of the arm. Each action is a vector with four numbers, corresponding to torque applicable to two joints. Every entry in the action vector should be a number between -1 and 1.

<center>
    
![ALt text](images/reacher.gif)

</center>

The task is episodic, and in order to solve the environment, your agent must get an average score of +30 over 100 consecutive episodes.

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

- Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Linux.zip)
- Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana.app.zip)
- Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86.zip)
- Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86_64.zip)

Place the environment in the same folder where you put the notebooks and the python files and unzip (or decompress) it

## Instructions

Enter the cloned repository and open a jupyter notebook:

    jupyter notebook
    
Before running code in the notebook, change the kernel to match the navigation environment by using the drop-down Kernel menu.
