# 👩‍⚕️ Adenoma Analysis Project

This project investigates clinical and hormonal data related to adenoma diagnosis. Using an R-based pipeline, the project performs data cleaning, descriptive statistics, visualization, and inferential analysis to explore associations between patient characteristics (e.g., age, height, weight, hormone levels) and tumor features. 

---

##  📋 Table of Contents

- [Introduction](#introduction)
- [Data and Preprocessing](#data-and-preprocessing)
- [Statistical Analysis](#statistical-analysis)
- [Reproducibility and Usage](#reproducibility-and-usage)
- [Example Results](#example-results)

---

## 📝 Introduction

The goal of this project is to analyze a dataset (`adenoma.csv`) containing clinical and laboratory data of patients with and without adenoma. The analysis includes:
- Loading and preprocessing data.
- Generating descriptive statistics and visualizations.
- Testing associations and differences between groups (with/without adenoma).
- Building regression models and performing correlation analyses.

The methodology and rationale are detailed in the accompanying presentation.

---

## 📎 Data and Preprocessing

Data is imported from web link. 

```r
# Load the dataset
file_url <- "https://drive.google.com/uc?export=download&id=1ejSVvnWfX4elV1hOcQLsZKENaLznkQyH"
adenoma_file <- read.csv(file_url, 
                         header = TRUE, 
                         sep = ';', 
                         na.strings = c('-', '-99', ' ', 'NA'), 
                         dec = ",", 
                         stringsAsFactors = FALSE)

# Load required libraries
library(DescTools) 
library(ggplot2)
library(skimr)
library(tidyr)
library(dplyr)
library(corrr)
library(corrplot)

# Preprocessing
# Check for missing values in cases where Diagnosis == 0
skimr::skim(Without_adenoma_file)
```
---

## 📊 Statistical Analysis

Statistical tests include **correlation (Pearson, Spearman), t-tests, Wilcoxon tests**, and **ANOVA** to assess relationships between tumor volume, hormone levels, and other clinical variables.

**Multiple linear regression** and **logistic regression models** are used to examine the influence of various predictors on hormone levels and tumor volume. The project also uses mosaic plots to explore categorical data relationships.

---

## 🔧 Reproducibility and Usage

To reproduce the analysis:

1. Clone the repository:

   git clone https://github.com/yourusername/adenoma_analysis_project.git
   
   cd adenoma_analysis_project
   
2. Install the required R packages:
   
   install.packages(c("DescTools", "tidyverse", "skimr", "ggplot2", "tidyr", "dplyr", "corrr", "corrplot"))
   
3. Run the R script
   
---

## 🔍 Example Results

- **Multiple Correlations:**  
  [View Multiple Correlations Results](https://drive.google.com/file/d/1HfB2PU1SnOSna1vNHCls70237o70vIIh/view?usp=sharing)

- **Wilcoxon (Mann–Whitney) Test:**  
  [View Wilcoxon Test Results](https://drive.google.com/file/d/1mL23J9RnO2u99Ca2YlcqpSD8Ybtu1hBK/view?usp=sharing)

- **ANOVA:**  
  [View ANOVA Results](https://drive.google.com/file/d/1XCUM0XU990J-yY8NhHxfJWjwxm_L_MCs/view?usp=sharing)

- **Pearson Correlations:**  
  [View Pearson Correlations Results](https://drive.google.com/file/d/1akJSYXaGKHjPmCw5joF2KRaXimctz8fX/view?usp=sharing)

- **Multiple Linear Regression:**  
  [View Multiple Linear Regression Results](https://drive.google.com/file/d/18WidPq5DnzwQ7HG1k8QuVoL0hbGDRXXX/view?usp=sharing)

- **Paired t-Test:**  
  [View Paired t-Test Results](https://drive.google.com/file/d/1fRgiXvU0DSaCmZwx6Fpcy_RgxaZjAAx8/view?usp=sharing)
---
