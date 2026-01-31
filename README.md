# Insurance Premium Prediction Project

This project focuses on analyzing and preprocessing a medical insurance dataset to understand the factors affecting insurance premiums (`charges`). The notebook performs comprehensive Exploratory Data Analysis (EDA), Feature Engineering, and Feature Selection to prepare the data for Machine Learning modeling.

## 📂 Project Structure

- `ML_project.ipynb`: The main Jupyter Notebook containing the data analysis, visualization, and preprocessing steps.
- `insurance.csv`: The dataset used for the project.

## 📊 Dataset Overview

The dataset contains the following features:
- **age**: Age of the primary beneficiary.
- **sex**: Insurance contractor gender (female, male).
- **bmi**: Body mass index (ideal 18.5 to 24.9).
- **children**: Number of children covered by health insurance / Number of dependents.
- **smoker**: Smoking status (yes, no).
- **region**: The beneficiary's residential area in the US (northeast, southeast, southwest, northwest).
- **charges**: Individual medical costs billed by health insurance.

## 🛠️ Technologies Used

- **Python**
- **Pandas**: For data manipulation and analysis.
- **NumPy**: For numerical operations.
- **Matplotlib & Seaborn**: For data visualization (Histograms, Heatmaps).
- **Scipy**: For statistical testing (Pearson correlation, Chi-Square test).
- **Scikit-learn**: For data preprocessing (StandardScaler).

## 🔍 Key Steps in Analysis

1.  **Data Loading & Cleaning**:
    -   loaded the `insurance.csv` dataset.
    -   Checked for missing values and data types.

2.  **Exploratory Data Analysis (EDA)**:
    -   Visualized distributions of numerical features (`age`, `bmi`, `children`, `charges`).
    -   Analyzed categorical relationships.

3.  **Feature Engineering**:
    -   **Encoding**: Converted categorical variables (`sex`, `smoker`) to numerical format. One-hot encoding applied to `region`.
    -   **Binning**: Created a `bmi_category` feature (Underweight, Normal, Overweight, Obese) to better capture non-linear relationships.

4.  **Feature Selection**:
    -   **Correlation Analysis**: Used Pearson correlation to identify features strongly correlated with `charges`.
    -   **Statistical Testing**: Performed Chi-Square tests to determine the significance of categorical features.
    -   **Selected Features**: Based on the analysis, the most relevant features selected for the model are: `age`, `is_smoker`, `children`, `region_southeast`, `is_female`, and `bmi`.

5.  **Data Preprocessing**:
    -   **Scaling**: Applied `StandardScaler` to numerical features (`age`, `children`, `bmi`) to standardize the data distribution.

## 📈 Key Insights

- **Smoking status** (`is_smoker`) has the highest correlation with insurance charges, indicating it's a primary driver of costs.
- **BMI** and **Age** also show significant positive correlations with charges.
- Statistical tests helped in refining the feature set by identifying less relevant features (e.g., certain regions were dropped based on p-values).

## 🚀 How to Run

1.  Ensure you have Python installed along with the required libraries:
    ```bash
    pip install pandas numpy matplotlib seaborn scipy scikit-learn
    ```
2.  Open the notebook:
    ```bash
    jupyter notebook ML_project.ipynb
    ```
3.  Run the cells sequentially to reproduce the analysis.
