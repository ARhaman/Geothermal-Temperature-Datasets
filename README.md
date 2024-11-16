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

Geothermal-temperature/: Contains models and results related to geothermal temperature predictions.
Enhanced optimized of set1 and 2
Enhanced cross plot
Enhanced and updated GP-result-without outlier
Enhanced and updated GP-result-with outlier
Enhanced comparison for Set-1 before Opt and after
Enhanced comparison for Set-2 before Opt and after
Enhanced Gaussian Set-1 TS Before Opt + After
Enhanced Gaussian Set-1 TS crossPlot with and without outlier
Enhanced Gaussian Set-2 Testing without outlier
Enhanced MLP-Set-2 &1-TS Optimized & Not optimized
Enhanced RF-Predicted vs measure
Enhanced set-1 GP-training&testing-Optimized
Enhanced SMOreg set-1 TS-N Before & After opt
Enhanced Summary-IQR
Enhanced Summary-No-opt set1+set2
Geothermal-temperature
Geothermal-temperature-gradient
GP_model_performance_with_final_calibration
MLP-set-2-CV After & After opt
RandomCommittee-training-cross
S-1-with-outlier
S-2-with-outlier
Set-1-LOF
Set-1-model-LOF-training.model
Set-1-model-LOF-training+testing.model
Set-1-Crossplot-testing-No-outlier.xlsx
Set-1-Crossplot-training+testing.xlsx
Set-1.model
Set-1-cross-plot-training.xlsx
Set-1-cross-plot-training-No-outlier.xlsx
Set-1-testing-results-1.xlsx
Set-1-training+testing-LOF-results.xlsx
Set-2.model
Set-2-testing-results-Cross-No-outlier.xlsx
Set-2-training-results-Cross.xlsx
Set-2-training-results-Cross-No-outlier.xlsx
Summary-IQR.xlsx
results-TR-CV-Test.xlsx

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

1. Datasets Overview
Explain the purpose and format of the datasets:

dataset-1.arff and dataset-2.arff: Main datasets for geothermal temperature analysis.
data-temperature-depth.xlsx: Contains summarized temperature data at various depths.
GP-result-no outlier.xlsx and GP-result-outlier.xlsx: Used for Gaussian Process modeling with and without outliers.
Enhanced comparison for Set-1 before Opt and after.xlsx: Highlights results for Set-1 before and after Bayesian optimization.
2. Preprocessing Data
Provide detailed steps for preprocessing:

Preprocessing Missing Data:

Use the file data-temperature-depth-missing.xlsx for testing imputation methods.
Run the preprocessing script:
bash
Copy code
python scripts/data_preprocessing_script.py --input datasets/data-temperature-depth-missing.xlsx --output datasets/processed-data.xlsx
Input: Missing data file.
Output: Cleaned and imputed data file saved in datasets/.
Handling Outliers:

Use set-1-Crossplot-testing-No-outlier.xlsx and set-1-Crossplot-training+testing.xlsx for training and testing with and without outliers.
Example:
bash
Copy code
python scripts/outlier_detection.py --input datasets/GP-result-no-outlier.xlsx --output results/no_outliers_processed.xlsx
3. Running Machine Learning Models
Explain how to train and test models:

Gaussian Process Model:

Training:
bash
Copy code
python models/gp_model_training.py --dataset datasets/GP-result-no-outlier.xlsx --output models/gp_results/
Testing:
bash
Copy code
python models/gp_model_testing.py --model models/gp_results/model.pkl --test datasets/dataset-2.arff
Outputs:
Trained model saved in models/.
Predictions saved in results/.
MLP Model:

Training:
bash
Copy code
python models/mlp_training.py --train datasets/dataset-1.arff --test datasets/dataset-2.arff --output results/mlp_results/
Example Output:
Enhanced MLP-Set-2 &1-TS Optimize.xlsx: Contains optimized results.
MLP-set-2-CV-CrossPlot-optimized.xlsx: Cross-plots for optimized MLP model.
Random Forest Model:

Training:
bash
Copy code
python models/rf_training.py --train datasets/dataset-1.arff --test datasets/dataset-2.arff --output results/rf_results/
Example Output:
Enhanced RF-Predicted vs measure.xlsx: Predicted vs. measured results for RF.
4. Comparing Results
Explain how to use comparison files:

Set-1 Results:
Use Enhanced comparison for Set-1 before Opt and after.xlsx for comparing model performance before and after optimization.
Set-2 Results:
Use Enhanced comparison for Set-2 before Opt and after.xlsx for similar comparisons on Set-2.
5. Visualization
Provide instructions for generating cross-plots and visualizations:

Cross-Plots:
For Set-1, use:
bash
Copy code
python scripts/plot_generator.py --input results/Enhanced-set-1-cross-plot-training.xlsx --output plots/set1_crossplot.png
For Set-2, use:
bash
Copy code
python scripts/plot_generator.py --input results/Enhanced-set-2-cross-plot-testing-No-outlier.xlsx --output plots/set2_crossplot.png
6. System Requirements
Languages: Python 3.8+, R (optional).
Dependencies: Use requirements.txt:
bash
Copy code
pip install -r requirements.txt
7. Reproducing the Study
Clone the repository:
bash
Copy code
git clone https://github.com/ARhaman/Geothermal-Western-Yemen.git
cd Geothermal-Western-Yemen
Preprocess the data:
bash
Copy code
python scripts/data_preprocessing_script.py --input datasets/data-temperature-depth.xlsx --output datasets/processed.xlsx
Train models:
Example for MLP:
bash
Copy code
python models/mlp_training.py --train datasets/dataset-1.arff --test datasets/dataset-2.arff --output results/mlp_results/
Visualize results:
bash
Copy code
python scripts/plot_generator.py --input results/mlp_results/predicted_vs_measured.xlsx --output pl

## Contributing

We welcome contributions to improve the datasets and scripts. Please submit pull requests with clear descriptions of your changes.

## License

This project is licensed under the MIT License.

## Contact

For any questions or inquiries, please contact Abdulrahman Al-Fakih at alja2014ser@gmail.com.

### Citing This Work

If you use this repository or find our work helpful, please cite:

Al-Fakih, A., Al-khudafi, A., Koeshidayatullah, A., Kaka, S., & Al-Gathe, A. (2024). Forecasting geothermal temperature in western Yemen with Bayesian-optimized machine learning regression models. *College of Petroleum Engineering and Geosciences, King Fahd University of Petroleum & Minerals, King Fahd Road, Dhahran, 31261, Eastern Province, Saudi Arabia*; *Faculty of Engineering and IT, Oil, and Gas Engineering Department, Emirates International University, Hadda Street, Sanaa, Yemen*; *Faculty of Engineering and Petroleum, Department of Petroleum Engineering, Hadhramout University, Al-Mukalla, Yemen*.

