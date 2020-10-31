# CartPole ([source](https://github.com/openai/gym/blob/master/gym/envs/classic_control/cartpole.py))

**Goal.** A pole is attached by an un-actuated joint to a cart, which moves along a frictionless track. The pole starts upright, and the goal is to prevent it from falling over. 

**Actions.** The system is controlled by applying a force of **+1 or -1** to the cart.

**Reward.** A reward of +1 is provided for every timestep that the pole remains upright.

**Failure.** The episode ends when the pole is more than 15 degrees from vertical, or the cart moves more than 2.4 units from the center.

## CartPole-v0

|Key|Value|
|:--|:---:|
|Benchmark (max episodes to solve)|1000 episodes|
|Max episode steps|200 steps|
|Success threshold|195.0|


## CartPole-v1

|Key|Value|
|:--|:---:|
|Benchmark (max episodes to solve)|?|
|Max episode steps|500 steps|
|Success threshold|475.0|

CartPole-v1 shares the same environment at CartPole-v0, but has a different episode length and success threshold (source: [stackexchange](https://stackoverflow.com/questions/56904270/difference-between-openai-gym-environments-cartpole-v0-and-cartpole-v1), [archive](https://archive.is/s9FtS)).
