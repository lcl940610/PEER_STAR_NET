# PEER_STAR_NET
This is the repository for [Pacific Earthquake Engineering Research Center (PEER)](https://peer.berkeley.edu/) STructural Acceleration Response Network (STAR-Net, or ★-Net), which includes the collected recorded acceleration responses of structures under seismic ground motions in the form of Time Series. The dataset is used primarily for the experiment on the Machine Learning based Structural Health Monitoring damage detections. Performances could be compared using different algorithms over the same dataset.

## Data Source
The data mainly comes from two resources. The first resource is the the recorded data from real structures or lab experiments (e.g., the recorded responses from the [Center for Engineering Strong Motion Data (CESMD)](https://strongmotioncenter.org/)). The second source is the numerical simulations using Finite Element Model (FEM) software (e.g., [DIANA FEA](https://dianafea.com/) and [OpenSees](https://openseespydoc.readthedocs.io/en/latest/)). 

## Format
Each folder in this repository contains the data from one structure. Time Series data is standardized and is stored as a 2-D array in the form of `*.npy` files. Unless otherwise specified, each column of the 2-D array corresponds to the records of one location, while each row of the 2-D array corresponds to the records of a time step. Therefore, the shape of 2-D array is `(steps, sensors)`. 

```
import numpy as np
```

to import the package `numpy`. Then, the data is loaded using:

```
data = np.load("*.npy")
```

where `*.npy` is the name of the `.npy` file to be loaded. The data is stored in the 2-D array variable `data`. The users could use the indexing syntax of Python to retrieve segments if needed. For example, the users could retrieve the segment in the step range of `[i,j)` where i < j by:

```
data[i:j]
```
In addition to the `.npy` files, for each structure, a `README.md` file is present to include the general information, including but not limited to the description of the structure, damage states, and the sources of data (e.g., measured from real sensors or simulted using FEM software). 

Users could make personalized processing of data. For example, users could split the training/validation/test datasets by using external functions (e.g., function `train_test_split` defined in Python toolkit `scikit-learn`). The users could also created personalized dataset labels based on the descriptions in the `README.md`.

## Notice of use
Users who use the data from repository should acknowledge Pacific Earthquake Engineering Research Center (PEER). 
