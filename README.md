# Udacity Deep Reinforcement Learning Nano Degree - Continuous Control
This is the submission for the Continuous Control project in Udacity Deep Reinforcement Learning Nano Degree.

# The Environment
![](Resource/reacher.gif)

In this environment, a double-jointed arm can move to target locations. A reward of +0.1 is provided for each step that the agent's hand is in the goal location. Thus, the goal of your agent is to maintain its position at the target location for as many time steps as possible.

The observation space consists of 33 variables corresponding to position, rotation, velocity, and angular velocities of the arm. Each action is a vector with four numbers, corresponding to torque applicable to two joints. Every entry in the action vector should be a number between -1 and 1.

# Solving the Environment
There are two versions to solve this environment and **this project implements the second version that supports 20 agents environment**.

**Option 1: Solve the First Version**\
The task is episodic, and in order to solve the environment, the agent must get an average score of +30 over 100 consecutive episodes.

**Option 2: Solve the Second Version**\
The barrier for solving the second version of the environment is slightly different, to take into account the presence of many agents. In particular, the agents must get an average score of +30 (over 100 consecutive episodes, and over all agents). Specifically, After each episode, the rewards of all agents need to be added up to get a score for each agent. This yields 20 (potentially different) scores. Then, the average of these 20 scores will be calculated. This yields an average score for each episode (where the average is over all 20 agents).

The environment is considered solved, when the average (over 100 episodes) of those average scores is at least +30. 


# Getting started
**Step 1: Clone the DRLND Repository**  
Please follow the [instructions in the DRLND GitHub repository](https://github.com/udacity/deep-reinforcement-learning#dependencies) to set up your Python environment. These instructions can be found in README.md at the root of the repository. By following these instructions, you will install PyTorch, the ML-Agents toolkit, and a few more Python packages required to complete the project.

(For Windows users) The ML-Agents toolkit supports Windows 10. While it might be possible to run the ML-Agents toolkit using other versions of Windows, it has not been tested on other versions. Furthermore, the ML-Agents toolkit has not been tested on a Windows VM such as Bootcamp or Parallels.

**Step 2: Download the Unity Environment**  
Please download and extract the **Reacher** application in the current project from one of the links below. You only need to download the environment that matches your operating system:

- **Version 1: One (1) Agent**\
Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Linux.zip)\
Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher.app.zip)\
Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Windows_x86.zip)\
Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Windows_x86_64.zip)

- **Version 2: Twenty (20) Agents**\
Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Linux.zip)\
Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher.app.zip)\
Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86.zip)\
Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86_64.zip)

**Step 3: Run the notebook for this project inside drlnd environment**  
> jupyter notebook Continuous_Control.ipynb	

**Step 4: Change the path of reacher application**  
Please change the path to the reacher application based on the location of the application in the following command:
> env = UnityEnvironment(file_name="path/to/your/reacher")

**Step 5: Execution**  
The section four (4) is the actual implementation for training and testing the agent. It contains three cells:
- The first cell is for loading modules.
- The second cell is for training the agent with DDPG method.
- The third cell is for testing the agent with trained network. The actor and critic network-weights are loaded from 'checkpoint_actor.pth' and 'checkpoint_critic.pth' files respectively.

If you need to only test the agent with pre-trained model, please skip the training cell.

# Report
The implemented method for the training of the agent is explained in the [report](REPORT.md).

<sub><sub>This readme is adapted from Udacity Deep RL Nano Degree course.<sub><sub>

