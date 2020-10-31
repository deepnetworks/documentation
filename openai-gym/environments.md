# Working with Environments in OpenAI Gym

A list of all the environments can be found in the GitHub repository ([envs/\_\_init\_\_.py](https://github.com/openai/gym/blob/master/gym/envs/__init__.py)).

#### Create an environment

```python
import gym
env = gym.make("CartPole-v0")

obs = env.reset()
```

### Getting metadata about the environment

#### Spaces

##### `Box`

- `Box().shape` (`tuple(int)`)
  - The dimensions of the box (i.e. the product of the values will equal the number of input dimensions). It does not include information about the _range_ of those dimensions.
- `Box().low` (`np.ndarray(int)`)
- `Box().high` (`np.ndarray(int)`)

##### `Dict`
##### `Discrete`
##### `MultiBinary`
##### `MultiDiscrete`
##### `Tuple`

#### Performing an action

```python
action = env.action_space.sample()
obs, reward, done, info = env.step(action)
```

Note that `info` should not be used for learning by the agent; it is simply
metadata that is available for the researcher.

#### Recording the environment
