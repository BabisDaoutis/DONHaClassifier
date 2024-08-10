# DONHa classifier

The DONHa (D4000, [OIII], [NII], and Hα) activity classsifer - decomposing galaxy activity

A Random Forest-based, 4-dimensional galaxy activity classifier 

Repository for galaxy activity clasifier from the paper "Novel diagnostic methods for resolving galaxy activity: From
seagull to hummingbird"\
Astronomy & Astrophysics\
ArXiv: \
ADS:  \
Publisher (A&A): 

**Authors:**\
C. Daoutis, A. Zezas, E. Kyritsis, K. Kouroumpatzakis, and P. Bonfini

### Abstract 
**Context.**  One of the principal challenges in astrophysics involves the classification of galaxies based on their activity. Presently, the characterization of galactic activity relies on diagnostics that do not fully cover the diverse spectrum of galaxy activity types. Additionally, degeneracies arising from the selected discriminating features hinder the attainment of a definitive characterization, particularly in the case of galaxies exhibiting mixed activity.\
**Aims.**  In this study, our objective is to develop an activity diagnostic tool that addresses the degeneracy inherent in the existing emission line diagnostics by identifying and decomposing the underlying excitation mechanisms of a mixed-activity galaxy into three principal components: star formation, active nucleus, or old stellar populations.\
**Methods.** We utilize the random forest machine-learning algorithm, trained on three primary activity classes of star-forming, active galactic nucleus (AGN), and passive, that represent the three key gas excitation mechanisms. This diagnostic relies on four discriminating features: the equivalent widths of three spectral lines-[OIII]λ5007, [NII]λ6584, and Hα-along with the D4000 continuum break index. \
**Results.**  We find that this classifier achieves almost perfect performance scores in the principal activity classes. In particular, the achieved overall accuracy is ~99%, while the recall scores are: ~100% for star-forming, ~98% for AGN, and ~99 for passive. The nearly perfect scores achieved enable the decomposition of mixed activity classes into the three primary gas excitation mechanisms with high confidence, thereby resolving the degeneracy inherent in current activity classification methods. Furthermore, we find that our classifier scheme can be simplified to a two-dimensional diagnostic diagram of D4000 against log(EW([OIII])^2) without significant loss of its diagnostic power.\
**Conclusions.** We have introduced a diagnostic capable of classifying galaxies based on their primary gas excitation mechanisms. Simultaneously, it can deconstruct the activity of mixed-activity galaxies into these principal components. This diagnostic encompasses the entire range of galaxy activity, providing enhanced resolution in terms of activity classification. Additionally, D4000 serves as a valuable indicator for resolving the degeneracy among various activity components by estimating the age of the stellar populations within a galaxy.

### Application of the model

This repository includes all the necessary files and a Jupyter notebook as an example of application. The pre-trained random forest model for implementing the algorithm described in the referenced paper is the 'DONHa_classifier.sav'. We have provided a test file named 'test_sample_galaxies.csv' to verify that your code is functioning correctly. To classify the activity of galaxies in your own catalog, simply replace this test file with your catalog. Supported formats for your catalog are 'fits' or 'csv'.

- **Output of classifier**\
Once the model has been applied to your galaxy catalog, a new column labeled 'classification' will show each galaxy's activity class. The classification labels are encoded numerically, with each number representing a distinct activity class. Below is a legend explaining the meaning of these numerical codes. \
**Classification legend** \
0 - Pure star forming \
1 - Pure AGN \
2 - Pure passive \
3 - Starburst-AGN \
4 - AGN-starburst \
5 - Starburst-passive \
6 - Passive-starburst \
7 - Passive-AGN \
8 - AGN-passive \
-1 - Unclassified (no result) 
  
For more detailes about the definition of each activity classes see Table 3 of the paper. 

Given the significant dependency on specific versions of Python packages, we recommend that users create a conda environment where all required packages are installed according to the versions with which this code has been successfully tested. Detailed instructions for creating the appropriate conda environment are provided below:

```
conda create --name DONHaclassifier python==3.11.5
conda activate DONHaclassifier
conda install scikit-learn==1.4.0
conda install astropy==5.3.3
conda install matplotlib==3.7.3
conda install pandas==2.2.2
conda install jupyter notebook
```
