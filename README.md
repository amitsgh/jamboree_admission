# Jamboree Admission Analysis

## Overview
This project explores and predicts the probability of admissions based on academic and personal factors such as GRE scores, TOEFL scores, CGPA, and research experience. Using data analysis, visualization, and machine learning techniques, this analysis identifies key features and builds predictive models to estimate admission chances.

The primary goal is to assist students in understanding what factors influence admission rates, thereby guiding them in making informed decisions during their application process.

## Table of Contents
- [Overview](#overview)
- [Data](#data)
- [Methodology](#methodology)
  - [1. Data Exploration](#1-data-exploration)
  - [2. Data Visualization](#2-data-visualization)
  - [3. Statistical Analysis](#3-statistical-analysis)
  - [4. Data Preprocessing](#4-data-preprocessing)
  - [5. Model Development](#5-model-development)
- [Results](#results)

## Data
The dataset used in this analysis includes information about students' academic performance, personal ratings, and other factors influencing admissions. The dataset has the following features:

- **GRE Score**: Scores range from 0 to 340.
- **TOEFL Score**: Scores range from 0 to 120.
- **University Rating**: Ratings range from 1 to 5, with 5 being the highest.
- **SOP (Statement of Purpose)**: A rating for the quality of the applicant's statement of purpose (1-5).
- **LOR (Letter of Recommendation)**: A rating for the strength of the applicant's letter of recommendation (1-5).
- **CGPA**: Undergraduate Cumulative GPA on a 10-point scale.
- **Research**: Binary indicator (0 or 1) of whether the applicant has research experience.

The dataset is stored as a CSV file named `Jamboree.csv` in the `/data` directory.

## Methodology
The project follows a systematic data science pipeline to ensure a thorough analysis:

### 1. Data Exploration
- **Objective**: Understand the data structure, detect missing values, outliers, and assess the distribution of features.
- **Steps**:
  - Loaded the dataset using Pandas.
  - Checked for missing values and identified the data types of each feature.
  - Examined the shape and summary statistics of the dataset.

### 2. Data Visualization
- **Objective**: Visualize patterns, distributions, and relationships between features.
- **Steps**:
  - Created histograms and scatter plots to observe distributions and potential relationships.
  - Generated a correlation heatmap to understand relationships between variables, highlighting strong correlations (e.g., GRE scores and CGPA).
- **Key Visuals**:
    ![Histogram](images/histogram.png)
  - **Histogram**: Displayed the distribution of scores and ratings.
  
  ![Correlation Heatmap](images/correlation_heatmap.png)
  - **Correlation Heatmap**: Showed strong positive correlations between GRE scores, CGPA, and admission probability.

### 3. Statistical Analysis
- **Objective**: Identify statistically significant relationships between features.
- **Steps**:
  - Conducted correlation tests and computed correlation coefficients to determine the strength and nature of relationships.
  - Applied the ANOVA test to evaluate the differences in admission chances based on university ratings.
  - Performed a chi-square test to assess the association between research experience and university ratings.

- **Tests Conducted**:

  1. **ANOVA Test for University Rating**
     - **Description**: One-Way ANOVA was used to evaluate if there are significant differences in the mean admission chances across different university ratings.
     - **Result**: The F-statistic value was 114.01 with a p-value of 7.75e-69.
     - **Interpretation**: The extremely small p-value indicates that there is a statistically significant difference in admission chances based on university ratings.

  2. **Correlation Test for Continuous Variables**
     - **Description**: Pearson Correlation Coefficient was used to evaluate the strength and direction of the linear relationship between continuous variables (GRE score, CGPA) and the chance of admission.
     - **Results**:
       - GRE score: Correlation value = 0.81, p-value = 1.09e-117
       - CGPA: Correlation value = 0.88, p-value = 3.40e-165
     - **Interpretation**: Both GRE score and CGPA have a strong positive correlation with the chance of admission, with p-values indicating that these relationships are statistically significant.

  3. **Chi-Square Test for Research and University Rating**
     - **Description**: A Chi-Square Test of Independence was conducted to evaluate whether research experience and university rating are associated.
     - **Result**: The Chi-Square statistic was 96.90 with a p-value of 4.49e-20.
     - **Interpretation**: The small p-value indicates that there is a statistically significant association between research experience and university ratings.

- **Findings**:
  - There is a significant variation in admission chances across different university ratings (ANOVA test).
  - Both GRE scores and CGPA have strong positive correlations with admission chances (Pearson correlation).
  - There is a statistically significant association between having research experience and the university rating (Chi-Square test).

### 4. Data Preprocessing
- **Objective**: Prepare the data for modeling by cleaning and transforming it.
- **Steps**:
  - Removed unnecessary columns and handled missing data.
  - Encoded categorical variables (e.g., research experience) and standardized numerical features using Min-Max scaling.
- **Outcome**: Cleaned and standardized data, ready for model training.

### 5. Model Development
- **Objective**: Train and evaluate multiple machine learning models to predict admission probabilities.
- **Models Developed**:
  - Linear Regression
  - Decision Tree Regressor
  - Random Forest Regressor
  - Support Vector Machine (SVM)
  - Gradient Boosting Regressor
- **Evaluation Metrics**:
  - Mean Absolute Error (MAE)
  - Mean Squared Error (MSE)
  - R² Score
- **Best Model**: The Random Forest Regressor provided the highest accuracy and insight into feature importance.

## Results
The analysis revealed that the Random Forest Regressor was the most effective model, with high R² scores and low error rates. The model identified GRE scores and CGPA as the most influential factors for predicting admission probabilities, which aligns with expectations for graduate school applications.

## Acknowledgments
Special thanks to the Jamboree team for providing the dataset and to all contributors of the open-source libraries used in this project.
