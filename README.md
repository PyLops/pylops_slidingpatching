# PyLops - sliding and patching benchmarking

This repository contains an extensive benchmarking suite for the new implementations of PyLops sliding and patching operators. Notebooks and summary tables of timings and memory uses of the old and new implementations are provided.

These numbers have been computed using an Intel(R) Xeon(R) Gold 6230R CPU @ 2.10GHz with an NVIDIA GeForce RTX 3090 GPU.


## Time-to-solution summary tables (New: with savetaper=True - fast option)

**NumPy**

| Operator                |      Old (ms)     |      New (ms)      | New broad. (ms)  |
|-------------------------|-------------------|--------------------|------------------|
| Sliding1D               |       24.2        |     12.6           |   **1.5**        |
| Sliding1D.H             |       13.2        |     7.65           |    **0.353**     |
| Sliding2D               |       200         |     20.7           |  **16.2**        |
| Sliding2D.H             |       10.8        |     8              |   **5.1**        |
| Sliding3D               |       1620        |     20.7           |      **16.2**    |
| Sliding3D.H             |       674         |     446            |     **205**      |
| Patching2D              |       108         |     **50**         |      64.8        |
| Patching2D.H            |       59.7        |     **41.3**       |      81          |
| Patching3D              |       1880        |    **587**         |     759          |
| Patching3D.H            |       1170        |     796            |       **491**    |

**CuPy (only GPU time using cupyx.profiler.benchmark)**

| Operator                |      Old (ms)     |      New (ms)      | New broad. (ms)  |
|-------------------------|-------------------|--------------------|------------------|
| Sliding1D               |        X          |         X          |        X         |       
| Sliding1D.H             |        X          |         X          |        X         |
| Sliding2D               |      66.8         |     60.2           |      **5**       |
| Sliding2D.H             |       47          |       32           |     **0.5**      |
| Sliding3D               |        338        |      303           |    **14**        |
| Sliding3D.H             |        216        |      189           |    **2.3**       |
| Patching2D              |        219        |       173          |    **17.8**      |
| Patching2D.H            |        160        |     96             |    **0.67**      |
| Patching3D              |        104        |    80.8            |      **7.2**     |
| Patching3D.H            |        67.1       |    41.3            |      **6.9**     |


## Memory tables (New: with savetaper=True/False)

| Operator                |      Old (Mb)     |      New (Mb)      | New broad. (Mb)  |
|-------------------------|-------------------|--------------------|------------------|
| Sliding1D               |       1.2         |  0.13/**0.016**    |  0.13/**0.016**  |
| Sliding2D               |                   |                    |                  |
| Sliding3D               |       1.1         |      207/2.89      |    207/2.89      |
| Patching2D              |                   |                    |                  |
| Patching3D              |                   |                    |                  |
