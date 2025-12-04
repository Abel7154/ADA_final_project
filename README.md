
# Advanced Data Analysis Final Project – Gastroesophageal Cancer Outcomes

## Project Description
This repository contains the R Markdown code for my Advanced Data Analysis (ADA) final project.  
The project examines racial and sex differences in stage at diagnosis and overall survival among
patients with gastroesophageal cancer treated at [Siteman Cancer Center] between 2021 and 2025.

Using a retrospective cohort exported from REDCap, I:
- Described patient sociodemographic and clinical characteristics
- Evaluated racial and sex disparities in late (stage III–IV) vs early (stage I–II) diagnosis
- Examined racial and sex differences in overall survival using Kaplan–Meier curves and Cox models

## Files Included
- `Final_Project.Rmd`: R Markdown file containing all data cleaning, analysis, tables, figures, and interpretation
- `README.md`: This file, describing the project and how to run the code
- **Data file (not included):** The code assumes a dataset named `RetrospectiveStudyOf_DATA.csv`
  containing the analytic cohort of 150 gastroesophageal cancer patients.
  The dataset is **not** shared in this repository due to HIPAA, patient privacy and IRB restrictions.
  It is stored locally in the working directory.

## What the Code Does
The R Markdown file:
- Reads in the REDCap export (`RetrospectiveStudyOf_DATA.csv`) from a local, secure location
- Recodes variables (race, sex, Barrett’s esophagus, tobacco use, H. pylori, cancer type, stage, treatments, and out status)
- Creates analytic datasets for:
  - Late (III–IV) vs early (I–II) clinical stage at diagnosis
  - Overall survival in months from diagnosis to death or last follow-up
- Produces:
  - **Table 1:** Overall sociodemographic and clinical characteristics
  - Univariable and multivariable logistic regression models for late vs early stage
  - Kaplan–Meier survival curves overall, by race, and by sex
  - Multivariable Cox proportional hazards model for overall survival
  - **Table 2:** Multivariable logistic regression for late (III–IV) vs early (I–II) stage
  - **Table 3:** Multivariable Cox proportional hazards model for overall survival
  
## How to Run the Code
1. Obtain secure access to the patient-level REDCap dataset used for this project  
   (file name assumed: `RetrospectiveStudyOf_DATA.csv`).  
   *Note: This dataset is not shared in this repository due to privacy and IRB restrictions.*
2. Save the CSV file in the same folder as `Final_Project.Rmd`.
3. Open `Final_Project.Rmd` in RStudio.
4. Install any required packages if prompted (e.g., `tidyverse`, `table1`, `survival`, `survminer`, `broom`).
5. Knit the R Markdown document to HTML.

Without access to the underlying dataset, the code will not run fully,
but the repository still documents the analysis workflow and code structure.

## Author
- Name: Abel Abebe  
- Course: Advanced Data Analysis (ADA)  
- Program: MPH in Epidemiology/Biostatistics, Washington University in St. Louis  
- Date: December 2025
  