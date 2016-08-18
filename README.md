# Working efficiently with multi-dimensional arrays in NumPy and xarray

Materials for "Advanced NumPy" tutorial at EuroScipy 2016

Author: Bartosz Telenczuk

## Introduction

A standard problem in many applications scientific computing is how to munge arrays of numbers coming from experiments or simulations. For example, one may try to process time series coming from sensors or summarise assays obtained with high-throughput technologies. These data are often small enough to be stored and analysed on a single machine, large enough to require CPU- and memory-efficient algorithms. 

In this tutorial I will present how to work with multi-dimensional (mainly numerical) arrays in Python. I will focus on NumPy and its  `ndarray` and show how to leverage its implementation to boost performance of data processing. I will also demonstrate how to work with labelled data in NumPy and `xarray`. 

## Format

The tutorial will consist of short demos of some advanced NumPy features followed by hands-on exercises. The format is inspired by Software Carpentry workshops and will use much of its teaching techniques. 

## Pre-requisites

*  installation of Python 3,  Jupyter notebook, NumPy, xarray, Cython, pillow and matplolib

   You can install all dependencies with `conda` ([link](http://conda.pydata.org/miniconda.html)):
   
   ```
   conda create -n advanced_numpy python=3 notebook numpy matplotlib xarray pillow cython
   ```
   
   This will create `advanced_numpy` environment, which you can activate with:
   
   ```
   source activate advanced_numpy
   ```
   
*  familiarity with basic features of NumPy (creating arrays, indexing, elementwise operation, axis-based reductions)

## Tentative syllabus

* broadcasting
* `ndarray` object, manipulating `strides`
* dtypes and structured arrays
* labelled arrays with `xarray`
* interfacing with other libraries through `__array_interface__`
* ufuncs and generalised ufuncs
* extending NumPy with Cython

## Materials

All materials are available as Jupyter notebooks on [Github](https://github.com/btel/2016-erlangen-euroscipy-advanced-numpy)
