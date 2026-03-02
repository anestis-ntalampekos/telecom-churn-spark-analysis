# Telecom Customer Churn Analysis with Apache Spark

This project analyzes customer churn data from a telecommunications provider using Apache Spark (PySpark).
The goal was to explore churn patterns, perform feature engineering, and build a machine learning model to predict monthly charges.

## Technologies

* Python
* Apache Spark (PySpark)
* Spark SQL
* Machine Learning (Spark MLlib)
* Google Colab

## Dataset

The dataset contains customer information such as:

* Age
* Tenure
* Monthly charges
* Contract type
* Payment method
* Country
* Services used
* Churn indicator

The dataset includes approximately 10,000 telecom customers.

## Data Processing

The following steps were implemented:

### Data Cleaning

* Removal of rows with missing values in the target variable (CHURN)
* Median imputation for numerical fields
* Handling missing values in:

  * AGE
  * TENURE_MONTHS
  * MONTHLY_CHARGES
  * TOTAL_CHARGES

### Feature Engineering

New features were created to improve analysis:

* NUM_SERVICES
* AVG_CHARGE_PER_MONTH
* IS_LONG_TENURE

### Exploratory Analysis

The analysis identified important churn patterns such as:

* Higher churn in month-to-month contracts
* Higher churn among customers with fewer services
* Slightly higher charges among customers who churn

### Spark SQL Analysis

Business-related queries were executed to analyze:

* Churn by contract type
* Churn by number of services
* Churn by country
* Average charges by churn status

### Machine Learning Model

A **Decision Tree Regressor** was implemented to predict monthly charges using:

* Customer demographics
* Services used
* Contract type
* Country
* Customer activity

Pipeline steps:

* StringIndexing
* OneHotEncoding
* Feature Vector Assembly
* Decision Tree Model

## Model Evaluation

Model performance:

* RMSE ≈ 7.87
* R² ≈ 0.49

These results indicate that the model captures part of the variability of monthly charges but additional features may improve performance.

## Project Structure

notebook/
telecom_churn_spark.ipynb

