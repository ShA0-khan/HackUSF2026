All the code runs using conda venv in Ubuntu 20.04 with recommended setup on HIMLoco github repo https://github.com/InternRobotics/HIMLoco:

conda tos accept --override-channels --channel https://repo.anaconda.com/pkgs/main
conda tos accept --override-channels --channel https://repo.anaconda.com/pkgs/r
conda create -n himloco python=3.8 -y
conda activate himloco

Then try to run play.py and train.py, note: you might need to downgrade some of the packages to run the code on Ubuntu 20.04
