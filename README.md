# Project 'je_ub'

This repo ensures the source codes for the "Determining the Uncertain Boundaries of the Diagnostics Tests by Using Information Criteria" manuscript. 

# Abstract of the Manuscript

The decision-making process in medicine often concludes with binary outcomes, determining whether a person has a medical condition and requires treatment or not. Various sources of information, such as patient complaints, symptoms, and diagnostic tests are utilized to rule-in or rule-out potential diseases. Despite certain diagnostic tests having limitations in perfectly discriminating between subjects, they are widely used in clinics due to their efficiency. Using a single cut-off value for classifying subjects in ordinal and quantitative diagnostic tests may lead to challenges when the distributions of diseased and healthy subjects overlap. This binary approach, particularly in the overlapped region, can result in false negatives and positives. For this uncertainty, there exist various approaches known as a "gray zone" or "middle inconclusive area." In this study, we intend to propose a novel solution for the boundaries of the gray zone based on an information theory. Thus, we aimed to compare the performance of this proposed solution against existing methods. For equal variances, the proposed algorithm consistently achieves the smallest length of the gray zone in simulations. For unequal variances, it outperforms in certain cases. Yet, it has such an advantage that there is no prior information for the proposed algorithm.

# The Information About Simulation Scenarios in the Manuscript

The simulation scenarios were based on the combinations of the below factors. 

1) Sample size (n): {50, 100 and 200} To investigate the effect of sample size on the distributions of diagnostic tests, the total sample sizes of Y<sub>C</sub> and Y<sub>D</sub> (the distributions of non-diseased and diseased groups, respectively) were changed.

2)Prevalence of the disease (P(D)): {0.2, 0.5 and 0.8} To learn how the distribution of diagnostic test results vary with disease prevalence, several disease prevalences were examined.

3)Ratio of variances: {1 and 3} To evaluate the impact of variability on the distributions, the ratio of variances between the diseased group ( Y<sub>D</sub>) and the non-diseased group ( Y<sub>C</sub>) was adjusted. The ratio of the sick group's deviations to those of the unaffected group was taken into account.

4)Effect size (d): {0.5 0.8 and 1.2} It was employed to measure the degree to which the  Y<sub>C</sub> and  Y<sub>D</sub> distributions overlapped or were near one another. This made it possible to comprehend the diagnostic test results' discriminative ability better.

Table: The Values for AUROC with Effect Sizes   

|Effect Size|-----------|Interval of AUROC|    

|d=0.5      |-----------|   68% to 70%    |

|d=0.8      |-----------| 	76% to 78%    |

|d=1.2 	    |-----------|   84% to 86%    |

# The R files:

1)	greyzone: The function for greyzone adapted for simulation scenarios. Please use this function before run for simulation_codes.R files. 
2)	info_distance_based_function: The function for proposed algorithm based on Euclidian distance.
3)	info_distance_based_simulation_function: The function for proposed algorithm based on Euclidian distance for simulation scenarios. Please use this function before run for simulation_codes.R files. 
4)	info_kernel_based_function: The function for proposed algorithm based on kernel-smoothed densities.
5)	info_kernel_based_simulation_function: The function for proposed algorithm based on kernel-smoothed densities for simulation scenarios. Please use this function before run for simulation_codes.R files. 
6)	simulation_codes: The codes for simulation scenarios. 

# References

1) Coste J, Pouchot J. A grey zone for quantitative diagnostic and screening tests. International journal of epidemiology. 2003;32(2):304–313.
2) Landsheer JA. Interval of uncertainty: an alternative approach for the determination of decision thresholds, with an illustrative application for the prediction of prostate cancer. PloS one. 2016;11(11):e0166007.
3) Landsheer H.: UncertainInterval: Uncertain Interval Methods for Three-Way Cut-Point Determination in Test Results. R Package Version 0.7. 0.
4) Wickham H. ggplot2: elegant graphics for data analysis. Springer; 2016

# Contact Information
ebru.ztrk3@gmail.com or ebru.ozturk3@hacettepe.edu.tr
