# Data Analytics Group Project: BMI and Its Relationship with Sleep Disorders, Blood Pressure, and Smoking

Welcome to my **Data Analytics Group Project** for my Data Analytics module in Semester 6 for my BSc in Computing. This project focuses on analyzing the relationship between Body Mass Index (BMI) and various health factors, such as sleep disorders, blood pressure, and smoking habits, using the **NHANES 2017-2018** dataset.

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

## Installation

### Dependencies
- **R** (version 4.2.2 or higher)
- **RStudio** (optional, but recommended for running the R scripts)
- **Required R packages**:
  - ggplot2
  - dplyr
  - tidyr
  - haven
  - survey

### Installing

1. **Clone the Repository**:

   ```bash
   git clone https://github.com/yourusername/bmi-sleep-analysis.git
   ```

2. **Install Required R Packages: After opening R or RStudio, install the required packages**:
   ```r
   install.packages(c("ggplot2", "dplyr", "tidyr", "haven", "survey"))
   ```

3. **Download the NHANES 2017-2018 Dataset**: Download the dataset files from the CDC's NHANES website.
4. **Set Up Working Directory**: Set the working directory to the location of the dataset files:
   ```bash
   setwd("path/to/dataset/folder")
   ```

### Executing Program   

1. **Run the R Scripts**: After installing the necessary packages and setting up the dataset, run the provided R scripts to load and analyze the data.
   ```r
   source("data_analysis.R")
   ```

2. **Generate Visualizations**: The R script will generate various visualizations, including:
      -   BMI distribution by sleep disorder status.
      -   Correlation plots between BMI and other health factors.

4. **View Results**: The script will output the descriptive statistics, correlation results, and regression models directly in the R console or as a saved output file.

## Usage

The project provides a comprehensive analysis of the relationship between BMI and health factors using the NHANES 2017-2018 dataset.

### Correlation Analysis
Run the correlation analysis to examine how BMI is related to sleep disorders and other health outcomes.

### Linear Regression
The regression model allows you to predict sleep disorder status based on BMI while controlling for demographic variables like age and gender.

### Group Comparisons
Perform t-tests and ANOVA to compare different groups (e.g., smokers vs. non-smokers) and their health outcomes.

## Contributors

- **Daniel Gallagher** - Lead Data Analyst responsible for the BMI and sleep disorder correlation analysis.
- **Calvin Harvey** - Data Scientist responsible for blood pressure and smoking analysis.
- **Eryk Gloginski** - Data Visualization Specialist responsible for visualizing trends across demographic groups.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.

## Help

If you encounter any issues during the setup or execution of the analysis, ensure the following:

- **R** and required packages are installed correctly.
- The **NHANES dataset** files are downloaded and placed in the correct directory.
- The **working directory** in the R script matches the location of your dataset files.

If problems persist, please contact the contributors for assistance.

## Acknowledgments

Special thanks to:

- **NHANES** for providing the dataset used in this analysis.
- **RStudio** for offering a robust IDE for R development.
- **Stack Overflow** for providing valuable troubleshooting advice during the development process.

   



