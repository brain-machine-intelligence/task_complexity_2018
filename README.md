[![DOI](https://zenodo.org/badge/145090153.svg)](https://zenodo.org/badge/latestdoi/145090153)

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


## Acknowledgement

This work was funded by grants R01DA033077 and R01DA040011 to J.P.O.D. from the National Institute on Drug Abuse. This work was also supported by Institute of Information & Communications Technology Planning & Evaluation(IITP) grant funded by the Korea government (MSIT) (No. 2019-0-01371, Development of brain-inspired AI with human-like intelligence) (No. 2017-0-00451, Development of BCI based Brain and Cognitive Computing Technology for Recognizing User’s Intentions using Deep Learning), the ICT R&D program of MSIP/IITP (No. 2016-0-00563, Research on Adaptive Machine Learning Technology Development for Intelligent Autonomous Digital Companion), the National Research Foundation of Korea (NRF) grant funded by the Korea government (MSIT) (No. NRF-2019M3E5D2A01066267), and Samsung Research Funding Center of Samsung Electronics under Project Number SRFC-TC1603-06.

