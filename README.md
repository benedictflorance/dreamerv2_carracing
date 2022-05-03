
## Setup Instructions

To modify the DreamerV2 agent, clone the repository and follow the instructions
below. There is also a Dockerfile available, in case you do not want to install
the dependencies on your system.

Get dependencies:

```sh
pip3 install tensorflow==2.7.0 tensorflow_probability ruamel.yaml 
```

- Follow the setup instructions on the customized Gym environment [here](https://github.com/benedictflorance/gym) to install gym

Train on Car Racing Environment:

`python3 dreamerv2/train.py --logdir ~/logdir/carracing/dreamerv2/ \
  --configs gym --task gym_car_racing --train_game_mode high_accel --eval_mode high_accel --train_map_id 0 --eval_map_id 0`
  
These input parameters are as follows:

- `logdir`: the directory to which you want logs to be outputted to
- `train_game_mode`: for the CarRacing OpenAI train environment, these can be either "high_friction", "high_accel", or "slow_braking"
- `eval_game_mode`: for the CarRacing OpenAI eval environment, these can be either "high_friction", "high_accel", or "slow_braking"
- `train_map_id`: the random seed number for which the training map will be generated
- `eval_map_id`: the random seed number for which the evaluation map will be generated

Customizations made can be found by looking at the commit history.
