# GROWTH School Python Notebook README

These python notebooks are part of the GROWTH school series.  These notebooks
accompany lectures given by professional astronomers on the topic of 
time-domain astronomy and observational followup to astrophysical transients.
There are twelve such "modules" each providing a series of lessons and
worked examples on different aspects of time-domain astronomy.  For more detail
on the other modules and the winter school, please see:

http://growth.caltech.edu/growth-astro-school-2018-resources.html

The modules can be run individually or in any order.  The order of the GROWTH 
winter school in 2018 was:

* 1:  Python Basics
* 2:  Gravitational Wave Localization and Galaxy Crossmatch
* 3:  Observing Run Preparation
* 4:  X-ray Analysis
* 5:  Image Reduction
* 6:  UV/Optical/IR Photometry
* 7:  Image Subtraction
* 8:  Optical/IR Spectra
* 9:  Light Curve Analysis
* 10: Asteroids
* 11: Radio Analysis I: GMRT
* 12: Radio Analysis II: VLA


## Installing Dependencies

To run any of these modules, you must have a working python 3.x install 
and several python libraries.  You can tell your python version by running:

```
$ python -V
```

If you lack a python 3.x install, conda is a good source.  Find and download
the conda installer script of the latest version for your operating system here: 
https://repo.continuum.io/miniconda/

For example, if you have a linux system:

```
$ wget https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86_64.sh
```

Now, run the installer and follow the prompts:

```
$ bash Miniconda3-latest-Linux-x86_64.sh
```

Next, you'll want to install several necessary python packages using pip.  
For all of the notebooks, you'll want to get these basic packages.  We have 
pinned a few of the versions to assure things operate as they did at the winter 
school and don't break with new software updates.

```
$ pip install matplotlib==2.2.2 numpy scipy astropy==3.1.2 astroquery jupyter
```

### Installing All Dependencies for All Notebooks

For each of the notebooks, there are some additional packages or external 
programs required, each listed below.  If you plan on running all of the 
notebooks, you can just install all of the necessary dependencies as:

```
$ pip install healpy pygcn ligo.skymap astroplan astroscrappy pyregion photutils image_registration pytest pyds9 emcee corner
```

Additional external software is required for the modules: 
Image Reduction, Image Subtraction, UVOIR Photometry, and OIR spectra.

* SWarp
* SExtractor
* PSFEx
* ds9

These external software packages (except ds9) come from the Astromatic group,
http://www.astromatic.net/software, and we recommend installing these 
dependencies from your favorite package manager: `rpm`, `apt-get`, `homebrew`, 
etc.  You can alternatively install them from source, but there are additional 
dependencies (FFTW, and ATLAS) that make doing so very tedious and time 
consuming. For a standard ubuntu linux installation you can just run:

```
apt-get install swarp sextractor psfex
```

To install ds9, download the appropriate version for your platform and place
it somewhere in your path: http://ds9.si.edu/site/Download.html

### Alternatively Installing Individual Dependencies for Each Notebook

1:  Python Basics:
No additional packages required

2:  Gravitational Wave Localization and Galaxy Crossmatch
$ pip install healpy pygcn ligo.skymap

3:  Observing Run Preparation
$ pip install astroplan

4:  X-ray Analysis
No additional packages required

5:  Image Reduction
$ pip install astroscrappy pyregion

6:  UV/Optical/IR Photometry
No additional packages required

7:  Image Subtraction
$ pip install photutils image_registration pytest

8:  Optical/IR Spectra
$ pip install pyds9

9:  Light Curve Analysis
No additional packages required

10: Asteroids
No additional packages required

11: Radio Analysis I: GMRT
$ pip install emcee corner

12: Radio Analysis II: VLA
No additional packages required

## Starting the Lesson

Each module is available as a zipped file, or you can download them all 
together.  Inside the zipped file are two `.ipynb` files, Jupyter Notebook
files, which contain the lesson.  One is labeled as "solutions" and contains
the fully worked examples from the school, whereas the other leaves lessons
for the student to complete on their own.  In addition, many of the modules
contain a data directory with some configuration and science data to use
in the examples.

Once you have selected and downloaded your desired module, you can open it/them
with the command:

```
$ tar -zxvf <module_name.tar.gz>
```

Now, move to the desired module directory and launch a jupyter notebook
on the desired .ipynb file.  From here, you can follow the GROWTH lesson 
by hitting <shift-enter> on any numbered box, and it will attempt to execute 
the code within that box to produce some sort of output to illustrate the 
lesson.  When you are done, save your work, close the notebook from the 
window, and then go back to the terminal and hit <ctrl>-C to quit.  You can 
check the solutions at the end in the included notebook.  Good luck!

```
$ cd python_basics
$ jupyter notebook python_basics.ipynb
```
