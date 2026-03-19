## Reproducible dbGaP Phenotype Data Harmonization Pipeline in R

Reproducible R pipeline for cleaning, harmonizing, de-identifying, and structuring clinical phenotype data into dbGaP-compliant formats.

---

## Project Overview

The goal of this project is to transform raw phenotype data into standardized formats required for submission to dbGaP.

- Distinguishing subject-level vs. sample-level data  
- Performing data cleaning and validation  
- Resolving duplicate records and inconsistencies  
- Implementing two-step de-identification of IDs  
- Generating submission-ready data files and data dictionaries  

All steps are implemented programmatically using tidyverse-based workflows, ensuring reproducibility and scalability.

---

## Key Features

### Data Import and Cleaning

- Reads Excel-based phenotype and data dictionary files  
- Standardizes missing values and formats variables  

### Data Transformation

- Reorders and aligns variables with the data dictionary  
- Splits dataset into subject-level and sample-level components  

### Data Quality Control

- Detects and resolves duplicated subject and sample IDs  
- Handles inconsistent categorical values  

### De-identification Pipeline

- Generates randomized subject and sample IDs  
- Implements dbGaP-required two-step ID anonymization  

### Data Integration

- Merges externally provided key files  
- Maintains referential integrity across datasets  

### Feature Engineering

- Aggregates repeated measurements (e.g., average gestational age)  

### dbGaP File Generation

- Subject phenotype dataset (DS)  
- Subject-sample mapping file (SSM)  
- Data dictionary (DD) with properly formatted VALUE fields  

### Visualization

- Plotly-based visualization of phenotype relationships with custom tooltips  

---

## Technologies Used

- R  
- tidyverse (dplyr, tidyr, ggplot2)  
- readxl  
- here  
- plotly  
- dbGaPCheckup  
- openxlsx  

---

## Outputs

The pipeline generates dbGaP-compliant files:

- 5a_SubjectPhenotypes_DS.txt  
- 5b_SubjectPhenotypes_DD.xlsx  
- 3a_SSM_DS.txt  
- subjectKey.txt  
- sampleKey.txt  

---

## Reproducibility

- No manual editing of raw data  
- Uses the here package for portable file paths  
- Fully script-based workflow for easy reruns on updated datasets  

---

## Key Skills Demonstrated

- Data wrangling and transformation (tidyverse)  
- Clinical and genomic data standardization  
- Reproducible research practices  
- Data validation and quality control  
- Pipeline development in R  
- Preparation of dbGaP submission files  

---

## Notes

This project was completed as an independent academic assignment simulating real-world data submission workflows for genomic studies.
