<!-- # Jamboree Admission Analysis -->
<p align="center">
  <img src="images/jamboree.jpg" alt="Jamboree Logo" width="300">
</p>

A data-driven approach to predict admission chances using academic and personal factors.

## Overview
This project explores how factors like GRE, TOEFL scores, CGPA, and research experience influence university admission decisions. Our goal is to provide insights and predictions to help students make informed application choices.

## Key Features
- **Data Analysis & Visualization**: Understand the influence of each factor.
- **Model Development**: Predict admission chances using Linear Regression, Random Forest, and other models.
- **Insights & Recommendations**: Identify key areas to focus on for improving admission chances.

## Data
- **GRE Score** (0-340)
- **TOEFL Score** (0-120)
- **University Rating** (1-5)
- **SOP & LOR** Ratings (1-5)
- **CGPA** (0-10)
- **Research Experience** (0 or 1)

Stored in `data/Jamboree.csv`.

## Methodology
1. **Data Exploration**: Identified missing values, outliers, and data distributions.
2. **Data Visualization**: Created histograms and correlation heatmaps.
   - ![Histogram](images/histogram.png)
   - ![Correlation Heatmap](images/correlation_heatmap.png)
3. **Statistical Analysis**: Tested relationships using ANOVA, correlation tests, and Chi-square.
4. **Data Preprocessing**: Scaled numerical features, encoded categorical variables.
5. **Model Development**: Evaluated models using MAE, MSE, and R² scores.

## Results
- **Best Model**: Random Forest Regressor
- **Top Factors**: CGPA, GRE, TOEFL

| Model                  | MAE    | R²    | Cross-Validation R² |
|------------------------|--------|--------|---------------------|
| Linear Regression      | 0.043  | 0.816  | 0.790               |
| Random Forest          | 0.046  | 0.785  | 0.778               |
| Gradient Boosting      | 0.045  | 0.788  | 0.763               |

## Key Insights
- **CGPA** is consistently the strongest predictor.
- **GRE & TOEFL** scores are also influential, particularly in competitive programs.
- **Research** experience positively impacts university ratings.

## Recommendations
- **Focus on CGPA**: Prioritize academic performance for better chances.
- **Improve Test Scores**: Higher GRE/TOEFL scores increase competitiveness.
- **Engage in Research**: Adds value, especially for top-rated universities.

## Acknowledgments
Thanks to the Jamboree team for the dataset and the open-source community for tools and libraries.

---
For more details or to collaborate, please feel free to reach out!
