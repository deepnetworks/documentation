# `gym.wrappers.Monitor`

- Source code: [GitHub (openai/gym)](https://github.com/openai/gym/blob/master/gym/wrappers/monitor.py)

#### Creating a Monitor wrapper

- `env` (`Env`, see [gym/core.py](https://github.com/openai/gym/blob/master/gym/core.py))
  - The environment to wrap.
- `directory` (`str`)
  - The directory to save the output videos to.
- `video_callable` (`Function(int) -> Bool`)
  - A function that takes in an episode number and outputs a boolean stating whether or not that episode should be recorded.
- `force` (`Bool`)
  - If true, will overwrite any previous recordings if the same output directory (`directory`) is used.

#### Get the file infix for saved videos
