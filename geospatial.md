# Geospatial


Windows Setup
=============

1 Conda Setup
-------------
- [Go here](https://docs.conda.io/en/latest/miniconda.html) and download the installer appropriate for your system (choose Python 3.X). **IMPORTANT: Do NOT choose the latest one, but scroll down a bit to the one called "Python 3.9"**
- Keep the defaults for installation.
- Once installed, `Start -> Anaconda3 (64-bit) -> Anaconda Prompt (Miniconda3)`.
- Run the following command in the conda prompt
```conda update conda``` 

2 Creating and activating virtual environment
---------------------------------------------
- Create a folder for this course and set it as working directory `cd "your path"` 
- Run the following code block changing prexix to suit your path structure 
```
conda create --prefix="/path/to/your/course/folder/envpygis"
conda activate "/path/to/your/course/folder/envpygis"
```
- Now the text in front of your prompt should have changed.
-**don't create them on a cloud-storage linked folder for sync issue**.

3 Installing necessary packages
-------------------------------
- Run the following block code to install many more packages than what you explicitly specify. Those are dependencies.
- Make sure you run these commands **one line at a time**.

```
conda install pygeos --channel conda-forge
conda install numpy pandas matplotlib shapely geopandas -c conda-forge
conda install -c conda-forge nodejs
conda install -c conda-forge jupyterlab
conda install -c conda-forge rasterstats
conda install -c plotly plotly 
conda install --channel conda-forge esda
conda install geopy -c conda-forge
conda install contextily -c conda-forge
conda install mapclassify -c conda-forge
conda install networkx -c conda-forge
```

4 Open JupyterLab
-----------------
- Run the following block code to open `JupyterLab` in a new browser window. If a browser window does not open automatically, open a new browser window and paste one of the URLs given in the command prompt into the address bar.

```
jupyter lab --notebook-dir="path/to/your/course/folder/"
```

5 Launch a notebook and import packages
---------------------------------------
- In the `Launcher`, under `Notebook`, click on `Python 3`
- Type the following commands in the first cell and hit `SHIFT-ENTER`.
```
import pandas as pd
import geopandas as gpd
```

- When trying to launch a notebook, you may receive a `permission denied` error. In that case, shut down Jupyterlab and relaunch it from an elevated conda prompt (opened using admin rights). 

7 References
------------
- Based on [Sebastian Hohmann](https://gist.github.com/sebastianhohmann/4098cc6763b35f04317a850881af998a) guide.
- [Getting started with conda guide](https://docs.conda.io/projects/conda/en/latest/user-guide/getting-started.html)
- [conda cheetsheat](https://docs.conda.io/projects/conda/en/4.6.0/_downloads/52a95608c49671267e40c689e0bc00ca/conda-cheatsheet.pdf)
