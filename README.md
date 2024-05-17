# Solving Lunar Lander with (D)DQN

## Problem Definition

In the simulation, the spacecraft has a main engine and two lateral
boosters that can be used to control its descent and the orientation of
the spacecraft. The spacecraft is subject to the moon's gravitational
pull, and the engines have an unlimited amount of fuel. The spacecraft
must navigate to the landing spot between two flags at coordinates (0,0)
without crashing. Landing outside of the landing pad is possible. The
lander starts at the top center of the viewport with a random initial
force applied to its center of mass. The environment has 4 discrete
actions:

- 0: do nothing
- 1: fire left orientation engine
- 2: fire main engine
- 3: fire right orientation engine

The state is an 8-dimensional vector: the coordinates of the lander in x
& y, its linear velocities in x & y, its angle, its angular velocity,
and two booleans that represent whether each leg is in contact with the
ground or not.

After every step a reward is granted. The total reward of an episode is
the sum of the rewards for all the steps within that episode.

For each step, the reward:

- is increased/decreased the closer/further the lander is to the
  landing pad.
- is increased/decreased the slower/faster the lander is moving.
- is decreased the more the lander is tilted (angle not horizontal).
- is increased by 10 points for each leg that is in contact with the
  ground.
- is decreased by 0.03 points each frame a side engine is firing.
- is decreased by 0.3 points each frame the main engine is firing.

The episode receive an additional reward of -100 or +100 points for
crashing or landing safely respectively. An episode is considered a
solution if it scores at least 200 points. The episode finishes if the
lander crashes, flies outside of the viewport of stops moving.

This repository contains the code for a research project investigating the application of a Double Deep Q-Network (DDQN) for lunar lander control within the OpenAI Gym Lunar Lander v2 environment.

## Installation:

### Clone this repository:

git clone https://meetsavla2468@github.com/lunarLanderResearch.git
Navigate to the project directory:

Install the required libraries from terminal by:
pip install -r requirements.txt

### Running the Experiment:

Train and Evaluate the DDQN agent:
1) Open the lunarlander-torch.ipynb file
2) Run the file cell wise
3) Replace [--hyperparameter1 value1 --hyperparameter2 value2 ...] with optional command-line arguments to adjust hyperparameters (e.g., learning rate, batch size).

Follow above steps for lunarlander-tfkeras to train and visualize the model in tfkeras

### Visualizing the results

1) Run the visual_comparison.ipynb file to compare and simulate results from different models

### File Structure:
lunarlander-tfkeras: Script for training the DDQN agent and evaluating the trained DDQN agent in tensorflow and keras.
lunarlander-torch: Script for training the DDQN agent and evaluating the trained DDQN agent in torch.
ddqn_torch_model.h5 : Trained DDQN model.
requirements.txt: Text file listing required Python libraries.

### Further Notes:
Training the DDQN agent can be computationally expensive. Adjust hyperparameters and training time based on your hardware resources.