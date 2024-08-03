# Patient motality prediction
SQL to pull time series data from ICU, Reduce feature with PCA and UMAP, build model by lightgbm, XGBoost, HistGradientBoosting

# Project objectives

1. Pulling data by SQL on Snowflakes with time series format from eICU to get patient vital signs and laboratory results
2. Perform EDA and clean up data
3. Apply feature reduction with PCA and UMAP for comparison
4. Build and test with multiple model LightGBM, XGBoost, HistGradientBoosting to predict patient motality after admitted to ICU


# Dataset

The data used for this study is from eICU [1] (v2.0, released in 2018). Along with MIMICIII, and MIMICIV, these are databases pulished by Massachusetts Institute of Technology (MIT) Laboratory for Computational Physiology. This collect patient information from the hospital that participated in the Philips eICU Program in the US. The data in eICU include patient demographic info, their dianoses, treatment note, vital signs and laboratory test result, etc..

Specifically for this eICU, you can see more details about this dataset structure in the website of [eICU Collaborative Research Database](https://eicu-crd.mit.edu/)

# Reference
[1] Pollard, T.J.; Johnson, A.E.W.; Raffa, J.D.; Celi, L.A.; Mark, R.G.; Badawi, O. The eICU Collaborative Research Database, a freely available multi-center database for critical care research. Sci. Data 2018, 5, 180178. [Google Scholar](https://scholar.google.com/scholar_lookup?title=The+APACHE+III+Prognostic+System:+Risk+Prediction+of+Hospital+Mortality+for+Critically+III+Hospitalized+Adults&author=Knaus,+W.A.&author=Wagner,+D.P.&author=Draper,+E.A.&author=Zimmerman,+J.E.&author=Bergner,+M.&author=Bastos,+P.G.&author=Sirio,+C.A.&author=Murphy,+D.J.&author=Lotring,+T.&author=Damiano,+A.&publication_year=1991&journal=Chest&volume=100&pages=1619%E2%80%931636&doi=10.1378/chest.100.6.1619) 

[2] Na Pattalung T, Ingviya T, Chaichulee S. Feature Explanations in Recurrent Neural Networks for Predicting Risk of Mortality in Intensive Care Patients. Journal of Personalized Medicine. 2021; 11(9):934. [DOI](https://doi.org/10.3390/jpm11090934/)

[3] Johnson, A.E.; Pollard, T.J.; Shen, L.; Lehman, L.W.H.; Feng, M.; Ghassemi, M.; Moody, B.; Szolovits, P.; Anthony Celi, L.;
Mark, R.G. MIMIC-III, a freely accessible critical care database. Sci. Data 2016, 3, 160035. [CrossRef] [PubMed]

[4] Johnson, A.; Bulgarelli, L.; Pollard, T.; Horng, S.; Celi, L.A.; Mark, R. MIMIC-IV (Version 0.4). PhysioNet. 2020. Available online:
https://physionet.org/content/mimiciv/0.4/ (accessed on 1 May 2021).

