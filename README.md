Geothermal Data of Western Yemen
Description
This repository contains datasets and scripts related to geothermal temperature measurements in the western region of Yemen. The data includes surface and subsurface temperatures, as well as various geographical and geological parameters. This repository aims to provide comprehensive metadata and facilitate reproducibility and validation of the methodology used in our research.

Repository Structure
datasets/

dataset-1.arff
dataset-2.arff
data-temperature-depth.xlsx
All-data-set-summary.xlsx
comparison-for-Set-1.xlsx
GP-result-no-outlier.xlsx
GP-result-outlier.xlsx
data-temperature-depth-missing.xlsx
data-temperature-depth-missing-1.xlsx
scripts/

data_analysis_script.R
data_preprocessing_script.py
Datasets
dataset-1.arff
Description: Contains geothermal temperature readings and associated geographical data.
Columns:
Temp.Gradient (°C/km)
Surface Temp. (°C)
Depth (m)
Elevation (m)
Latitude (degree)
Longitude (degree)
Subsurface Temperature (°C)
dataset-2.arff
Description: Additional geothermal temperature data with extended coverage and depth.
Columns: Same as dataset-1.
data-temperature-depth.xlsx
Description: Excel file summarizing temperature data at various depths.
All-data-set-summary.xlsx
Description: Summary of all datasets, including statistical analyses.
comparison-for-Set-1.xlsx
Description: Comparison data for Set 1.
GP-result-no-outlier.xlsx
Description: Results of Gaussian Process analysis excluding outliers.
GP-result-outlier.xlsx
Description: Results of Gaussian Process analysis including outliers.
data-temperature-depth-missing.xlsx
Description: Data with missing temperature values to test imputation methods.
data-temperature-depth-missing-1.xlsx
Description: Additional data with missing values for imputation testing.
Scripts
data_analysis_script.R
Description: R script for performing statistical analysis on the datasets.
Usage: Rscript data_analysis_script.R
data_preprocessing_script.py
Description: Python script for preprocessing and cleaning the data.
Usage: python data_preprocessing_script.py
Usage
To reproduce the analyses presented in our study, follow these steps:

Clone the repository:
bash
Copy code
git clone https://github.com/yourusername/Geothermal_Western_Yemen.git
Navigate to the repository directory:
bash
Copy code
cd Geothermal_Western_Yemen
Run the preprocessing script:
bash
Copy code
python scripts/data_preprocessing_script.py
Run the analysis script:
bash
Copy code
Rscript scripts/data_analysis_script.R
Metadata
Each dataset includes relevant metadata for each row, such as references, geothermal field information (e.g., lithology, location), well names, and sample names as originally reported by the bibliographic sources.

Contributing
We welcome contributions to improve the datasets and scripts. Please submit pull requests with clear descriptions of your changes.

License
This project is licensed under the MIT License.

Contact
For any questions or inquiries, please contact Abdulrahman Al-Fakih at alja2014ser@gmail.com.

