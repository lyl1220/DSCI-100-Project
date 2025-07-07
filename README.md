# Pulsar Classification Project

## Project Overview
This project aims to classify pulsar signals from radio frequency interference (RFI) noise using machine learning techniques. The dataset used is from the High Time Resolution Universe Survey (HTRU2). We apply a K-Nearest Neighbors (KNN) classifier to accurately distinguish pulsars from noise.

## Dataset
- **Name:** HTRU2
- **Description:** Contains statistical features extracted from pulsar candidates and noise samples.
- **Source:** [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/HTRU2)

## Technologies & Libraries
- Programming Language: R
- Key Packages:
  - tidyverse
  - tidymodels
  - GGally
  - themis
  - ggcorrplot

## Methodology
1. **Data Loading and Cleaning**  
   - Download dataset from URL  
   - Rename columns and convert target variable to factor  

2. **Data Splitting**  
   - Stratified split into 80% training and 20% testing sets  

3. **Preprocessing**  
   - Feature normalization (centering and scaling)  
   - Handle class imbalance with upsampling  

4. **Exploratory Data Analysis (EDA)**  
   - Visualize feature relationships using pair plots and correlation matrix  
   - Select features with high discriminative power  

5. **Model Training and Tuning**  
   - Perform 5-fold cross-validation to find optimal k in KNN  
   - Train KNN model on preprocessed data  

6. **Evaluation**  
   - Predict on test set  
   - Compute accuracy and generate confusion matrix  

## Results
- Best k value found: 3  
- Test accuracy: Approximately 96.17%  
- Confusion matrix indicates strong pulsar detection performance

## How to Run
```r
# Install required packages if not already installed
install.packages(c("tidyverse", "tidymodels", "GGally", "themis", "ggcorrplot"))

# Load libraries
library(tidyverse)
library(tidymodels)
library(GGally)
library(themis)
library(ggcorrplot)

# Run the scripts or code blocks in sequence for data processing, training, and evaluation
