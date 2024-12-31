# Two-Step Algorithm for Cyclic Causal Systems

Matlab functions to run the ICA-based **Two-Step algorithm** introduced in Sanchez-Romero, R., Ramsey, J. D., Zhang, K., Glymour, M. R., Huang, B., & Glymour, C. (2019). [Estimating feedforward and feedback effective connections from fMRI time series: Assessments of statistical methods](https://doi.org/10.1162/netn_a_00061). Network Neuroscience, 3(2), 274-306. 

The algorithm was designed and applied to fMRI data but can be applied to other non-Gaussian, linear problems.

**Input**: a dataset X of non-Gaussian variables, together with a positive value for the regularization parameter, lambda.

**Output**: B matrix of causal coefficients, from X = BX + E. 

In B, the causal direction goes from column to row, such that a matrix entry Bij, implies Xj --> Xi

two_step_CD.m  runs Two-Step with Adaptative Lasso as a first step, using lambda to control the regularization.

two_step_CD_mask.m  should be used if the adjacency matrix of the first step was computed with some other algorithm.
