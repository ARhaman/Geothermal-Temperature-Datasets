# Geothermal Temperature Prediction in Western Yemen

This repository contains datasets and scripts related to geothermal temperature measurements in the western region of Yemen. The data includes surface and subsurface temperatures, as well as various geographical and geological parameters. This repository aims to provide comprehensive metadata and facilitate reproducibility and validation of the methodology used in our research.

## Repository Structure

### Datasets

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

### Machine Learning Models and Results

- `Geothermal-temperature/`: Contains models and results related to geothermal temperature predictions.
    - `Gaussian-Set-1`
    - `Gaussian-Set-1-CV-crossPlot`
    - `Gaussian-Set-1-CV-crossPlot-optimized`
    - `linearRegression-set-1`
    - `M5P-set-1`
    - `M5P-set-1-Testing-CrossPlot`
    - `MLP-set-1`
    - `RBFRegressor-set-1`
    - `REPT-set-1`
    - `REPT-set-1-After-outlier`
    - `REPT-set-1-After-outlier+randomize`
    - `REPT-set-1-After-outlier+randomize+SMOTE-Training`
    - `REPT-set-1-After-outlier+randomize+SMOTE-Training+Testing`
    - `RF-set-1`
    - `RT-set-2`
    - `simpleLinearRegression-set-1`
    - `simpleLinearRegression-set-1-CV-Cross-No-optim`
    - `SMOreg-set-1`
    - `SMOreg-set-1-CV-Cross-No-optim`
- `Geothermal-temperature-gradient/`: Contains models and results related to geothermal temperature gradient predictions.
    - `Gaussian-Set-2`
    - `Gaussian-Set-2-CrossP-CV-with-optimization`
    - `Gaussian-Set-2-CrossP-CV-without-optim`
    - `linearRegression-set-2`
    - `M5P-set-2`
    - `MLP-set-2`
    - `MLP-set-2-CV-CrossPlot-optimized`
    - `MLP-set-2-CV-CrossPlot-without-optim`
    - `RandomCommittee-Testing-cross-V`
    - `RBFRegressor-set-2`
    - `RBFRegressor-set-2-CV-CrossP-optimized`
    - `RBFRegressor-set-2-CV-CrossP-without-optim`
    - `REPTree-set-2`
    - `RF-set-2`
    - `RT-set-1`
    - `simpleLinearRegression-set-2`
    - `SMOreg-set-2`
- `Outlier-Detection/`: Contains outlier detection models and results.
    - `LOF-summary-result.xlsx`
    - `set-1-LOF`
    - `set-1-model-LOF-training.model`
    - `set-1-model-LOF-training+testing.model`
    - `set-1-Crossplot-testing-No-outlier.xlsx`
    - `set-1-Crossplot-training+testing.xlsx`
    - `set-1.model`
    - `set-1-cross-plot-training.xlsx`
    - `set-1-cross-plot-training-No-outlier.xlsx`
    - `set-1-testing-resuts-1.xlsx`
    - `set-1-training+testing-LOF-resuts.xlsx`
    - `set-2.model`
    - `set-2-testing-resuts-Cross-No-outlier.xlsx`
    - `set-2-training-resuts-Cross.xlsx`
    - `set-2-training-resuts-Cross-No-outlier.xlsx`
    - `Summary-IQR.xlsx`

### Scripts

- `data_analysis_script.R`: R script for performing statistical analysis on the datasets.
- `data_preprocessing_script.py`: Python script for preprocessing and cleaning the data.

## Metadata

Each dataset includes relevant metadata for each row, such as references, geothermal field information (e.g., lithology, location), well names, and sample names as originally reported by the bibliographic sources.

## References

For a detailed list of references related to Yemen’s geothermal energy potential, please see the [references.txt](./references.txt) file.

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

3. **Unzip the ML models and results:**
    ```bash
    unzip datasets/ML-models-and-results.zip -d scripts/
    ```

4. Use the provided models for temperature prediction and analysis.

## Contributing

We welcome contributions to improve the datasets and scripts. Please submit pull requests with clear descriptions of your changes.

## License

This project is licensed under the MIT License.

## Contact

For any questions or inquiries, please contact Abdulrahman Al-Fakih at alja2014ser@gmail.com.
