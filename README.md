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

RMnT/RESULTS/
│
├── box_office_prediction.ipynb        # Main execution notebook
│
├── data/                              # Raw dataset directory
│   ├── credits.csv                    # Cast and crew metadata
│   └── movies_metadata.csv            # TMDb movie metadata
│
├── figures/                           # Generated plots and charts (PDF & PNG)
│   ├── fig1_distributions.pdf         # Target and feature distribution plots
│   ├── fig2_main_results.pdf          # Comparative model performance
│   ├── fig4_pdp_budget.pdf            # Partial dependence plot for budget
│   ├── fig_error_vs_budget.pdf        # Error vs. budget analysis plot
│   ├── fig_smoothing_sensitivity.pdf  # Target encoding smoothing sensitivity
│   ├── model_performance.pdf / .png   # Overall model performance charts
│   ├── model_performance_label_encoded.pdf / .png # Label-encoded model performance
│   ├── residual_plot.pdf              # Regression residual analysis
│   └── shap_summary.pdf               # SHAP feature importance summary
│
├── tables/                            # Exported results and tables (CSV & LaTeX .tex)
│   ├── per_seed_test_metrics.csv      # Multi-seed robustness tracking
│   ├── table_cv_selection.csv / .tex  # Cross-validation performance grid
│   ├── table_error_by_budget.csv / .tex # Budget-tiered error breakdown
│   ├── table_error_summary.csv / .tex # Comprehensive error metrics summary
│   ├── table_shap_stability.csv / .tex # SHAP feature stability analysis
│   ├── table_smoothing_sensitivity.csv / .tex # Target encoding smoothing metrics
│   ├── table_target_transform.csv / .tex # Target distribution transformation metrics
│   ├── table1_data_flow.csv / .tex    # Data filtering and cleaning audit trail
│   ├── table2_dataset.csv / .tex      # Dataset summary properties
│   ├── table2b_target_distribution.csv / .tex # Train vs. test target statistics
│   ├── table3_main_results.csv / .tex # Out-of-sample evaluation matrix
│   ├── table4_h1_encoding_tests.csv / .tex # Categorical encoding test results
│   ├── table5_h2_model_tests.csv / .tex # Model architecture comparison results
│   ├── table5b_success_criteria.csv / .tex # Success criteria validation
│   ├── table6_feature_ablation.csv / .tex # Feature ablation test results
│   ├── table7_group_results.csv / .tex # Group-wise performance metrics
│   ├── table8_worst_cases.csv / .tex  # Worst-performing prediction cases
│   └── table9_shap_top15.csv / .tex   # Top 15 SHAP feature attributions
│
└── catboost_info/                     # CatBoost training logs and telemetry
    ├── learn/
    │   └── events.out.tfevents        # TensorBoard training event logs
    ├── tmp/                           # Temporary training files
    ├── catboost_training.json         # Training configuration/metadata
    ├── learn_error.tsv                # Training error tracking
    └── time_left.tsv                  # Training progress time log