# Home Credit Default Risk

### Introduction

Many individuals face difficulty obtaining loans due to limited or non-existent credit histories. Unfortunately, this group is often vulnerable to exploitation by untrustworthy lenders.

Home Credit aims to promote financial inclusion for the unbanked by offering a safe and positive borrowing experience. To ensure that this underserved population receives fair loan opportunities, Home Credit leverages a wide range of alternative data - including telecom and transactional information - to predict clients' repayment potential.

Although Home Credit currently uses various statistical and machine learning techniques to make these predictions, they are continuously working to unlock the full potential of their data. By refining these methods, they aim to ensure that clients capable of repayment are not turned away and that loans are provided with terms - such as principal, maturity, and repayment schedules - that set clients up for long-term financial success.

### Goal

The objective of this project is to create a reliable predictive model for Home Credit, using alternative data to assess the risk of default among prospective clients and support responsible lending decisions.

### Objectives

To achieve this goal, the following objectives have been established:

- Download, load and clean the dataset.
- Conduct exploratory data analysis and visualize data to identify underlying patterns.
- Perform statistical inference to validate findings.
- Apply machine learning models to predict the probability of client default.
- Summarize results and provide actionable recommendations based on the analysis.

## Exploratory Data Analysis

In this section, the dataset is explored by performing the following:

- Uploading and providing an overview of the dataset
- Generating charts and summaries to visualize key insights
- Analyzing statistics to identify correlations between features and the target variable

## Statistical Inference

This section focuses on statistical inference to evaluate:

- Whether there is a difference in the distribution of age between individuals who defaulted and those who did not
- The significance of the correlation between categorical independent variables and the dependent variable

## Feature Engineering 

Before training machine learning models, the dataset is prepared by:

- Merging all tables into a single dataset to create a comprehensive view of the data
- Generating new features to uncover valuable patterns
- Developing functions to calculate sums, means, maximum and minimum values, various financial ratios, differences, and new categorical values

## Statistical Modeling

In this section, statistical modeling is performed by:

- Utilizing a dummy classifier as a benchmark
- Implementing LightGBM for model training
- Removing low-importance and highly correlated features
- Conducting hyperparameter tuning using Optuna
- Adjusting thresholds to minimize false negatives

## Conclusions

- **Target Variable Definition:** The target variable distinguishes clients with repayment difficulties in a highly imbalanced dataset (92% non-default).
- **KDE & Categorical Analysis:** KDE plots and categorical analyses indicated that higher external scores, longer employment duration, and greater education levels correlate with lower default risks.
- **LightGBM Performance:** LightGBM was chosen for its efficiency with large datasets and handling of categorical features, achieving a validation PR AUC of 0.2663 and AUC of 0.7805.
- **Threshold Adjustment:** Adjusting the threshold reduced false negatives, increasing recall to 73% but lowering precision.
- **Feature Importance & SHAP Analysis:** Key features, including external scores and annuity-to-credit ratios, were highlighted through SHAP analysis, demonstrating their importance in model predictions.

## License

This project is licensed under the [MIT License](LICENSE).

