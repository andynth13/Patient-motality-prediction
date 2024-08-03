# Patient motality prediction
SQL to pull time series data from ICU, Reduce feature with PCA and UMAP, build model by lightgbm, XGBoost, HistGradientBoosting

# Project objectives

1. Pulling data by SQL on Snowflakes with time series format from eICU to get patient vital signs and laboratory results
2. Perform EDA and clean up data
3. Apply feature reduction with PCA and UMAP for comparison
4. Build and test with multiple model LightGBM, XGBoost, HistGradientBoosting to predict patient motality after admitted to ICU


# Dataset

The data used for this study is from eICU [1] (v2.0, released in 2018). This is a critical care database of more than 200,000 intensive care stays collected between 2014 and 2015 from hospitals in the United States that participate in the Philips eICU Program. The database contains demographics, diagnoses, treatment information, care plan documents, vital signs, laboratory tests, doctor notes, etc.

# Reference
[1] Pollard, T.J.; Johnson, A.E.W.; Raffa, J.D.; Celi, L.A.; Mark, R.G.; Badawi, O. The eICU Collaborative Research Database, a freely available multi-center database for critical care research. Sci. Data 2018, 5, 180178. [Google Scholar](https://scholar.google.com/scholar_lookup?title=The+APACHE+III+Prognostic+System:+Risk+Prediction+of+Hospital+Mortality+for+Critically+III+Hospitalized+Adults&author=Knaus,+W.A.&author=Wagner,+D.P.&author=Draper,+E.A.&author=Zimmerman,+J.E.&author=Bergner,+M.&author=Bastos,+P.G.&author=Sirio,+C.A.&author=Murphy,+D.J.&author=Lotring,+T.&author=Damiano,+A.&publication_year=1991&journal=Chest&volume=100&pages=1619%E2%80%931636&doi=10.1378/chest.100.6.1619) 

[2] Na Pattalung T, Ingviya T, Chaichulee S. Feature Explanations in Recurrent Neural Networks for Predicting Risk of Mortality in Intensive Care Patients. Journal of Personalized Medicine. 2021; 11(9):934. [DOI](https://doi.org/10.3390/jpm11090934/)

