# Budget, Cost, or Both? An Empirical Exploration of Mechanisms in Quadratic Surveys Data Analysis

This repository contains notebooks and data used for the paper ``Budget, Cost, or Both? An Empirical Exploration of Mechanisms in Quadratic Surveys'' published in Collective Intelligence 2025. The main notebooks in the repository load models created elsewhere and generate the figures found in `output/` and `plots/`.

## Repository Structure

- `QV_intensity_analysis.ipynb` – Post modeling analysis notebook for intensity conditions.
- `QV_sign_analysis.ipynb` – Post modeling analysis notebook for sign conditions.
- `modeling_notebook/` – Public versions of the notebooks used to fit the models.
- `data/` – Experiment data files used by the notebooks.
- `output/` and `plots/` – Generated CSVs and PDF figures.

## Reproducing the Results

The analysis notebooks expect pre‑computed model traces. These traces are large and are not stored in this repository. To generate them:

1. Clone and run the separate modeling repository that accompanies this analysis.
2. Execute the notebooks inside that repository to fit the models using the data found here under `data/`.
3. Note the location where the model files (`.trace` NetCDF files) are saved and update the corresponding paths in the analysis notebooks.

After the models are created, edit the `MODEL_PATH` variable near the top of each root notebook so it points to the folder containing the saved models. You may also adjust `DATA_PATH`, `OUTPUT_PATH`, and `PLOT_PATH` if your directory layout differs.

Once the paths are configured, run the notebooks in this repository to reproduce the plots and CSV outputs.

## Dependencies

The notebooks were developed with Python and require packages such as `numpyro`, `arviz`, `pandas`, and `seaborn`. The modeling notebooks include cells that install these packages via `pip`. It is recommended to use a virtual environment or conda environment to manage dependencies prior to running the notebooks.

## Cite
Please cite the paper should the data or models be useful for your work:

```
@inproceedings{cheng2025budget,
  author    = {Ti-Chung Cheng, Tiffany Wenting Li, Karrie Karahalios, and Hari Sundaram},
  title     = {Budget, Cost, or Both? An Empirical Exploration of Mechanisms in Quadratic Surveys},
  booktitle = {Proceedings of the Collective Intelligence Conference (CI 2025)},
  year      = {2025},
  month     = {August},
  pages     = {1--13},
  address   = {San Diego, CA, USA},
  publisher = {ACM},
  doi       = {10.1145/3715928.3737474},
  isbn      = {979-8-4007-1489-4/2025/08},
  url       = {https://doi.org/10.1145/3715928.3737474}
}
```

