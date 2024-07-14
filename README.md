
# Geothermal Data of Western Yemen

## Description

This repository contains datasets and scripts related to geothermal temperature measurements in the western region of Yemen. The data includes surface and subsurface temperatures, as well as various geographical and geological parameters. This repository aims to provide comprehensive metadata and facilitate reproducibility and validation of the methodology used in our research.

## Repository Structure

### Datasets

The `datasets` directory includes:

- `dataset-1.arff`: Contains geothermal temperature readings and associated geographical data.
- `dataset-2.arff`: Additional geothermal temperature data with extended coverage and depth.
- `data-temperature-depth.xlsx`: Excel file summarizing temperature data at various depths.
- `All-data-set-summary.xlsx`: Summary of all datasets, including statistical analyses.
- `comparison-for-Set-1.xlsx`: Comparison data for Set 1.
- `GP-result-no-outlier.xlsx`: Results of Gaussian Process analysis excluding outliers.
- `GP-result-outlier.xlsx`: Results of Gaussian Process analysis including outliers.
- `data-temperature-depth-missing.xlsx`: Data with missing temperature values to test imputation methods.
- `data-temperature-depth-missing-1.xlsx`: Additional data with missing values for imputation testing.
- `data-temperature-depth,Statics.xlsx`: Statistical data related to temperature and depth measurements.

### Scripts

The `scripts` directory includes:

- `data_analysis_script.R`: R script for performing statistical analysis on the datasets.
- `data_preprocessing_script.py`: Python script for preprocessing and cleaning the data.
- Subfolders with machine learning models and results (e.g., `Geothermal-temperature`, `Geothermal-temperature-gradient`).

### Metadata

Each dataset includes relevant metadata for each row, such as references, geothermal field information (e.g., lithology, location), well names, and sample names as originally reported by the bibliographic sources.

## Usage

To reproduce the analyses presented in our study, follow these steps:

1. Clone the repository:
    ```bash
    git clone https://github.com/ARhaman/Geothermal-Western-Yemen.git
    cd Geothermal-Western-Yemen
    ```

2. Run the analysis script:
    ```bash
    python scripts/data_preprocessing_script.py
    Rscript scripts/data_analysis_script.R
    ```

3. Use the provided models for temperature prediction and analysis.

## Contributing

We welcome contributions to improve the datasets and scripts. Please submit pull requests with clear descriptions of your changes.

## License

This project is licensed under the MIT License.

## Contact

For any questions or inquiries, please contact Abdulrahman Al-Fakih at alja2014ser@gmail.com.
