# GEODE-geepython-intro

Provides a brief intro to using Google Earth Engine via the Python API. This assumes you already have a GEE account and have already installed Anaconda or have some other way to run Python and manage packages on your local machine.

## Run the following commands from a command prompt (either powershell, anaconda terminal, etc.). They create a new conda environment called geepy (you can call your new env. whatever you want). They then install geemap and associated packages. Just fyi, the gee python api and jupyter will be installed along with geemap.

conda create -n geepy

conda activate geepy

conda install geopandas

conda install geemap localtileserver -c conda-forge

conda install jupyter_contrib_nbextensions -c conda-forge

conda install altair

## The following line opens up a browser window. Select the account associated with GEE and paste the token back into the command prompt window.

earthengine authenticate

## Then run jupyter notebook or jupyter lab from the command prompt.

jupyter notebook

## Using the menus in Jupyter Lab or Jupyter Notebook, create a new notebook and optionally save it.
## Run the following code in the notebook to test your install by pasting each block into a new cell and then running the cell.
## If successful you should see metadata for a DEM dataset and an interactive map window.

> ### First cell
import ee

import geemap

ee.Initialize()

> ### Second cell
print(ee.Image('USGS/SRTMGL1_003').getInfo())

> ### Third cell
Map = geemap.Map(center=(40, -100), zoom=4)

Map

