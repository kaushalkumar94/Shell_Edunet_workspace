#  Fire Detection and Classification using MODIS Satellite Data

This repository contains a full pipeline for detecting and classifying fire occurrences in India using MODIS satellite data and machine learning. Developed during an internship at **Edunet Foundation**, it is organized for clarity and ease of use.

---

## Repository Structure & Workflow

To get the most out of this repository, follow the step-by-step sequence below:

1. **Exploratory Data Analysis (EDA)**
   - File: `Exploratory Data Analysis (EDA).ipynb`
   - Purpose: Explore raw MODIS data for trends, distributions, and possible data quality issues.  
   **Start here** to understand what the data looks like before modeling.

2. **Data Loading and Cleaning**
   - File: `data_loading_cleaning.ipynb`
   - Purpose: Load the three years of MODIS data, merge them, handle missing values, encode categorical variables, and perform preliminary feature selection.  
   **Ensures your data is ready for analysis and modeling.**

3. **Model Training and Evaluation**
   - File: `model_training_and_evaluation.ipynb`
   - Purpose: Apply feature selection, build machine learning models (Logistic Regression, Random Forest, KNN), and evaluate their performance on classification tasks.  
   **Test and compare models using cleaned data.**

### Data Files

- `modis_2021_India.csv`
- `modis_2022_India.csv`
- `modis_2023_India.csv`

> All notebooks files are available in the project root directory.

---

## How to Use

1. **Clone the repository** git clone https://github.com/kaushalkumar94/fire-detection-edunet.git
cd fire-detection-edunet
2. **Install dependencies**
3. **Run the notebooks sequentially:**
- `Exploratory Data Analysis (EDA).ipynb`
- `data_loading_cleaning.ipynb`
- `model_training_and_evaluation.ipynb`

---

## Data Columns

- `latitude`, `longitude`, `brightness`, `scan`, `track`, `acq_date`, `acq_time`, `satellite`, `instrument`, `confidence`, `version`, `bright_t31`, `frp`, `daynight`, `type`

---

## Results

- **Models Evaluated:** Logistic Regression, Decision Tree, Random Forest, K-Nearest Neighbors (KNN)
- **Metrics:** Accuracy, Precision, Recall, F1-Score, Confusion Matrix

### Performance Comparison

| Model                 | Accuracy | Precision    | Recall       | F1-Score    |
|-----------------------|----------|--------------|--------------|-------------|
| Logistic Regression   | 0.5858   | 0.58 (avg)   | 0.59 (avg)   | 0.58 (avg)  |
| Decision Tree         | 0.9499   | 0.95 (avg)   | 0.95 (avg)   | 0.95 (avg)  |
| Random Forest         | 0.9780   | 0.98 (avg)   | 0.98 (avg)   | 0.98 (avg)  |
| K-Nearest Neighbors   | 0.9311   | 0.94 (avg)   | 0.93 (avg)   | 0.93 (avg)  |

> **Random Forest consistently achieved the best overall performance (Accuracy: 97.80%), making it the chosen model for this task.**

#### Example Classification Report (Random Forest)
          precision    recall  f1-score   support

       0       0.97      0.96      0.97     45710
       2       0.96      0.97      0.97     45710
       3       1.00      1.00      1.00     45711

accuracy                           0.98    137131

- **Visualizations:** Confusion matrix plots and per-class metrics show Random Forest’s reliable detection for all fire types.

---

## Future Enhancements

- Integrate deep learning models (CNN, LSTM) for image-based or sequential analysis.
- Enable real-time predictions using streaming APIs or Google Earth Engine.
- Add geo-visualization features to present fire locations on interactive maps.

---

## Author

[**Kaushal Kumar**]

---

_Recommendation: Always begin with EDA, process and clean data, and then train and evaluate your models for clear reproducibility and best results._


   

