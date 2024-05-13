# PyLops - sliding and patching benchmarking

This repository contains an extensive benchmarking suite for the new implementations of PyLops sliding and patching operators. Notebooks and summary tables of timings of the old and new implementations are provided.


## Summary tables

**Numpy**

| Operator                |      Old (ms)     |      New (ms)      | New broad. (ms)  |
|-------------------------|-------------------|--------------------|------------------|
| Sliding1D               |       24.2        |     12.6           |       1.5        |
| Sliding1D.H             |       13.2        |     7.65           |      0.353       |
| Sliding2D               |       200         |     20.7           |      16.2        |
| Sliding2D.H             |       11.6        |     8.65           |      5.58        |


## TO DO

- [ ] Include option not to store the entire set of tapers but apply them one by one (slower but more memory efficient)