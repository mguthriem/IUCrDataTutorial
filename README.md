# Neutron powder diffraction data reduction demo

The goal of this is to illustrate some important concepts for working with neutron powder diffraction data. Data reduction is an important data processing step where the majority of instrumental contributions to the measured data are removed as a prelude to data analysis, typically using the Rietveld method.

The data reduction workflow will be illustrated with two different approaches:

1. Using the `Mantid` Framework (see [mantidproject.org](mantidproject.org) a well established project supporting neutron data structures and algorithms.
2. [ScippNeutron](https://scipp.github.io/scippneutron/about/index.html) an ESS-led project for manipulating neutron data

Both software packages are open source, freely available and support Windows, MacOS and Linux. 

## Prerequisites

To follow the demo and explore yourself, there are some prerequisites:

### Download this repo

This repository contains the content of the demos, in the form of [jupyter notebooks](https://jupyter.org/). The repo also contains the necessary conda environment definition to run the demo on your local machine. 

The first set-up step is to download the repo, there are several ways to do this, all linked via the green `Code` button on the front page of the repo.

### Conda

The preferred method to install and manage mantid is to use conda. 

#### Scenario 1: you know what a conda environment is

Create a new environment using the `environment.yml` in the repository. This will create an environment called `IUCrDataTutorial`. Activate this environment and you are ready to go.

#### Scenario 2: you don't know what a conda environment is

TODO: 
