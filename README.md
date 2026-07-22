All the code runs using conda venv in Ubuntu 20.04 with recommended setup on HIMLoco github repo https://github.com/InternRobotics/HIMLoco:

conda tos accept --override-channels --channel https://repo.anaconda.com/pkgs/main
conda tos accept --override-channels --channel https://repo.anaconda.com/pkgs/r
conda create -n himloco python=3.8 -y
conda activate himloco

Then try to run play.py and train.py, note: you might need to downgrade some of the packages to run the code on Ubuntu 20.04

useful commands:
python train.py --task=go2 --headless --num_envs=4096 --max_iterations=6000 --resume --load_run=-1
tensorboard --logdir ~/robots/HackUSF2026/HIMLoco/legged_gym/legged_gym/scripts --port 6006
python play.py --task=go2
python play.py --task=go2 --num_env=num_of_parallel_robots --load_run=your_run

another useful example to run a specific checkpoint
python play.py \
  --task go2 \
  --load_run JulXX_XX-XX-XX_ \
  --checkpoint 4440

I pushed only the last checkpoint (3000.pt) due to github sizelimits
