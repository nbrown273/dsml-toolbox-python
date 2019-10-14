# Data Science/Machine Learning Toolbox in Python
A collection of notebooks and supporting resources used for teaching the fundamentals of data science and machine learning in python. Covers most of the SciPy framework and introduces examples of each of the fundamental techniques of data science: data-exploration, feature extraction/selection, machine learning models, and more. 

## Agenda
This repository is divided into two directories: modules and projects. The modules provide tutorials on each aspect of the SciPy framework while introducing common data science techniques through short interactive examples. The projects provide practice and a more comprehensive experience by combining several SciPy packages to solve a focused problem. The intended flow between modules and projects is:

1. Part I
    1. Module: IPython Notebooks
    2. Module: Numpy
    3. Project: Neural Network Forward Propagation
2. Part II
    1. Module: Matplotlib
    2. Module: Pandas
    3. Project: Exploring Handwritten Digits
3. Part III
    1. Module: Scipy
    2. Module: Scikit-Learn
    3. Project: Getting Started with Kaggle

## Installation

### Docker
The easiest way to ensure this project runs smoothly is to use Docker. To install Docker follow the instructions available for [Windows](https://docs.docker.com/docker-for-windows/install/) or[Mac](https://docs.docker.com/docker-for-mac/install/). If you're using a Linux distribution, Docker is probably available through your package manager; however, instructions vary slightly for each. You can check availability for your Linux distribution [here](https://docs.docker.com/v17.12/install/#server).

Once Docker is installed and the Docker daemon is started, open a terminal and change to the directory of this repository. Then pull down and run the Jupyter Lab SciPy Docker image using the following command.

```bash
docker run \
    --rm \
    --publish 8888:8888 \
    --env JUPYTER_ENABLE_LAB=yes \
    --name jlab-scipy \
    --volume `pwd`:`pwd` \
    --workdir `pwd` \
    jupyter/scipy-notebook
```

As the container runs, it will eventually print a url for the UI of the running jupyter lab server. Follow the link to open the UI in your browser.

### PIP
If you want to install the resources locally, make sure you have python3 and pip installed and accessible via the command line. For a fresh install, find the instructions for your OS [here](https://realpython.com/installing-python/). 

Next, you can optionally install and activate virtualenv if you would like to install the SciPy installations locally. Just follow the instructions [below](#optional-virtual-env).

When you're ready to install requirements, open a terminal to this repository's directory and run:

```bash
python -m pip install -U -r requirements.txt
```
Once installed, start jupyter lab in the root of this project by running:

```bash
jupyter lab
```
Startup will eventually print the URL of the UI. Visit the provided url to start working in Jupyter Lab.

#### [Optional] Virtual Env
If you would like to install your SciPy installations locally and diminish the concern of conflicting dependencies with other installations, I recommend using virtualenv to manage them. Use pip to install virtualenv globally by opening a terminal and executing the following.

```bash
pip install virtualenv
```

Then change directories to this repository and create a virtualenv by executing

```bash
virtualenv
```

This will create a folder called venv, housing the local python executable environment. Finally, activate the environment by running the activate script found in `venv/bin` (the exact script name will depend on your OS)