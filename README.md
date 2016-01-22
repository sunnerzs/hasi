Hierachical Adaptive Soft Impute
======================================

HASI is an algorithm for low-rank matrix completion descibed in reference [1].
It uses nonconvex nuclear penalties arising from a hierarchical sparsity 
inducing prior on singular values.
The algorithm iteratively performs adaptive weighted soft thresholded SVD.

Applications are in Collaborative Filtering (predicting user preferences for 
items), image inpainting, imputation of missing values.

The software is distributed as a Matlab package. It makes use of the PROPACK 
algorithm for handling large scale matrices.

Getting started
---------------
1. Please see `demo_hasi.m` to see how to use HASI on an example.

2. To run the programs, folders `Matlab_files` and `PROPACK_utils` need to be in path.

3. Install mex files by running `install_mex` (details in `install_mex.m`).

Functions
---------
* `ha_soft_impute`: the main function that runs HASI algorithm (see [1]).

We also provide:

* `soft_impute`: runs Soft-impute algorithm (see [2]), special case of HASI 
    with `gamma` variant and infinite beta parameter.
* `hard_impute`: runs Hard-impute algorithm (see [2]).
* `spectral_norm`: computes the largest singular value of a sparse matrix.

Any function help is available via the command `help funcname`.

Authors
-------
HASI software was written by [Adrien Todeschini](http://adrtod.github.io) 
(<adrien.todeschini@inria.fr>).

HASI software is adapted from the [`Soft-Impute`](http://www.mit.edu/~rahulmaz/software.html) 
Matlab code written by [Rahul Mazumder](http://www.mit.edu/~rahulmaz/) with 
considerable input from [Trevor Hastie](https://web.stanford.edu/~hastie/) 
based on reference [2].

References
----------
[1]: "Probabilistic Low-Rank Matrix Completion with Adaptive Spectral Regularization Algorithms" 
by Adrien Todeschini, Francois Caron, Marie Chavent (NIPS' 2013)

[2]: "Spectral Regularization Algorithms for Learning Large Incomplete Matrices"
 by Rahul Mazumder, Trevor Hastie, Rob Tibshirani (JMLR vol 11, 2010)

Revisions
----------
- v1.0 : (2013-12-05) Original release

