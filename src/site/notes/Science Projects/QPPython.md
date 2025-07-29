---
{"dg-publish":true,"permalink":"/science-projects/qp-python/"}
---


## What?

Python implementation of the core functionality of;

**QPPLab: A generally applicable software package for detecting, analyzing, and visualizing large-scale quasiperiodic spatiotemporal patterns (QPPs) of brain activity**

published here: [https://www.ncbi.nlm.nih.gov/pmc/articles/PMC10557593/](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC10557593/)

and maintained here: [https://github.com/GT-EmoryMINDlab/QPPLab](https://github.com/GT-EmoryMINDlab/QPPLab)

Aside from having been written in Matlab, the original package enforces a lot of custom data structures both for inputs and outputs. This one does not. We also made what we believe to be some improvements on the algorithm (e.g. better sliding window implementations requiring less memory).

---
## Usage

The **find_qpp(data,qpp_template)** function carries out the main analysis.

Given:
- a 2d numpy array of shape (# of features/channels/voxels, # of timepoints) that stores the multivatiate timeseries data,
- and a 2d numpy array of shape (# of features/channels/voxels, # of timepoints in QPP window) that stores the initially guessed QPP pattern

the function returns:
- the final QPP pattern
- and it's sliding window similarity to the whole timeseries data.

### Preparing your data

Any multivariate timeseries data that is stored in a 2d numpy array of shape (# of features/channels/voxels, # of timepoints) can be used as input.
### QPP parameters

The QPP window size is inferred from the shape of the initial QPP template provided.

---
See more [here on github](https://github.com/drgzkr/QPPython), and [here as a development notebook](https://colab.research.google.com/drive/13zPfqNZjsMoEvU3zeUjIEppcRAtDOXa4?usp=sharing).

