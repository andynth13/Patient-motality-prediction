# Patient motality prediction
SQL to pull time series data from ICU, Reduce feature with PCA and UMAP, Build model by lightgbm, XGBoost, HistGradientBoosting

# Skill demontration

* Proficiency in **SQL** and **Snowflake** for complex data extraction and transformation.
* Strong **analytical skills** in EDA and data preprocessing, ensuring high-quality input for modeling.
* Advanced knowledge of machine learning algorithms (LightGBM, XGBoost, HistGradientBoosting) and model evaluation methods.
* Ability to manage and interpret **time-series data** for critical clinical predictions.


# About Dataset

The data used for this study is from eICU [1] (v2.0, released in 2018). Along with MIMICIII, and MIMICIV, these are databases pulished by Massachusetts Institute of Technology (MIT) Laboratory for Computational Physiology. This collect patient information from the hospital that participated in the Philips eICU Program in the US. The data in eICU include patient demographic info, their dianoses, treatment note, vital signs and laboratory test result, etc..

Specifically for this eICU, you can see more details about this dataset structure in the website of [eICU Collaborative Research Database](https://eicu-crd.mit.edu/)

# Result

1. The model achieved high predictive performance, especially with 28 features from 3 groups: patient demographics, their vital signs and their lab test result.
2. SHapley Additive exPlanation (SHAP) is an useful method to indicate the most significant features contributing to mortality predictions, such as vital signs like systolic blood pressure, heart rate, and SpO2, as well as laboratory values like platelet count and blood urea nitrogen (BUN).
3. Temporal features are crucial in this case, noting that measurements taken closer to the end of the observation window (when patient discharged from ICU) had a larger impact on mortality predictions.
4. The findings are consistent with clinical knowledge, indicating that the models and the interpretability method used (SHAP) provided valuable insights into patient conditions and could potentially help with the clinical decision-making.


# Lesson learn

* Explore and utilize other models that are suitable to handle time-series data, such as CNN-RNN Hybrids, Transformer model.
* Document the steps for pulling data in a clear, detailed, and organized manner.


# Reference
[1] Pollard, T.J.; Johnson, A.E.W.; Raffa, J.D.; Celi, L.A.; Mark, R.G.; Badawi, O. The eICU Collaborative Research Database, a freely available multi-center database for critical care research. Sci. Data 2018, 5, 180178. [Google Scholar](https://scholar.google.com/scholar_lookup?title=The+APACHE+III+Prognostic+System:+Risk+Prediction+of+Hospital+Mortality+for+Critically+III+Hospitalized+Adults&author=Knaus,+W.A.&author=Wagner,+D.P.&author=Draper,+E.A.&author=Zimmerman,+J.E.&author=Bergner,+M.&author=Bastos,+P.G.&author=Sirio,+C.A.&author=Murphy,+D.J.&author=Lotring,+T.&author=Damiano,+A.&publication_year=1991&journal=Chest&volume=100&pages=1619%E2%80%931636&doi=10.1378/chest.100.6.1619) 

[2] Na Pattalung T, Ingviya T, Chaichulee S. Feature Explanations in Recurrent Neural Networks for Predicting Risk of Mortality in Intensive Care Patients. Journal of Personalized Medicine. 2021; 11(9):934. [DOI](https://doi.org/10.3390/jpm11090934/)

[3] Johnson, A.E.; Pollard, T.J.; Shen, L.; Lehman, L.W.H.; Feng, M.; Ghassemi, M.; Moody, B.; Szolovits, P.; Anthony Celi, L.;
Mark, R.G. MIMIC-III, a freely accessible critical care database. Sci. Data 2016, 3, 160035. [CrossRef] [PubMed]

[4] Johnson, A.; Bulgarelli, L.; Pollard, T.; Horng, S.; Celi, L.A.; Mark, R. MIMIC-IV (Version 0.4). PhysioNet. 2020. Available online:
https://physionet.org/content/mimiciv/0.4/ (accessed on 1 May 2021).

