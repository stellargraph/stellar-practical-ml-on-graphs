# Practical Machine Learning on Graphs course

## Overview

This document describes how to prepare your system for the Practical Machine Learning on Graphs course. 

The main requirements are **Python 3.6** and a set of python modules listed in the file **requirements.txt** 
with the correct module version numbers. 

We cannot guarantee that you will be able to do the course exercises if you don’t have the correct software tools 
installed on your machine. Please take care to make sure your system is up to date as we will have limited capacity to 
help you with software installation during the course.

We provide installation instructions for Windows 10 and MacOS. The latter can be used as a guide for common Linux 
distributions such as Ubuntu. We expect that users have some experience programming in Python and using basic tools 
such as pip and git.

Course Instructors: Anna Leontjeva and Pantelis Elinas

### Instructions for MacOS

[1] Install a Python 3 (version 3.6) distribution. We recommend 
Anaconda that can be downloaded by clicking
[here.](https://conda.io/docs/user-guide/install/download.html) Alternatively, install
Python 3.6 from [here](https://www.python.org/downloads/release/python-362/) and also
`virtualenv` via the command `pip install virtualenv`.

[2] Download and install the latest version of `git` from [here.](https://git-scm.com/download/mac)

[3] Create a working directory, e.g., `/Users/YOUR-USER-NAME/Projects`, where `YOUR_USER_NAME`
should be replaced with your user name and `Projects` is the new working directory. From this
point on we will use `HOME` to refer to `/Users/YOUR-USER_NAME` such that the working
directory will be `HOME/Projects`

[4] Create a custom environment using the command (if using conda)

 `conda create --name practical-ml python=3.6` 
 
 Alternatively, if you are not using Anaconda and conda, you can create a new virtual 
 environment using `virtualenv`. Instructions on how to install and use `virtualenv` can be 
 found [here.](https://virtualenv.pypa.io/en/stable/)
 
 `virtualenv practical-ml`
 
 The above command will create a new Python environment at location `HOME/Projects/practical-ml`

[5] Create the file `matplotlibrc` in directory `~/.matplotlib`; create the directory if it does
not exist in your system. The file contents should be,

`backend:TkAgg`
 
[6] Activate the new virtual environment created with `conda` by executing the command,

`source activate practical-ml`

or if created using `virtualenv` use the command,

`source practical-ml/bin/activate`

[7] Download or clone the course source code repository  using the command (from the `HOME/Projects` directory),

`git clone https://github.com/stellargraph/stellar-practical-ml-on-graphs.git`

[8] Change to the `stellar-practical-ml-on-graphs` directory and install the python requirements using the command,

`pip install -r requirements.txt`

[9] You also need to register the `practical-ml` environment so that it is available in `Jupyter`. You 
should use the following command,

`python -m ipykernel install --user --name=practical-ml`

[10] You can verify that you have the correct version of stellargraph installed by using the command,

 `python -c “import stellargraph as sg; print(sg.__version__)”`

Pay attention to the double quotes and the __ is two underscores (before and after the word version.) The above command 
should print

`0.5.0`

[11] You can now run jupyter notebook using the command,

`jupyter notebook`

You can access the course notebooks using your web browser at localhost:8888


**The installation should now be complete.**


### Instructions for Windows 10

[1] Install a Python 3 (version 3.6) distribution. You can download the recommended 
version from [here](https://www.python.org/downloads/release/python-362/). Make sure to select the
option to **Add Python 3.6 to PATH** on the Setup screen.


[2] Open a Windows Command Prompt and run the following command,

`python --version`

if the installation was successful then it should print,

`Python 3.6.2`

The default Python distribution also includes `pip`. On the Command Prompt type the following
command,

`pip --version`

if the installation was successful then it should print the pip version,

`pip 19.0.2`

[3] Install `virtualenv` using the following command,

`pip install virtualenv`

[4] Install `Jupyter Notebook` using the command,

`pip install jupyter`

[5] Download and install the latest version of `git` from [here.](https://git-scm.com/download/win)

[6] Create a working directory, e.g., `C:\users\YOUR-USER-NAME\Projects`, where `YOUR_USER_NAME`
should be replaced with your user name and `Projects` is the new working directory. From this
point on we will use `HOME` to refer to `C:\users\YOUR-USER_NAME` such that the working
directory will be `HOME\Projects`

[7] Change to the `HOME\Projects` directory and create a new Python virtual environment called `practical-ml`
using the following command,

`virtualenv practical-ml`

This will create a new folder `HOME\Projects\practical-ml`

[8] Activate the new environment using the command,

`practical-ml\Scripts\activate`

[9] Download or clone the `stellar-practical-ml-on-graphs` repository (in `HOME\Projects`) using the 
command,

`git clone https://github.com/stellargraph/stellar-practical-ml-on-graphs.git`

[10] Change to the `stellar-practical-ml-on-graphs` directory and install the python requirements using
the command,

`pip install -r requirements.txt`

[12] You also need to register the `practical-ml` environment so that it is available in `Jupyter`. 
You should use the following command,

`python -m ipykernel install --user --name=practical-ml`

[13] You can verify that you have the correct version of `stellargraph` installed by using the command,
 
`python -c “import stellargraph as sg; print(sg.__version__)”`
 
Pay attention to the double quotes and the __ is two underscores (before and after the word version.) The above command should print

`0.5.0`

[14] You can now run jupyter notebook using the command,

`jupyter notebook`

You can access the course notebooks using your web browser at localhost:8888


**The installation should now be complete.**

## License

Copyright 2010-2019 Commonwealth Scientific and Industrial Research Organisation (CSIRO).

All Rights Reserved.

NOTICE: All information contained herein remains the property of the CSIRO. The intellectual and technical concepts
contained herein are proprietary to the CSIRO and are protected by copyright law. Dissemination of this information 
or reproduction of this material is strictly forbidden unless prior written permission is obtained from the CSIRO.
