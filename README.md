🏥 Health Insurance Cost Predictor

This project analyzes a medical insurance dataset to understand the factors influencing insurance premiums (charges). It includes Exploratory Data Analysis (EDA), Feature Engineering, Feature Selection, and prepares the dataset for Machine Learning modeling.

📂 Project Structure

ML_project.ipynb – Main Jupyter Notebook containing analysis, visualizations, and preprocessing steps.

insurance.csv – Dataset used for analysis and modeling.

📊 Dataset Overview

The dataset contains the following features:

Feature	Description
age	Age of the primary beneficiary
sex	Insurance contractor gender (female, male)
bmi	Body Mass Index (ideal 18.5–24.9)
children	Number of children/dependents covered by insurance
smoker	Smoking status (yes, no)
region	Residential area in the US (northeast, southeast, southwest, northwest)
charges	Individual medical costs billed by health insurance
🛠️ Technologies Used

Python – Core programming language

Pandas & NumPy – Data manipulation and numerical operations

Matplotlib & Seaborn – Data visualization (histograms, heatmaps, plots)

SciPy – Statistical testing (Pearson correlation, Chi-Square test)

Scikit-learn – Preprocessing (StandardScaler) and ML preparation

🔍 Key Steps in the Analysis

Data Loading & Cleaning

Loaded insurance.csv.

Checked for missing values and data types.

Exploratory Data Analysis (EDA)

Visualized numerical features (age, bmi, children, charges).

Analyzed categorical features and their relationships with charges.

Feature Engineering

Encoding: Converted sex and smoker to numerical; one-hot encoded region.

Binning: Created bmi_category (Underweight, Normal, Overweight, Obese) to capture non-linear relationships.

Feature Selection

Correlation Analysis: Identified numerical features strongly correlated with charges.

Statistical Testing: Chi-Square tests for categorical feature significance.

Selected Features: age, is_smoker, children, region_southeast, is_female, and bmi.

Data Preprocessing

Scaling: Standardized numerical features (age, children, bmi) using StandardScaler.

📈 Key Insights

Smoking status (is_smoker) is the strongest driver of insurance costs.

BMI and age positively correlate with charges, meaning higher BMI and older age lead to higher premiums.

Statistical tests helped refine features, dropping less impactful ones like certain regions.

🚀 How to Run

Install Python and required libraries:

pip install pandas numpy matplotlib seaborn scipy scikit-learn


Open the Jupyter Notebook:

jupyter notebook ML_project.ipynb


Run the notebook cells sequentially to reproduce the analysis.
