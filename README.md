# PyLops - sliding and patching benchmarking

This repository contains an extensive benchmarking suite for the new implementations of PyLops sliding and patching operators. Notebooks and summary tables of timings of the old and new implementations are provided.


## Summary tables

**NumPy**

| Operator                |      Old (ms)     |      New (ms)      | New broad. (ms)  |
|-------------------------|-------------------|--------------------|------------------|
| Sliding1D               |       24.2        |     12.6           |   **1.5**        |
| Sliding1D.H             |       13.2        |     7.65           |    **0.353**     |
| Sliding2D               |       200         |     20.7           |  **16.2**        |
| Sliding2D.H             |       1160        |     537            |   **423**        |
| Sliding3D               |       1620        |     20.7           |      **16.2**    |
| Sliding3D.H             |       674         |     446            |  **205**         |
| Patching2D              |       108         |     **50**         |      64.8        |
| Patching2D.H            |       59.7        |     **41.3**       |      81          |
| Patching3D              |       1880        |    **587**         |     759          |
| Patching3D.H            |       1170        |     796            |       **491**    |

**CuPy (only GPU time - RTX 3090)**

| Operator                |      Old (ms)     |      New (ms)      | New broad. (ms)  |
|-------------------------|-------------------|--------------------|------------------|
| Sliding1D               |        
| Sliding1D.H             |        
| Sliding2D               |                   |                    |                  |
| Sliding2D.H             |                   |                    |                  |
| Sliding3D               |        338        |      303           |    **14**        |
| Sliding3D.H             |        216        |      189           |    **2.3**       |
| Patching2D              |                   |                    |                  |
| Patching2D.H            |                   |                    |                  |
| Patching3D              |        104        |    80.8            |      **7.2**     |
| Patching3D.H            |        67.1       |    41.3            |      **6.9**     |


## TO DO

- [ ] Include option not to store the entire set of tapers but apply them one by one (slower but more memory efficient)