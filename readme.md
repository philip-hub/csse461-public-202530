% CSSE 461 Lecture Notebooks
% Spring 2025

## Overview

This repository hosts the notebooks and in-class codebase for the lectures in CSSE 461. I recommend 
creating a virtual Python environment for this course so that we can match package versions.

I find managing my Python environment simpler in Linux, so my workflow is based in WSL. You're 
welcome to set up a Windows-based Python environment if you prefer. Our course's officially 
supported environment is Python in Jupyter Lab, running the packages listed in `requirements.txt`.

## Windows Setup

1. Download and install [Anaconda Python](https://www.anaconda.com/download). You want the 64-bit 
version for Windows with the graphical installer. (The registration is skippable!) The default install
options are fine.

2. Launch the `Anaconda Navigator` application. A long loading time is normal.

3. In the left sidecar choose "Environments". Next click "Create". Name it `csse461` and select the Python 
checkbox. Click create.

4. This step is rather manual. In the Anaconda Navigator environments tab, with `csse461` selected, 
search for each of the python packages in our `requirements.txt` package. (It's best practice to 
select all the packages first, and then click Install.)

5. To launch Jupyter Lab: from the Home tab of Anaconda Navigator, with the `csse461` environment
selected, click on Jupyter Lab. (There may be a first time install.)

## Linux Setup

1. Clone the repository.

2. Install Python
    ```
    sudo apt install python3 python3-pip python3-venv nodejs
    ```

3. Create and activate a virtual environment:
   ```
   $ python3 -m venv 461env
   $ source 461env/bin/activate
   ```

4. Install the required python packages:
   (from the course repository where `requirements.txt` lives)
   ```
   $ pip install -r requirements.txt
   ```

5. Launch jupyterlab:

   ```
   jupyter lab
   ```

   and use the Jupyterlab interface to navigate around among notebooks and code files.

   In the future you will need to activate your course Python environment (`workon 461env`) before launching Jupyter Lab.
