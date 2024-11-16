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


To format your code blocks in a GitHub README to appear as they do in the example, follow these steps:

Markdown Syntax for GitHub Code Preview
Use Triple Backticks (```):

Wrap your code with triple backticks (```) to create a code block.
Specify the language for syntax highlighting (e.g., python, bash, etc.).
Add Comments and Indentation:

Include comments (# or //) and organize the code with proper indentation to enhance readability.
Example for Your README.md
Here’s how you can structure it for GitHub:

markdown
Copy code
## 🚀 Usage Guide

Follow these simple steps to preprocess the data, train models, and visualize results:

---

### 1️⃣ Preprocess the Data
Clean datasets, handle missing values, and prepare your data for modeling:
```bash
python scripts/data_preprocessing_script.py \
  --input datasets/data-temperature-depth-missing.xlsx \
  --output datasets/processed-data.xlsx

Input: datasets/data-temperature-depth-missing.xlsx
Output: datasets/processed-data.xlsx
---
### 2️⃣ Train Machine Learning Models
Use the provided datasets to train models and generate predictions:

🔹 Gaussian Process (GP)
---
bash
Copy code
python models/gp_model_training.py \
  --dataset datasets/GP-result-no-outlier.xlsx \
  --output models/gp_results/
---
🔹 Multi-Layer Perceptron (MLP)
bash
Copy code
python models/mlp_training.py \
  --train datasets/dataset-1.arff \
  --test datasets/dataset-2.arff \
  --output results/mlp_results/

🔹 Random Forest (RF)
bash
Copy code
python models/rf_training.py \
  --train datasets/dataset-1.arff \
  --test datasets/dataset-2.arff \
  --output results/rf_results/

### 3️⃣ Generate Visualizations
Create cross-plots and other visualizations for your results:

bash
Copy code
python scripts/plot_generator.py \
  --input results/mlp_results/predicted_vs_measured.xlsx \
  --output plots/mlp_crossplot.png

Input: Model predictions (e.g., predicted_vs_measured.xlsx)
Output: Plot saved in plots/mlp_crossplot.png

System Requirements
Python: 3.8+
Install dependencies:

bash
Copy code
pip install -r requirements.txt
yaml
Copy code


### Tips for Enhancing Code Blocks in GitHub:

1. **Add Syntax Highlighting**:
   - Use the language name after the opening backticks, e.g., ` ```python ` for Python code, ` ```bash ` for terminal commands.

2. **Ensure Proper Indentation**:
   - Indent code appropriately to make it visually pleasing.

3. **Use Comments**:
   - Add inline comments in your code to explain each step (e.g., `# Input data file`).

4. **Avoid Long Lines**:
   - Break long lines using backslashes (`\`) for better readability.
-------------------------------------------------
### References
For a detailed list of references related to Yemen’s geothermal energy potential, please see the references.txt file.


### Contributing

We welcome contributions to improve the datasets and scripts. Please submit pull requests with clear descriptions of your changes.

### License

This project is licensed under the MIT License.

### Contact

For any questions or inquiries, please contact Abdulrahman Al-Fakih at alja2014ser@gmail.com.

### Citing This Work

If you use this repository or find our work helpful, please cite:

Al-Fakih, A., Al-khudafi, A., Koeshidayatullah, A., Kaka, S., & Al-Gathe, A. (2024). Forecasting geothermal temperature in western Yemen with Bayesian-optimized machine learning regression models. *College of Petroleum Engineering and Geosciences, King Fahd University of Petroleum & Minerals, King Fahd Road, Dhahran, 31261, Eastern Province, Saudi Arabia*; *Faculty of Engineering and IT, Oil, and Gas Engineering Department, Emirates International University, Hadda Street, Sanaa, Yemen*; *Faculty of Engineering and Petroleum, Department of Petroleum Engineering, Hadhramout University, Al-Mukalla, Yemen*.

