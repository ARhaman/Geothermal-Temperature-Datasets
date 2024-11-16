# 🌍 Geothermal Temperature Prediction in Western Yemen

This repository contains datasets and scripts for geothermal temperature analysis in the western region of Yemen. The data includes surface and subsurface temperatures alongside various geographical and geological parameters. Our goal is to provide metadata and tools for reproducibility and validation of the methodologies used.

---

## 📂 Repository Structure

### **Datasets**
- `dataset-1.arff`: Geothermal temperature readings with geographical data.
- `dataset-2.arff`: Extended geothermal temperature data with greater depth.
- `data-temperature-depth.xlsx`: Summarized temperature data by depth.
- `GP-result-no-outlier.xlsx`: Gaussian Process results excluding outliers.
- `GP-result-outlier.xlsx`: Gaussian Process results including outliers.
- `data-temperature-depth-missing.xlsx`: Data with missing values for imputation tests.

### **Models and Results**
- **Geothermal-temperature/**:
  - Enhanced optimized results for Set-1 and Set-2.
  - Random Forest predicted vs. measured results.
  - Gaussian Process results with and without outliers.
- **Geothermal-temperature-gradient/**:
  - Gradient models (e.g., Random Forest, MLP, Gaussian Process) with and without optimization.
- **Outlier Detection**:
  - Outlier detection models (e.g., LOF) and cross-plot comparisons.

---

---

## 🚀 Usage Guide

Follow these simple steps to preprocess the data, train models, and visualize results.

---

### **1️⃣ Preprocess the Data**
Clean datasets, handle missing values, and prepare your data:
```bash
python scripts/data_preprocessing_script.py \
  --input datasets/data-temperature-depth-missing.xlsx \
  --output datasets/processed-data.xlsx

Input: Raw data file with missing values.
Output: Cleaned data saved in datasets/processed-data.xlsx.

2️⃣ Train Machine Learning Models
Train models using the provided datasets.

🔹 Gaussian Process (GP)
python models/gp_model_training.py \
  --dataset datasets/GP-result-no-outlier.xlsx \
  --output models/gp_results/

🔹 Multi-Layer Perceptron (MLP)
python models/mlp_training.py \
  --train datasets/dataset-1.arff \
  --test datasets/dataset-2.arff \
  --output results/mlp_results/

🔹 Random Forest (RF)
python models/rf_training.py \
  --train datasets/dataset-1.arff \
  --test datasets/dataset-2.arff \
  --output results/rf_results/

3️⃣ Generate Visualizations
Create cross-plots and visualizations for the results:
python scripts/plot_generator.py \
  --input results/mlp_results/predicted_vs_measured.xlsx \
  --output plots/mlp_crossplot.png
Input: Model predictions (predicted_vs_measured.xlsx).
Output: Plot saved in plots/mlp_crossplot.png.

4️⃣ Compare Model Performance
Use the provided files to compare performance:

📂 Set-1 Results: Enhanced comparison for Set-1 before Opt and after.xlsx
📂 Set-2 Results: Enhanced comparison for Set-2 before Opt and after.xlsx
These files highlight the differences before and after Bayesian optimization.
🛠 System Requirements
Python: 3.8+
Install Dependencies:
pip install -r requirements.txt

---
### Metadata
Each dataset includes metadata for rows, such as:
• Geothermal field data (e.g., lithology, location).
• Well names and sample references from original sources.

---
🤝 Contributing
We welcome contributions to improve this repository! Please submit pull requests with clear descriptions of your changes.

📜 License
This project is licensed under the MIT License.

✉️ Contact
For inquiries, contact Abdulrahman Al-Fakih: alja2014ser@gmail.com

---
## 📖 Citation
If you find this repository helpful, please cite:

**Al-Fakih, A., et al.** (2024). Forecasting geothermal temperature in western Yemen using Bayesian-optimized machine learning.

*King Fahd University of Petroleum & Minerals, Dhahran, Saudi Arabia*  
*Emirates International University, Sanaa, Yemen*  
*Hadhramout University, Mukalla, Yemen*
---


