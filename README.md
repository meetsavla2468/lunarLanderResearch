# Solving Lunar Lander with (D)DQN

## Problem Definition

This research concentrates on the establishment of a powerful form of Deep Reinforcement Learning (DRL) model that can be used for controlling a lunar lander through using OpenAI Gym Lunar Lander v2 environment [2] with Double Deep Q-Network(DDQN). The problem is about enabling an agent to learn the best thrust and orientation maneuvers
in low gravity circumstances. To achieve fuel efficient, safe landings, it is important that the model remains stable and converges during training. This research seeks to enhance the dependability of autonomous moon landing systems via state of the art DRL techniques.

A very popular benchmark for lunar landing control problem that has been used over time to evaluate and develop RL algorithms is the OpenAI Gym Lunar Lander
v2 environment. The simulation in this environment is highly detailed reproducing all complex physical dynamics of a moon landing including lunar gravity (g = 1.625 m/s2), controllable lander thrust with specific impulse and detailed interactions with the lunar surface.

- State Space: The lander’s current state is represented by an 8-dimensional continuous state space, S. Thisextensive state representation enables DRL agents to havea complete understanding of how the lander behaves dynamically.
- Action Space: The actions possible in the environment are binary and they can only take values from 0 to 3 as indicated by {0, 1, 2, 3}. Thus, during the descent stages of landing this set of discrete actions will enable DRL agents to steer or control trajectories in midair.
- Reward Structure: There is a thin reward structure R: S x A → R in the environment that encourages behaviors leading to a successful and efficient landing.
- Episode Termination: There are two main reasons why episodes end:
- Successful Landing: Occurs if both feet of the lander lie within a defined area on lunar ground.
- Crash Landing: Involves severe contact between the lander and the moon’s surface resulting in huge penalties.

This repository contains the code for a research project investigating the application of a Double Deep Q-Network (DDQN) for lunar lander control within the OpenAI Gym Lunar Lander v2 environment.

## Installation:

### Clone this repository:

git clone https://meetsavla2468@github.com/lunarLanderResearch.git
Navigate to the project directory:

Install the required libraries from terminal by:
pip install -r requirements.txt

### Running the Experiment:

Train and Evaluate the DDQN agent:

1. Open the lunarlander-torch.ipynb file
2. Run the file cell wise
3. Replace [--hyperparameter1 value1 --hyperparameter2 value2 ...] with optional command-line arguments to adjust hyperparameters (e.g., learning rate, batch size).

Follow above steps for lunarlander-tfkeras to train and visualize the model in tfkeras

### Visualizing the results

1. Run the visual_comparison.ipynb file to compare and simulate results from different models

### File Structure:

lunarlander-tfkeras: Script for training the DDQN agent and evaluating the trained DDQN agent in tensorflow and keras.
lunarlander-torch: Script for training the DDQN agent and evaluating the trained DDQN agent in torch.
ddqn_torch_model.h5 : Trained DDQN model.
requirements.txt: Text file listing required Python libraries.

### Further Notes:

Training the DDQN agent can be computationally expensive. Adjust hyperparameters and training time based on your hardware resources.
