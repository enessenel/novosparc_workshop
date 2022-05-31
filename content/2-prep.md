---
title: Workshop Prep
nav: Prep
topics: Conda; Installation; Getting data 
---

{% capture text %}
1. Install [Miniconda](https://github.com).
2. Setup a new conda environment and install novoSpaRc.
3. Download the datasets and template scripts.
{% endcapture %}
{% include card.html text=text header="Setup Overview" %}

-------------

## Install Miniconda

Conda is a python package manager that facilitates reproducibility of data analyses through separate environments. We recommend installing [Miniconda](https://docs.conda.io/en/latest/miniconda.html) which is available for all O/S.

## Create a new environment and install novoSpaRc

After having installed `conda`, create a new environment by typing `conda create -n novosparc python=3.9`. Then activate the environment with `conda activate novosparc` and try to install `novosparc` from `pip` by typing `pip install novosparc`. This should install the packages and all dependencies.

## Install Jupyter
`conda install -c anaconda jupyter` and you can start the notebook by `jupyter-notebook`  

## Tutorial Scripts

Here, we provide two files two help you with the tasks.
1. Tutorial to reconstruct droshophila embryo.
2. A generic reconstruction Python script.

{% include button.html text="Download Tutorial Files" link="files/tutorial_code.zip" color="info" %}
