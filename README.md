# Data Analytics Group Project: BMI and Its Relationship with Sleep Disorders, Blood Pressure, and Smoking

Welcome to the **Data Analytics Group Project** for our Data Analytics module in Semester 6. This project focuses on analyzing the relationship between Body Mass Index (BMI) and various health factors, such as sleep disorders, blood pressure, and smoking habits, using the **NHANES 2017-2018** dataset.

## Table of Contents
1. [Project Overview](#project-overview)
2. [Features](#features)
   - [Descriptive Statistics](#descriptive-statistics)
   - [Correlation Analysis](#correlation-analysis)
   - [Linear Regression](#linear-regression)
   - [Group Comparisons](#group-comparisons)
3. [Dataset Structure](#dataset-structure)
4. [Installation](#installation)
   - [Dependencies](#dependencies)
   - [Installing](#installing)
   - [Executing Program](#executing-program)
5. [Usage](#usage)
6. [Contributors](#contributors)
7. [License](#license)
8. [Help](#help)
9. [Acknowledgments](#acknowledgments)

## Project Overview

This project explores the relationship between **BMI** and health factors, including sleep disorders, blood pressure, and smoking, using the **NHANES 2017-2018 dataset**. The analysis employs statistical methods such as correlation analysis, linear regression, and group comparisons to investigate the associations between these health factors.

This project was developed using:
* **R** for data analysis and statistical modeling.
* **ggplot2** for data visualization.
* **dplyr** and **tidyr** for data manipulation.
* **survey** package for analyzing survey data.

The primary goal is to understand how these health factors interact, with a focus on public health implications related to obesity and sleep disorders.

## Features

### Descriptive Statistics
* **BMI Summary**: Descriptive statistics such as the mean, median, and standard deviation for BMI, sleep disorders, and other health-related variables.
* **Demographic Analysis**: Breakdown of BMI and sleep disorders by gender, age group, and ethnicity.

### Correlation Analysis
* **Correlation Between BMI and Sleep Disorders**: Examines the strength and direction of the relationship between BMI and sleep disorders.
* **Correlation with Other Health Factors**: Investigates how blood pressure and smoking correlate with BMI.

### Linear Regression
* **BMI and Sleep Disorders**: Linear regression model to predict sleep disorders based on BMI, controlling for age, gender, and other variables.

### Group Comparisons
* **ANOVA and t-tests**: Group comparisons (e.g., normal weight vs. obese) to explore how sleep disorders and smoking vary across BMI categories.

## Dataset Structure

The **NHANES 2017-2018** dataset is a publicly available dataset provided by the **Centers for Disease Control and Prevention (CDC)**. The dataset includes information from physical examinations, laboratory tests, and interviews, covering demographic, socioeconomic, and health-related data.

Key tables used:
* **demo_data**: Demographic data including age, gender, and race/ethnicity.
* **bm_data**: Body measures, including BMI.
* **slq_data**: Sleep disorder information.
* **bp_data**: Blood pressure measures.
* **smk_data**: Smoking history and current smoking status.

The dataset is nationally representative, making it relevant for public health research in the United States.

```r
# Example: Data loading and merging in R
demo_data <- read_xpt("DEMO_J.XPT")
bm_data <- read_xpt("BMX_J.XPT")
slq_data <- read_xpt("SLQ_J.XPT")

# Merging datasets
merged_data <- demo_data %>%
  inner_join(bm_data, by = "SEQN") %>%
  inner_join(slq_data, by = "SEQN")
```

