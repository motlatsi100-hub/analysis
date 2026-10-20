# Boston Property Values Prediction Using Regression

## Project Overview

This project investigates the prediction of median owner-occupied home values across suburbs of Boston using statistical regression and machine learning techniques in R.

The main objective is to build, evaluate, and compare regression models that predict the median value of owner-occupied homes, measured in thousands of dollars, using 12 explanatory variables.

The project follows a structured statistical modelling workflow, including exploratory data analysis, multiple linear regression, variable selection, regularization, interaction modelling, prediction evaluation, and residual diagnostics.

## Dataset

The dataset contains **506 observations**, with each row representing a different Boston suburb.

- **Target variable:** Median value of owner-occupied homes, expressed in thousands of dollars.
- **Predictors:** 12 explanatory variables describing characteristics associated with property values.
- **Training set:** 400 observations.
- **Test set:** 106 remaining observations.

The assignment requires a unique sample of 400 observations for training, with the remaining 106 observations reserved for testing.

### Dataset Files

| File | Description |
|---|---|
| Excel dataset (`.xlsx` or `.xls`) | Contains the Boston property data used for analysis |
| `boston_vars.txt` | Describes the dataset variables and their meanings |
| RStudio project (`.Rproj`) | Opens the project in RStudio |
| Quarto source (`.qmd`) | Contains the report, R code, analysis, and interpretations |
| HTML report (`.html`) | Rendered, browser-readable version of the report |
| PDF report (`.pdf`) | Portable version of the completed report |

*Replace the example variable filename or file extensions above if your actual filenames differ.*

## Project Objectives

### 1. Exploratory Data Analysis

The dataset was explored to understand its structure, quality, and relationships before fitting the models. The analysis includes:

- Checking variable types and missing values.
- Examining distributions of the response and explanatory variables.
- Visualizing relationships between predictors and property values.
- Identifying potential outliers and notable patterns.

### 2. Full Multiple Linear Regression

A multiple linear regression model was fitted using all 12 explanatory variables.

The analysis considers:

- Overall model fit and explanatory power.
- Estimated regression coefficients.
- Statistical significance of individual predictors.
- Predictions for the test dataset.
- Test mean squared error (MSE).

### 3. Model Improvement and Variable Selection

Several approaches were considered to improve the initial full regression model.

**Backward stepwise regression**

Backward selection was used to investigate reduced predictor sets, with model selection based on the Akaike Information Criterion (AIC) and Bayesian Information Criterion (BIC).

**Ridge regression**

Ridge regularization applies an L2 penalty to regression coefficients, helping control model complexity and reduce overfitting.

**LASSO regression**

LASSO applies an L1 penalty, which can shrink some coefficients to zero and therefore perform variable selection.

Each model was evaluated on the same held-out test set using MSE. The results were compared to identify the best-performing model according to test prediction error.

### 4. Interaction Modelling

An interaction term was introduced into the selected model to investigate whether the relationship between one predictor and property values depends on another predictor.

The choice of interaction was motivated by the variables and patterns observed during exploratory analysis. The interaction model was evaluated using test-set predictions and MSE and compared with the selected model before adding the interaction.

### 5. Residual Diagnostics

Residual plots were used to investigate the assumptions and adequacy of the regression models, focusing on:

- **Linearity:** Whether the model adequately captures relationships between predictors and the response.
- **Homoscedasticity:** Whether residual variance is reasonably constant.
- **Normality:** Whether residuals are approximately normally distributed.

These diagnostics support interpretation of model limitations and the reliability of statistical inference.

### 6. Conclusion and Interpretation

The final report discusses the practical implications of the findings, including which variables are associated with higher or lower predicted property values, how model selection affects predictive performance, and whether the interaction term improves predictions.

The analysis also considers the limitations of the dataset, model assumptions, and the distinction between statistical association and causation.

## Model Evaluation

The principal prediction metric is mean squared error (MSE):

\[
\operatorname{MSE}=\frac{1}{n}\sum_{i=1}^{n}(y_i-\hat{y}_i)^2
\]

where \(y_i\) is the observed property value, \(\hat{y}_i\) is the predicted value, and \(n\) is the number of test observations.

A lower test MSE indicates smaller average squared prediction errors on the held-out test set. Because the target variable is measured in thousands of dollars, MSE is expressed in squared thousands of dollars.

The full regression, stepwise models, Ridge, LASSO, and interaction model are compared using their test performance, with the best model selected according to the evaluation results.

## Tools and Technologies

- **R:** Data analysis, statistical modelling, and prediction.
- **RStudio:** Project development and execution.
- **Quarto:** Reproducible reporting using `.qmd` source documents.
- **HTML and PDF:** Rendered report formats.
- **Excel:** Dataset storage.
- **Text file:** Variable descriptions and dataset documentation.

## Reproducibility

To reproduce the project:

1. Clone or download the repository.
2. Open the `.Rproj` file in RStudio.
3. Install the R packages required by the source document.
4. Confirm that the Excel dataset and `boston_vars.txt` are available at the file paths used by the code.
5. Open the `.qmd` file and review the analysis code.
6. Render the Quarto document to regenerate the HTML report and, where configured, the PDF report.

The same training/test split and any random seeds used in the original analysis should be retained when reproducing the results. This helps ensure that model comparisons are consistent.

## Limitations

- The analysis uses a sample of 400 observations for training and 106 for testing.
- Results depend on the selected sample, predictor variables, model assumptions, and model tuning.
- Regression relationships do not establish causation.
- Performance on this dataset does not guarantee equivalent prediction accuracy for other locations or housing markets.

## Conclusion

This project applies a complete regression modelling workflow to Boston property values, from exploratory analysis through model selection and residual diagnostics. By comparing a full linear model with stepwise regression, Ridge, LASSO, and interaction modelling, the analysis evaluates how alternative approaches affect prediction accuracy and model interpretation.

The project demonstrates the use of R and reproducible Quarto reporting for statistical analysis, predictive modelling, and evidence-based model comparison.

---

**Project:** Boston Property Values Prediction Using Regression  
**Language:** R  
**Report formats:** Quarto, HTML, and PDF  
**Dataset:** Boston suburb property values and explanatory variables