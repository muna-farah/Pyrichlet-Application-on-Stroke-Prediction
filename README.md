# Bayesian Nonparametric Clustering - Stroke Prediction

**Author:** Muna Farah  
*Data Science Master's Candidate | B.S. in Public Health*

This project applies the **Dirichlet Process Mixture (DPM)** model from the `pyrichlet` package to the Stroke Prediction Dataset from Kaggle. Using Bayesian nonparametric methods, this analysis performs density estimation and discovers patient clusters without pre-specifying the number of groups.

## Contents
* **Exploratory Data Analysis (EDA):** Examination of stroke rates by smoking status, residence type, and gender.
* **DPM Modeling:** Implementation of Gibbs sampling with slice sampling to infer patient subgroups.
* **Visualizations:** Cluster assignment maps with uncertainty quantification and posterior predictive density estimation.
* **Stability Analysis:** Evaluation of model consistency across multiple random seeds and subset sizes (N=1000, 2000, 5000).
* **Performance Metrics:** Comparison of clustering stability using Mutual Information (MI), Adjusted Mutual Information (AMI), and Normalized Mutual Information (NMI).

## Key Findings
* The model identified a high-risk cluster with a **12.15% stroke rate**, significantly higher than the 4.9% baseline.
* BMI and average glucose level were stronger drivers of cluster separation than age.
* Cluster structures become increasingly stable at larger sample sizes (N=5000), with AMI values approaching 1.0.
* Assignment uncertainty was highest at the boundaries of clinical markers, where patient profiles naturally overlap.

## Files
* `Stroke Analysis.ipynb` – The Jupyter Notebook. 
* `Bayesian Nonparametric Stroke.qmd` – The Quarto analysis file.
* `Bayesian Nonparametric Stroke.html` – The rendered report.
* `healthcare-dataset-stroke-data.csv` – The Kaggle dataset used for analysis.
* `selva2024pyrichlet.pdf` – Reference paper for the `pyrichlet` implementation.

## Data Source
The dataset used in this project is sourced from the [Kaggle Stroke Prediction Dataset](https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset).

## References
Selva, F., Fuentes-García, R., & Gil-Leyva, M. F. (2025). pyrichlet: A Python Package for Density Estimation and Clustering Using Gaussian Mixture Models. *Journal of Statistical Software*, 112(8). https://doi.org/10.18637/jss.v112.i08
