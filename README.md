# GEODE-geepython-intro

Provides a brief intro to using Google Earth Engine via the Python API

## Run the following lines from a command prompt (either powershell, anaconda terminal, etc.). They create a new conda environment called geepy (you can call your new env. whatever you want). They then install geemap and associated packages. Just fyi, the gee python api will be installed along with geemap.

conda create -n geepy

conda activate geepy

conda install geopandas

conda install geemap localtileserver -c conda-forge

conda install jupyter_contrib_nbextensions -c conda-forge

## The following line opens up a browser window. Select the account associated with GEE and paste the token back into the command prompt window.

earthengine authenticate

## Run jupyter notebook or jupyter lab

jupyter notebook

## Create a new notebook and save it if you want.
## Run the following code into the notebook to test your install.
## If successful you should see metadata for a DEM dataset.

import ee
import geemap

ee.Initialize()

print(ee.Image('USGS/SRTMGL1_003').getInfo())
