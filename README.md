# ECMWF Open Data Explorer

The repository contains [Jupyter notebook-based tutorials](https://ecmwfcode4earth.github.io/open-data-explorer/) which will offer you the support for accessing [open data](https://confluence.ecmwf.int/display/DAC/ECMWF+open+data%3A+real-time+forecasts+from+IFS+and+AIFS), downloading data, and data analysis using Python libraries.

> This project has been developed during the [Code for Earth](https://codeforearth.ecmwf.int/) innovation programme run by the European Centre for Medium-Range Weather Forecasts (ECMWF). The challenge description is available [here](https://github.com/ECMWFCode4Earth/Challenges_2025/issues/7).

## Installation
You will need to install [Python](https://www.python.org/downloads/) and we recommend you to use a UNIX-based system. First, you will create the virtual environment called [`venv`](https://docs.python.org/3.12/library/venv.html) to isolate your dependencies from other projects and activate it
```
sudo apt install python3.12-venv
sudo apt install -y python3-pip

python3 -m venv venv 
source venv/bin/activate

python3 -m pip install --upgrade pip

# Install all of the packages (including jupyterlab, jupyterlab_myst, and jupyter-book)
python3 -m pip install -r requirements.txt
```
At the end of using your virtual environment, you deactivate it with
```
deactivate
```
The notebooks should be rendered with [`jupyterlab_myst`](https://mystmd.org/guide/quickstart-jupyter-lab-myst) as we will be using [JupyterLab](https://jupyterlab.readthedocs.io/en/latest/).
```
pip install jupyterlab
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
Here we will work with [Jupyter Book 2](https://next.jupyterbook.org/) that is being rebuild on top of [MyST Document Engine](https://mystmd.org/).
```
pip install "jupyter-book>=2.0.0a0"
```
To make use of Jupyter Book 2, you need to have [Node.js](https://nodejs.org/en/download) installed on your computer. If this is not the case, after executing the `jupyter book` command you will be prompt to install it
```
# Download and install nvm:
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.3/install.sh | bash

# in lieu of restarting the shell
\. "$HOME/.nvm/nvm.sh"

# Download and install Node.js:
nvm install 24

# Verify the Node.js version:
node -v # Should print "v24.2.0".
nvm current # Should print "v24.2.0".

# Verify npm version:
npm -v # Should print "11.3.0".

# Update a new patch version of npm
npm install -g npm@11.4.2
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
