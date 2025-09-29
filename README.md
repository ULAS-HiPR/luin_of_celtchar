# ULAS HiPR
Race 2 Space 2026: Lúin of Celtchar

## Overview

This repository contains some notebooks for using the 
[python wrapper](https://github.com/civilwargeeky/CEA_Wrap) for 
[NASA CEA](https://www.nasa.gov/glenn/research/chemical-equilibrium-with-applications/)

## Notebooks

### 01_single_problem.ipynb

This demonstrates setting up propellants and some basic parameters, running a single rocket problem, 
and accessing the results.

### 02_phi.ipynb

This runs multiple problems across a range of phi values to demonstrate looping
and accumulating results, plus some graphing techniques such as multiple
result parameters across a shared axis of the independent variable (phi in this case).

### 03_2_vars.ipynb

This runs problems across 2 independent variables, pivot tables the results and
projects onto both static and interactive graphs.

## Setup notes

Was difficult to get going on linux
Main bit is compiling the dan_cea for linux 
```bash 
gfortran -o Dan_CEA2 dan_cea2.f
```
and telling the wrapper to look there with 
```python 
import os
os.environ["CEA_USE_SITE_PACKAGES"] = '1'
from CEA_Wrap import Fuel, Oxidizer, RocketProblem
```
