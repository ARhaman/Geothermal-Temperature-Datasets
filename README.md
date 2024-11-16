Geothermal Temperature Prediction in Western Yemen
This repository contains datasets and scripts related to geothermal temperature measurements in the western region of Yemen. The data includes surface and subsurface temperatures, as well as various geographical and geological parameters. The repository aims to provide comprehensive metadata and facilitate reproducibility and validation of the methodology used in our research.

Repository Structure
Datasets
dataset-1.arff: Geothermal temperature readings and associated geographical data.
dataset-2.arff: Additional geothermal temperature data with extended coverage and depth.
data-temperature-depth.xlsx: Summarized temperature data at various depths.
All-data-set-summary.xlsx: Summary of all datasets, including statistical analyses.
comparison-for-Set-1.xlsx: Comparison data for Set 1.
GP-result-no-outlier.xlsx: Gaussian Process analysis excluding outliers.
GP-result-outlier.xlsx: Gaussian Process analysis including outliers.
data-temperature-depth-missing.xlsx: Data with missing temperature values to test imputation methods.
Machine Learning Models and Results
Geothermal-temperature/`:

Enhanced optimized results for Set 1 and 2.
Enhanced cross-plots.
Gaussian Process results with and without outliers.
Random Forest predicted vs. measured results.
MLP-Set-2 optimized and non-optimized results.
Geothermal-temperature-gradient/:

Models such as Random Forest, MLP, and Gaussian Process for gradient predictions.
Optimized and non-optimized cross-plots for Set-2 models.
Outlier-Detection/:

Outlier detection models (e.g., LOF) and results.
Cross-plot results for testing and training with/without outliers.
Scripts
data_preprocessing_script.py: Python script for preprocessing and cleaning the data.
plot_generator.py: Generates cross-plots and visualizations for model outputs.
data_analysis_script.R: R script for performing statistical analysis on the datasets.
🚀 Usage Guide
Follow these steps to preprocess the data, train models, and visualize results:

1️⃣ Preprocess the Data
Clean datasets, handle missing values, and prepare your data for modeling:

bash
Copy code
python scripts/data_preprocessing_script.py \
  --input datasets/data-temperature-depth-missing.xlsx \
  --output datasets/processed-data.xlsx
Input: datasets/data-temperature-depth-missing.xlsx
Output: datasets/processed-data.xlsx
2️⃣ Train Machine Learning Models
Train the provided models using the datasets:

🔹 Gaussian Process (GP)
bash
Copy code
python models/gp_model_training.py \
  --dataset datasets/GP-result-no-outlier.xlsx \
  --output models/gp_results/
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
3️⃣ Generate Visualizations
Create cross-plots and other visualizations for results:

bash
Copy code
python scripts/plot_generator.py \
  --input results/mlp_results/predicted_vs_measured.xlsx \
  --output plots/mlp_crossplot.png
Input: Model predictions (predicted_vs_measured.xlsx).
Output: Plot saved in plots/mlp_crossplot.png.
4️⃣ Compare Model Performance
Use the provided Excel files for performance analysis:

📂 Set-1 Results: Enhanced comparison for Set-1 before Opt and after.xlsx
📂 Set-2 Results: Enhanced comparison for Set-2 before Opt and after.xlsx
System Requirements
Python: 3.8+
Dependencies:
bash
Copy code
pip install -r requirements.txt
Metadata
Each dataset includes relevant metadata, such as references, geothermal field information (e.g., lithology, location), well names, and sample names as originally reported by bibliographic sources.

References
For a detailed list of references related to Yemen’s geothermal energy potential, please see the references.txt file.

Contributing
We welcome contributions to improve the datasets and scripts. Please submit pull requests with clear descriptions of your changes.

License
This project is licensed under the MIT License.

Contact
For any questions or inquiries, please contact Abdulrahman Al-Fakih at alja2014ser@gmail.com.

Citation
If you use this repository or find our work helpful, please cite:

Al-Fakih, A., Al-khudafi, A., Koeshidayatullah, A., Kaka, S., & Al-Gathe, A. (2024). Forecasting geothermal temperature in western Yemen with Bayesian-optimized machine learning regression models.
College of Petroleum Engineering and Geosciences, King Fahd University of Petroleum & Minerals, Dhahran, Saudi Arabia.
Faculty of Engineering and IT, Emirates International University, Yemen.
Faculty of Engineering and Petroleum, Hadhramout University, Yemen.

