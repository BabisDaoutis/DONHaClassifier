# DONHa_classifier

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
**Methods.** We utilize the random forest machine-learning algorithm, trained on three primary activity classes of star-forming, active galactic nucleus (AGN), and passive, that represent the three key gas excitation mechanisms. This diagnostic relies on four discriminating features: the equivalent widths of three spectral lines--[OIII]λ5007, [NII]λ6584, and Hα--along with the D4000 continuum break index. \
**Results.**  We find that this classifier achieves almost perfect performance scores in the principal activity classes. In particular, the achieved overall accuracy is $\sim$99\%, while the recall scores are: $\sim$100\% for star-forming, $\sim$98\% for AGN, and ~99 for passive. The nearly perfect scores achieved enable the decomposition of mixed activity classes into the three primary gas excitation mechanisms with high confidence, thereby resolving the degeneracy inherent in current activity classification methods. Furthermore, we find that our classifier scheme can be simplified to a two-dimensional diagnostic diagram of D4000 against $ \log_{10}(\mathrm{EW}([\ion{O}{III}])^{2}) $ without significant loss of its diagnostic power.\
**Conclusions.** We have introduced a diagnostic capable of classifying galaxies based on their primary gas excitation mechanisms. Simultaneously, it can deconstruct the activity of mixed-activity galaxies into these principal components. This diagnostic encompasses the entire range of galaxy activity, providing enhanced resolution in terms of activity classification. Additionally, D4000 serves as a valuable indicator for resolving the degeneracy among various activity components by estimating the age of the stellar populations within a galaxy.

### Application of the model

