# CS-370

### We were given two python files that were setting up aspects of the code and allowed us to reference parts of the code we had to write and allowed us to focus on the Agent AI to find the treasure. Those python files were the GameExperience.py and the TreasureMaze.py.

### We were responsible for writing the AI Agent. It's goal was to find the treasure before the human could.

The code trains a reinforcement learning agent to navigate a maze using an epsilon-greedy strategy for action selection and experience replay for stable learning. In each epoch, the maze is reset, and the agent starts at a random position. While the game is ongoing, the agent selects actions based on either exploration (random choice) or exploitation (model prediction), executes the action, and records the resulting state, reward, and game status. Training data from experience memory is used to train the model and evaluate loss. The agent's performance is tracked through win history and win rate, with the loop breaking when the game is won or lost. Progress is monitored by comparing the win rate to the exploration rate (epsilon).
