# Commute Research Project

This project is structured to organize data, code, and results for commute research analysis.

## Project Structure

- **.gitignore**: Configures which files not to upload to Git (e.g., data and results directories).

- **README.md**: This file, documenting the purpose of each folder and the execution order.

- **data/**: Ingredient warehouse (local only, never commit to Git!)
  - **01_raw/**: Raw data (e.g., original signaling data, never modify).
  - **02_intermediate/**: Intermediate data during cleaning.
  - **03_processed/**: Cleaned, standardized data ready for models.

- **results/**: Outputs (local only, use for papers).
  - **figures/**: High-resolution images (maps, charts).
  - **tables/**: Output CSV tables (pattern matrices, EC metrics).

- **src/**: Core engine (must commit to Git, keep code clean).
  - **__init__.py**: Empty file to make src a Python package.
  - **data_prep.py**: (Optional) Data cleaning functions.
  - **utils_format.py**: DataFrame and matrix conversions.
  - **models_pattern.py**: Three pattern models.
  - **metrics_eval.py**: Metric calculations.
  - **visualization.py**: Plotting functions.
  - **elasticity.py**: Elasticity parameter derivation.

- **notebooks/**: Workbench (exploratory code and main flow here).
  - **01_data_cleaning.ipynb**: Data cleaning and handling outliers.
  - **02_eda_and_stats.ipynb**: Exploratory data analysis and basic statistics.
  - **03_baseline_calibration.ipynb**: Beta parameter sweep and baseline model calibration.
  - **04_main_pipeline.ipynb**: Main control panel (integrate three patterns and scenario simulations).

## Execution Order

1. Start with `01_data_cleaning.ipynb` to clean and prepare data.
2. Use `02_eda_and_stats.ipynb` for exploratory analysis.
3. Run `03_baseline_calibration.ipynb` for model calibration.
4. Execute `04_main_pipeline.ipynb` for the main analysis pipeline.