# Two-Step Algorithm for Cyclic Causal Systems

Matlab functions to run the ICA-based **Two-Step algorithm** introduced in Sanchez-Romero, R., Ramsey, J. D., Zhang, K., Glymour, M. R., Huang, B., & Glymour, C. (2019). [Estimating feedforward and feedback effective connections from fMRI time series: Assessments of statistical methods](https://doi.org/10.1162/netn_a_00061). Network Neuroscience, 3(2), 274-306.

(See paper main repository for other resources, https://github.com/cabal-cmu/Feedback-Discovery)

The Two-Step algorithm was designed and applied to fMRI data but can be applied to other non-Gaussian, linear problems. See paper for details.

## Implementation

**Input**: a dataset X of non-Gaussian variables, together with a positive value for the regularization parameter, lambda.

**Output**: matrix B of causal coefficient estimates, from X = BX + E. 

In matrix B, the causal direction goes from column to row, such that a matrix entry Bij, implies Xj --> Xi

two_step_CD.m  runs Two-Step with Adaptative Lasso as a first step, using lambda to control the regularization.

two_step_CD_mask.m  should be used if the adjacency matrix of the first step was computed with some other algorithm.
