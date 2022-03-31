# Mathematics of Neural Networks 2MMA80

## Getting started

To get started with this repository you will need to have installed the version control system `git` and the package manager `conda`. If you do not already have these commands available on your Windows system:  install them from [Git for Windows](https://git-scm.com/download/win) and [Miniconda3](https://docs.conda.io/en/latest/miniconda.html).

If you are using Linux: use your system's package manager to install `git` and `conda`.

Also make sure your [Nvidia drivers](https://www.nvidia.com/download/index.aspx?lang=en-us) are up-to-date,

With `git` installed you can make a local clone of this repository:
- open your terminal (your usual on Linux, `Anaconda Powershell Prompt` on Windows),
- change directory to where you want to keep your local copy,
- `git clone https://gitlab.tue.nl/s143222/mathematics-of-neural-networks`,
- `cd mathematics-of-neural-networks` to enter your local repo.

With `conda` we can make a virtual environment in which we can install software packages. The benefit of virtual environments is that we can have several parallel installs of software of different versions and we do not have to worry about incompatible versions causing issues.

Open your terminal and navigate to where you cloned the repository. In the file `environment.yml` I have prepared a list of packages that we will be relying on, to make a new environment based on this list of packages do:
```
conda env create -f environment.yml
```

This will have created an environment called `mathnn` that contains packages such as PyTorch, Python, JupyterLab, etc. To indicate to the system that we want to work in a particular virtual environment we have to _activate_ it. We can activate the `mathnn` environment we just created with:
```
conda activate mathnn
```
To verify that the environment works start the python interpreter with
```
ipython
```
and try to import PyTorch with:
```
import torch
```
If this produces no errors you are good to go.
You can check the PyTorch version with
```
torch.__version__
```
You can check whether a GPU is available by
```
torch.cuda.is_available()
```
`True` will indicate that PyTorch has access to an Nvidia GPU through the CUDA API. In principle any code runs equally well on the CPU, but as we will see using a GPU can save a lot of time. If you have an Nvidia GPU but CUDA is not available you may need to update your drivers.
When you are done type
```
exit()
```
to terminate the interpreter.

## Working with Jupyter notebooks

Ensure you are in the `mathematics-of-neural-networks` directory and have activated the `mathnn` environment. Then you can start Jupyter lab with:
```
jupyter lab
```
This will launch Jupyter Lab inside your browser. On the left you will see a file browser. 
In the `Tutorials` directory you can find a set of notebooks that will guide you through learning PyTorch. 
If you are new to Jupyter notebooks, start with `1_GettingStartedWithJupyter.ipynb`.
The documentation for Jupyter Lab is availabe at <https://jupyterlab.readthedocs.io/en/latest/>.


