


# Anaconda environment with Python 2.7

GIAnT must be run under PYTHON2.7 (PYTHON3 and newer is not supported)

$ conda create --name giant python=2.7
$ conda activate giant


# PREREQUIREMENT PYTHON PAKAGE


Create requirements.txt and contain the following:

scipy
matplotlib
numpy	
cython	
h5py	
pywavelets
lxml	
gdal

Create requirement_condaforge.txt and contain the following:

pygrib
pykml
pyresample
pyhdf

```
$ conda install --yes --file requirements.txt
$ conda install -c conda-forge --yes --file requirements_condaforge.txt
```

Package only can be installed through pip:
`
$ pip install weave
`

# INSTALL PYAPS

run the command

`$ cd GIAnT`
`$ svn co http://earthdef.caltech.edu/svn/pyaps`

# INSTALL GIAnT

run the command

`$ export GIANT=$PWD
$ export PYTHONPATH=$GIANT:$PYTHONPATH
$ python setup.py build_ext`

# Environment 

Create GIANT_CONFIG.bash contains:
`
export GIANT=/the/GIANT/INSTALL/DIRECTORY
export PYTHONPATH=$GIANT:$PYTHONPATH
export PATH=$GIANT/SCR:$PATH
`
run the command
`$ source GIANT_CONFIG`
