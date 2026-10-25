This project was designed to develop and evaluate a machine learning framework for predicting movie box office revenue using historical metadata. The project was executed using TMDb and GroupLens dataset records processed within a structured data science pipeline.

The submission consists of the core notebook, data directories, exported evaluation artifacts, and documentation:

"box_office_prediction.ipynb" - a Jupyter Notebook that executes data cleaning, categorical target encoding, model training, cross-validation, and SHAP feature attribution.

"data/" - a directory containing raw datasets (movies_metadata.csv and credits.csv).

"tables/" - a directory containing exported CSV and LaTeX summary tables documenting data flow, cross-validation performance, and model comparison metrics.

"figures/" - a directory containing generated PDF and PNG figures illustrating target distributions, error analyses, and model performance.

"README.md" - a file with textual explanation of code execution and project structure.

To run the project:
1. Install Python version 3.12
2. Install the required Python packages
3. Open the project directory in your preferred environment (e.g., Jupyter Lab, VS Code, or Google Colab).

Place movies_metadata.csv and credits.csv inside the data/ folder.

Open and execute box_office_prediction.ipynb sequentially to run the end-to-end data preprocessing, training, evaluation, and artifact generation pipeline.
