# ECMWF Open Data Explorer

The repository contains [Jupyter notebook-based tutorials](https://ecmwfcode4earth.github.io/open-data-explorer/) which will offer you the support for accessing [open data](https://confluence.ecmwf.int/display/DAC/ECMWF+open+data%3A+real-time+forecasts+from+IFS+and+AIFS), downloading data, and data analysis using Python libraries.

> This project has been developed during the [Code for Earth](https://codeforearth.ecmwf.int/) innovation programme run by the European Centre for Medium-Range Weather Forecasts (ECMWF). The challenge description is available [here](https://github.com/ECMWFCode4Earth/Challenges_2025/issues/7).

## Installation
You will need to install [Python](https://www.python.org/downloads/) (Python 3.10) and we recommend you to use a UNIX-based system. First, you will create the virtual environment called `venv` to isolate your dependencies from other projects and activate it
```
sudo apt install python3.10-venv
python3 -m venv venv 
source venv/bin/activate
```
Here we will work with [Jupyter Book 2](https://next.jupyterbook.org/) that is being rebuild on top of [MyST Document Engine](https://mystmd.org/).
```
pip install "jupyter-book>=2.0.0a0"
```
The notebooks should be rendered with [`jupyterlab_myst`](https://mystmd.org/guide/quickstart-jupyter-lab-myst) as we will be using [JupyterLab](https://jupyterlab.readthedocs.io/en/latest/).
```
npm install -g mystmd # install myst locally
pip install jupyterlab_myst
jupyter lab # start using Jupyter Lab
```
To verify whether your installation was successfull, type
```
jupyter labextension list
```
and you should see the output as
```
jupyterlab-myst v2.x.x enabled OK
```

## Usage
You will move to the selected directory and clone this GitHub repository to create a local copy on your computer
```
git clone https://github.com/ECMWFCode4Earth/open-data-explorer/
```
To build a locally-served website, you will execute
```
jupyter book start
```

*To be continued...*
