# Pacman-QLearning
![]((https://github.com/TheRNB/Pacman-QLearning/blob/main/Illustration.gif))
An AI solution utilizing Q-learning to navigate and solve Pacman board configurations.

This is an implementation of solving the QLearning method. 


### Agent and Environment
We should first come up with action way to represent states and actions in the game. As the pacman can only move left, right, up, down (given there are no walls in that direction), each action can be simply mapped to moving either four directions. But we face a problem when we want to find a representation of the state in the QTable. If we define a state of the agent as an encoding of the whole environment in the QTable that would make the resulting table be overfitted to the specific environment that we are training it on. So as a result, We only takes the immediate adjacent cells to the agent at any given state.

### Q-table
Now we initialize the Q table being state_space * action_space which initially is filled with zeroes. The action space as defined above is just 4 possible actions (U, D, L, R). And the states are all the possible variations possible in the given state representation as explained above. please note that some representations are not present in the given environment but may appear in another environment.

### Parameters
Now before training the mode we should define our parameters. I have found the best learning rate and discount factor to be 0.2 and 0.9.

## Inference
After going through all of the above states, we can run the model and train it on the given environment. A result of the model after training is present on top of this page as a gif.
