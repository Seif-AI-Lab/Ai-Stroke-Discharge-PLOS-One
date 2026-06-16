# Ai-Stroke-Discharge-PLOS-One

Analysis code for the manuscript:

**An Explainable Artificial Intelligence Framework for Clinical Decision Support in Stroke Discharge Planning**

This repository contains the analysis notebook and serialized model-related artifacts used for explainable AI-based prediction of discharge disposition following acute stroke.

## Repository contents

* `Plos_One__Discharge_Disposition__code.ipynb`: Main analysis notebook.
* `S1_Code_README.txt`: Supplementary code documentation.
* `final_macro_f1_model_pipeline.joblib`: Serialized final model pipeline artifact.
* `final_macro_f1_model_probability_calibrator.joblib`: Serialized probability calibration artifact.
* `requirements.txt`: Python package requirements.
* `LICENSE`: MIT license.
* `CITATION.cff`: Citation metadata for this software repository.

## Data availability

The dataset used in this study is publicly available from Harvard Dataverse:

Voura E. Complete Stroke Data Repository V 3.0. Harvard Dataverse. 2026. doi: 10.7910/DVN/OYNYB4

Users should download the dataset from Harvard Dataverse and place it in the working directory before running the notebook.

## How to run

1. Clone or download this repository.
2. Install the required Python packages listed in `requirements.txt`.
3. Download the dataset from Harvard Dataverse.
4. Open and run the Jupyter notebook `Plos_One__Discharge_Disposition__code.ipynb`.

## Important note

The code and serialized model artifacts are provided for transparency and reproducibility of the research analysis. They are not intended for clinical deployment, bedside decision-making, or direct patient-care use.

## License

This repository is released under the MIT License.
