# Deep Reinforcement Learning
## Policy-Based Methods
### Deep Deterministic Policy Gradients (DDPG)
### Continuous Control (Reacher Environment)

---

The notebook and Python files in this repository present a solution using the Unity ML-Agents **Reacher** environment for the second project of the Udacity [Deep Reinforcement Learning Nanodegree](https://www.udacity.com/course/deep-reinforcement-learning-nanodegree--nd893).

## Project Details

In this project environment, a double-jointed arm can move to target specific locations. A reward of +0.1 is provided for each step that the agent's hand is in the goal location. Therefore, the arm must follow the target as much as possible. The environment is considered solved when the agent has an average score of 30 or higher in a rolling 100 episodes.

The observation space consists of 33 variables corresponding to position, rotation, velocity, and angular velocities of the arm. Each action is a vector with four numbers, corresponding to torque applicable to two joints. Every entry in the action vector should be a number between -1 and 1. 

In other words, The *state space* for this project consists of 11 continuous 3-dimensional vectors representing the position, rotation, velocity, and angular velocities of the two parts of a virtual "reacher" arm, along with the position of the "hand" and the position and speed of the goal sphere. The goal sphere is programmed to circle around the arm (within the X-Y plane, Z is constant).
The *action space* is a vector with four numbers, clamped between -1 and 1, corresponding to the X and Z torques applicable to arm's two joints ("shoulder" and "elbow"). 
Code for the **ReacherAgent** can be viewed [here](https://github.com/Unity-Technologies/ml-agents/blob/master/UnitySDK/Assets/ML-Agents/Examples/Reacher/Scripts/ReacherAgent.cs).
The animation below shows a version of the environment with 10 arms follow the goal spheres movements:

![Reacher Environment](images/reacher.gif)

A video -from UNITY- of the hands (blue) and goal spheres (green) in motion can be also watched from [here](https://youtu.be/2N9EoF6pQyE).

## Getting Started
- Follow the Udacity DRLND dependencies [instructions here](https://github.com/udacity/deep-reinforcement-learning#dependencies) 

- Be sure of install [Unity ML-Agents](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Installation.md), [NumPy](http://www.numpy.org/) and [PyTorch](https://pytorch.org/).

- Download a prebuilt simulator as follows:
#### Singe Agent:
Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Linux.zip)
Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher.app.zip)
Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Windows_x86_64.zip)
#### Twenty Agents:
Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Linux.zip)
Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher.app.zip)
Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86_64.zip).

## The Solution

In this repo, two solutions are provided:
1. The first solution is based on a Single Agent and solved using Deep Deterministic Policy Gradients (DDPG) method. The whole solution can be found [here](/Single_Arm/) and you can start by launching the [DDPG_Continuous_Control](/Single_Arm/DDPG_Continuous_Control_v0.3.ipynb) file using Jupyter notebook. The training performance is shown below: 
![Single Agent Training](/Single_Arm/result_score.jpg).

2. The second solution is based on 20 Agents trained simultaneously and solved using Deep Deterministic Policy Gradients (DDPG) method. The whole solution can be found [here](/Multiple_Arms/) and you can start by launching the [DDPG_Continuous_Control_20Agents](/Multiple_Arms/DDPG_Continuous_Control_20Agent_v0.4) file using Jupyter notebook. The training performance is shown below: 
![Multiple Agents Training](/Multiple_Arms/result_score.jpg).

More details can be found in this [report](report.pdf).
