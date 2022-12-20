<div align="center">

# Data Pipeline for Predictors Extraction based on Radiomics and Model Interpretation of the Brain

</div>

#### Authors: 

* Paulo Jorge Alves (paulojorgealves18@gmail.com); 

* Victor Alves (valves@di.uminho.pt)

* Tiago Gil Oliveira (tiagogiloliveira@gmail.com)

* Tiago Jesus (trajesus@hotmail.com)

#### Data pipeline: 

In the first stage, the segmentation of all exams are performed, with FreeSurfer. Once this segmentation is done, all radiomics features are extracted both from the original scans and from each desired zone. After the feature extraction, the datasets that will be used as input to the DL algorithm are created. With the application of the DL algorithm (XGBoost) and its interpretation, the desired predictors are obtained.

<div align="center">
  
![alt text](https://i.ibb.co/jLhhtc2/Screenshot-1.png)
  
</div>

#### Explanation of all the files created:

1 – Processa_dataset_inicial.ipynb: Pre-processing of the data extracted from the ADNI in order to create a reliable set of scans for the study.

2 – Check_scans&masks.ipynb: View all scans and their masks to confirm previous processing.

3 – processa_features_scans.ipynb: Extraction and processing of features from whole-brain scans.

4.0 – hipocamp_features_extract.ipynb: Extraction of features from the hippocampus.

4.1 – entorhinal_features_extract.ipynb: Extraction of entorhinal features.

4.2 – occipital_features_extract.ipynb: Extraction of lateraloccipital features.

5 – Processa_features_segments.ipynb: Processing of all the features extracted above, in the different zones.

6 – Histogram_Volum_Plots.ipynb: Compare the hippocampal volumes given by freesurfer with those of the respective features, in order to validate them.

7.0 – XGBOOST_scanCompleto.ipynb; 
7.1 – XGBOOST_hipocampo.ipynb; 
7.2 – XGBOOST_entorhinal.ipynb; 
7.3 – XGBOOST_occipital.ipynb: 
Apply XGBoost to the data, by cross-validation. Obtain the confusion matrix, Shap-Values and Feature Importance plots - this for each of the regions, where hyperparameters are adjusted for each data set.

<div align="center">
  
#### To have access to the dataset, please request by e-mail to the authors.
  
</div>
