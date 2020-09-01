# PEER_STAR_NET
This is the repository for Pacific Earthquake Engineering Research Center (PEER) STructural Acceleration Response Network (STAR-Net). 

## Organization
Time Series data stored as a 2-D array in the form of `*.npy` files. Unless otherwise specified, each column of the 2-D array corresponds to the records of one location, while each row of the 2-D array corresponds to the records of a time step. Therefore, the shape of 2-D array is `(steps, sensors)`. 

```
import numpy as np
```

to import the package `numpy`. Then, the data is loaded using:

```
data = np.load("*.npy")
```

where `*.npy` is the name of the `.npy` file to be loaded. The data is stored in the 2-D array variable `data`. The users could use the indexing syntax of Python to retrieve segments if needed. For example, the users could retrieve the segment in the step range of `[i,j)` where i < j by:

```data[i:j]```

## Notice of use
Users who use the data from repository should acknowledge Pacific Earthquake Engineering Research Center (PEER). 
