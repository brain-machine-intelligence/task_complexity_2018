Simulation code for the computational model of arbitration and fMRI results

## 1. Simulation Code : main.m

This will generate a file for each subject in modelRLsource/result_simul. Every simulation file(.mat) contains SBJ structure variable. SBJ{1, 1}.model_BayesArb.param is the optimized free parameters, and SBJ{1, 1}.model_BayesArb.val is sum of negative log likelihood for each subject. 

main.m contains following functions.

### 1.1. Model fitting

Negative log likelihood was calculated for each action, using softmax function with action value (Q). Free parameters are optimized to minimize the sum of negative log likelihood (which means better estimation of human actions) using Nelder-Mead simplex algorithm. For more details, please refer to the supplementary document of Lee et al. (Neuron, 2014). Especially, "Parameter Estimation" section in supplementary methods explains all the details for inferring parameters.

The sum of negative log likelihood further used to calculate BIC and model comparison (RFX BMS).

### 1.2. Generating regressors

Generates regressor that is in the supplementary document of our manuscript.


## 2. Group effect fMRI results : ./group_effect_fmri

## 3. Task files : ./task_complexity 

To perform an experiment, you must install psychtoolbox first. After the installation, run SIMUL_main.m line-by-line. 

## etc. Please refer to appendix file for the additional analysis!
