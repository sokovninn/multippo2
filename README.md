
# Multi-policy algorithm for robotic manipulation tasks with diverse subgoals

## Installation

Clone the repository:

`cd multippo2`

Create Python 3.7 conda env (later Python versions does not support TF 0.15.5 neccesary for Stable baselines ):

`conda create -n  mygym Python=3.7`

`conda activate mygym`

Install myGym:

`python setup.py develop`

If you face troubles with mpi4py dependency install the lib:

`sudo apt install libopenmpi-dev`

## How to replicate the results:

Pick and Place:
`train.py -config ./configs/train_pnp_3n.json`

Multitask Pick and Place:
`python train.py -config ./configs/train_pnp_2n_multitask2.json`

Pick and Rotate:
`python train.py -config ./configs/pnr_medium.json`

Multitask Pick and Rotate:
`python train.py -config ./configs/pnr_medium_multi2.json`

Swipe:
`python train.py -config ./configs/train_swipe.json`

Multitask Swipe:
`python train.py -config ./configs/train_swipe_multi2.json`

Test the trained model:
`python test.py --config ./path_to_the_training_config --gui 1`


