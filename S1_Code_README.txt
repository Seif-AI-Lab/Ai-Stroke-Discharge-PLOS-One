S1 Code README
===============

Manuscript title
----------------
An Explainable Artificial Intelligence Framework for Clinical Decision Support in Stroke Discharge Planning

Supplementary code file
-----------------------
Plos_One__Discharge_Disposition__code.ipynb

Purpose of the code
-------------------
This supplementary notebook provides the analysis code used for the stroke discharge disposition study. The code includes dataset preparation, descriptive and bivariate analyses, exploratory age ECDF and PCA visualizations, final multilayer perceptron (MLP) model development, probability calibration, hold-out test-set evaluation, and SHapley Additive exPlanations (SHAP)-based model interpretation.

The code is provided for transparency and reproducibility of the reported analyses. It is not intended to serve as a clinical deployment tool or bedside decision-support application.

Required input file
-------------------
The notebook expects the original dataset file to be available in the working directory:

    StrokeDataRepositoryV3.xlsx

The dataset is publicly available as described in the manuscript Data Availability statement:

	2026, "Complete Stroke Data Repository V 3.0", Harvard Dataverse, V1.
    	https://doi.org/10.7910/DVN/OYNYB4

If running the notebook in Google Colab, upload the dataset file to the Colab working directory before executing the notebook cells.

Computing environment
---------------------
The analyses were performed using Google Colab Pro+ with a high-memory CPU environment. The analysis pipeline was implemented in Python 3.11.2.

Main Python packages
--------------------
The notebook uses the following Python packages:

    numpy
    pandas
    scipy
    scikit-learn
    matplotlib
    shap
    joblib
    openpyxl
    pillow
    IPython

Recommended installation command
--------------------------------
If the required packages are not already installed, they can be installed with:

    pip install numpy pandas scipy scikit-learn matplotlib shap joblib openpyxl pillow

How to run the notebook
-----------------------
1. Open Plos_One__Discharge_Disposition__code.ipynb in Google Colab or Jupyter Notebook.
2. Place StrokeDataRepositoryV3.xlsx in the working directory.
3. Run the notebook cells sequentially from top to bottom.
4. Review the generated output files and figures in the working directory.

Major analysis sections
-----------------------
The notebook is organized into the following major sections:

1. Dataset creation and variable harmonization
2. Bivariate analysis of discharge disposition outcomes
3. Age empirical cumulative distribution function (ECDF) visualization
4. Exploratory three-dimensional principal component analysis (PCA)
5. Final MLP model development, tuning, calibration, evaluation, and SHAP interpretation

Primary expected outputs
------------------------
Depending on the local working directory and execution settings, the notebook generates outputs such as:

    StrokeData_ML_dataset.xlsx
    StrokeData_ML_summary.xlsx
    Bivariate analysis Excel output
    ECDF figure
    PCA figure
    Final MLP model performance results
    ROC curve figure
    Confusion matrix figure
    Learning curve figure
    Calibration curve figure
    SHAP summary plots
    SHAP age-threshold plots
    Serialized final MLP pipeline object
    Serialized probability-calibration object

Reproducibility notes
---------------------
- The target outcome is discharge disposition with four categories: home, specialized care, home with help, and expired.
- The final selected MLP model uses the prespecified clinical predictors described in the manuscript.
- Hyperparameter tuning is performed within the training set using stratified cross-validation, with macro-F1 as the primary selection metric.
- Probability calibration and class-specific threshold tuning are performed using out-of-fold predictions from the training set only.
- The independent hold-out test set is used only for final model evaluation and post hoc SHAP interpretation.
- Missing values are handled within the modeling pipeline using a MICE-style iterative imputation procedure with 30 iterations.
- Random seeds are set in the notebook where applicable to improve reproducibility. Small numerical differences may occur across software versions or computing environments.

Computational requirements
--------------------------
The final MLP hyperparameter search and SHAP analysis can be computationally intensive. Running the notebook in a high-memory environment is recommended. The shared notebook uses a computationally streamlined hyperparameter-search configuration to facilitate practical rerunning.

Data privacy
------------
The input dataset used by this code is the de-identified dataset described in the manuscript Data Availability statement. No direct patient identifiers are required by the notebook.

Contact
-------
For questions about the analysis code, please contact the corresponding author listed in the manuscript.
