# Privacy-enhancing technologies Hands-on Workshop

## Install

This project runs on a Jupyter server compatible with Python 3.7.
If you run the project on [colab](https://colab.research.google.com/),
the following installation is optional (unless you would like to run on
*colab* using local resources).

In order to run the notebooks without *colab*, first, you might create a
virtual environment (optional). Second, install the dependencies,
to do so install [poetry](https://python-poetry.org) a packaging and
dependency management tool. Third, clone the project sources. Finally,
run the *poetry* `install` command to setup the required dependencies.
The complete installation sequence is as follows (set the `PATH`
accordingly):

```bash
# clone the project and enter to the repo dir
git clone https://gitlab.inria.fr/spicy/pow.git pow && cd $_
# create a virtual environment  
python3.8 -m venv ${PATH}/venv-pow
# activate the environment
source ${PATH}/venv-pow/bin/activate 
# install the dependency management tool
pip install poetry
# install dependencies on the environment
poetry install
```

There is also an [conda](https://docs.conda.io) configuration file
`environment.yml` provided for cases where the management with `poetry`
is not possible, in that case instead of the standard install execute:

```bash
# clone the project and enter to the repo dir
git clone https://gitlab.inria.fr/spicy/pow.git pow && cd $_
# create a conda environment 
conda env create -f environment.yml
# activate the environment
conda activate pow
```

## Run

The project is organized in self-contained Jupyter notebooks. These are
located in the `notebooks` directory of the project. There are two ways
to run them:

- On [colab](https://colab.research.google.com/), click on the links of
  each notebook to copy the notebook to *colab*. You require your own
  Google credentials to execute it. Do not forget to restart the notebook
  after the installation of the dependencies (`pow-api`).
- On a local instance of a Jupyter server, after the dependencies
  installation, launch Jupyter (copy the link displayed in the terminal
  on a Web browser) and click on a notebook from the list.

  ```bash
  jupyter notebook
  ```

In fact, there is a hybrid way to execute the notebooks. On *colab* you
can choose "Connect to local runtime" from the `Connect` toolbar.
To ensure the connection to a local Jupyter server, you have to activate
the appropiate extension:

```bash
jupyter serverextension enable --py jupyter_http_over_ws
```
