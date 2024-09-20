# Neutron powder diffraction data reduction demo

The goal of this demo is to illustrate some important concepts for working with neutron powder diffraction data. Data reduction is an important data processing step where the majority of instrumental contributions to the measured data are removed as a prelude to data analysis, typically using the Rietveld method.

The data reduction workflow will be illustrated with two different approaches:

1. Using the `Mantid` Framework (see [mantidproject.org](mantidproject.org) a well established project supporting neutron data structures and algorithms.
2. [ScippNeutron](https://scipp.github.io/scippneutron/about/index.html) an ESS-led project for manipulating neutron data

Both software packages are open source, freely available and support Windows, MacOS and Linux. 

## Prerequisites

To follow the demo and explore yourself, there are some prerequisites:

### Python

For this tutorial, knowledge of the Python scripting language is not essential (for example, the planned in-person demo of mantid will use convenient GUI-based tools), however, having even a basic knowledge of python will be helpful and will greatly enrich the possiblities to interact with the data. If you have never used python before, we recommend that you spend some time looking at these free introductory links (taken from [wiki.python.org](https://wiki.python.org/moin/BeginnersGuide)):

* [Beginners Python tutorial at Python Land](https://python.land/python-tutorial) 
* [Dataquest for Python for data science](https://www.dataquest.io/)
* [HackInScience free and open source platform](https://www.hackinscience.org/)

There are also [many youTube videos](https://www.youtube.com/results?search_query=beginners+python+science)

### Download this repo

This repository contains the content of the demos, in the form of [jupyter notebooks](https://jupyter.org/). The repo also contains the necessary conda environment definition to run the demo on your local machine. 

The first set-up step is to download the repo, there are several ways to do this, all linked via the green `Code` button on the front page of the repo.

### Conda

The preferred method to install and manage mantid is to use conda. 

#### Scenario 1: you know what a conda environment is

Create a new environment using the `environment.yml` in the repository. This will create an environment called `IUCrDataTutorial`. Activate this environment and you are ready to go.

#### Scenario 2: you don't know what a conda environment is

Conda is a "package, dependency and environment manager". What do these words mean? 

* "Package manager" conda is able to locate, download and install software for you
* "Dependency manager" conda will ensure that any 3rd party software that your package needs is the correct version. Example: the package you want to run was developed using python 3.10 and will crash if you try to run it with python 3.11. Conda will ensure that python 3.10 is available and is what is invoked if you run `python`.
* "Environment manager" conda will make sure all of the 3rd party software needed is downloaded, is available and is the correct version for you package to run   

The [Conda Getting Started Page](https://docs.conda.io/projects/conda/en/stable/user-guide/getting-started.html) has full instructions on installing and running conda on Windows, MacOS and Linux. The same website has a bunch of "How To's", "Troubleshooting" and tutorials. 

Once conda is installed, you must create a conda environment. This is done from the command line in the folder where you downloaded the repo. The repo contains the file `environment.yml` which is a blueprint to build the environment. Conda will build the environment using this if you instruct it with the command: 
```
conda env create -f environment.yml
```
This will tell you all of the packages that will be downloaded and prompt you if it's OK to continue. If you agree, an environment called `IUCrDataTutorial` will be created and the necessary software installed within it. Once the environment is successfully created, you must activated it using:

```
conda activate IUCrDataTutorial
```
You should now be able to run the tutorial

### Data

In order to run this demo, you need to access some neutron data. These datasets can be quite large so are not included in this repo and are instead located on a dropbox folder here:

https://www.dropbox.com/scl/fo/kduv87wx4j2cc71u9lu97/AKy4Yn7Q_EAvXyd1jV0jd1w?rlkey=jcy7759n02vqc8ikwyglr5k30&st=rvf18jlv&dl=0

Inside that folder, you will find 4 files: 

| File Name | Description | File size (Gb) |
|----|----|----|
|diffract_consts.h5 | Contains calibration for each detector pixel | 0.00 |
|NIST_Silicon.nxs | Neutron powder from a NIST standard Silicon | 0.13 | 
|vanadium-niobium.nxs | Powder data from solid vanadium-niobium alloy | 0.36 |
|empty.nxs | Measurement of empty instrument | 0.06 |

You should download local copies of these files and remember where these are stored. 

### Jupyter notebooks

The content of the demo are contained in jupyter notebooks. If you are unfamiliar with these, they are like an interactive webpage that allows you to run code inside them. jupyter is already installed in the IUCrDataTutorial conda environment and can be activated by entering

```
jupyter notebook
```
or, alternatively
```
jupyter lab
```
Either application will open in your default browser, and you can select the notebook you want to open from there.

The content of the notebook consists of a series of "cells" blocks of content that contain either text or code. To activate code all that's needed is to select a cell and enter `shift-enter`. More detailed instructions are contained in the text of the notebook itself.

