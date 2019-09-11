# scientific-python
A collection of notebooks used for teaching the fundamentals of data science and machine learning in python. Covers six pieces of the SciPy framework, and introduces some basic machine learning models along the way. There are also comprehensive projects available that combine the basics of multiple modules together into one application. The intended flow between modules and projects is:

1. Part I
    1. Module: Jupyter Lab
    2. Module: Numpy
    3. Project: Neural Network Evaluation
2. Part II
    1. Module: Pandas
    2. Module: MatplotLib
    3. Project: ???
3. Part III
    1. Module: Scipy
    2. Module: Scikit-Learn
    3. Project: ???

## Installation
### Docker
The easiest way to ensure this project runs smoothly is to install Docker, pull down the jupyterlab scipy image, and run the container:
```bash
docker run -p 8888:8888 -e JUPYTER_ENABLE_LAB=yes jupyter/scipy-notebook
```
As the container runs, it will eventually print a url for the UI of the running jupyter lab server.

### PIP
If you would rather not use Docker, make sure you have python3 and pip installed and accessible via the command line. Then run 

```bash
python -m pip install -U -r requirements.txt
```

Once installed, start jupyter lab in the root of this project by running:
```bash
jupyter lab
```
then visit the provided url.