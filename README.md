# CI 2025 Analysis

This repository contains notebooks and data used for the final analysis and plotting for the CI 2025 study. The main notebooks in the repository load models created elsewhere and generate the figures found in `output/` and `plots/`.

## Repository Structure

- `QV_intensity_analysis.ipynb` – Analysis notebook for intensity conditions.
- `QV_sign_analysis.ipynb` – Analysis notebook for sign conditions.
- `modeling_notebook/` – Public versions of the notebooks used to fit the models.
- `data/` – Experiment data files used by the notebooks.
- `output/` and `plots/` – Generated CSVs and PDF figures.

## Reproducing the Results

The analysis notebooks expect pre‑computed model traces. These traces are large and are not stored in this repository. To generate them:

1. Clone and run the separate modeling repository that accompanies this analysis.
2. Execute the notebooks inside that repository to fit the models using the data found here under `data/`.
3. Note the location where the model files (`.trace` NetCDF files) are saved.

After the models are created, edit the `MODEL_PATH` variable near the top of each root notebook so it points to the folder containing the saved models. You may also adjust `DATA_PATH`, `OUTPUT_PATH`, and `PLOT_PATH` if your directory layout differs.

Once the paths are configured, run the notebooks in this repository to reproduce the plots and CSV outputs.

## Dependencies

The notebooks were developed with Python and require packages such as `numpyro`, `arviz`, `pandas`, and `seaborn`. The modeling notebooks include cells that install these packages via `pip`.

