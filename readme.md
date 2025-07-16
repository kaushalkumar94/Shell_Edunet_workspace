# 🔥 Fire Detection and Classification using MODIS Satellite Data

This project was developed as part of my internship at **Edunet Foundation**, focusing on detecting and classifying fire occurrences in India using satellite data and machine learning techniques.

##  Dataset

The dataset includes fire-related data from the **MODIS satellite** for the years:

- `modis_2021_India.csv`
- `modis_2022_India.csv`
- `modis_2023_India.csv`

These files were combined into a single DataFrame for a comprehensive analysis.

##  Problem Statement

The goal of this project is to:
- **Detect patterns in fire incidents** across India using satellite data.
- **Classify** data points to identify whether a given entry indicates a fire event.
- **Evaluate multiple machine learning models** for this classification task.

##  Tools & Technologies

- **Languages**: Python
- **Libraries**: 
  - Data Handling: `pandas`, `numpy`
  - Visualization: `matplotlib`, `seaborn`
  - ML Models: `scikit-learn` (`LogisticRegression`, `RandomForestClassifier`, `KNeighborsClassifier`)
  - Feature Selection: `SelectKBest`, `f_classif`, `mutual_info_classif`
  - Evaluation: `accuracy_score`, `classification_report`, `ConfusionMatrixDisplay`

##  Approach

1. **Data Loading and Merging**
   - Loaded fire data from 2021, 2022, and 2023
   - Concatenated into a single dataset

2. **Data Preprocessing**
   - Feature selection using `SelectKBest` with `f_classif` and `mutual_info_classif`
   - Feature scaling using `StandardScaler`

3. **Model Training & Evaluation**
   - Trained and tested multiple models:
     - Logistic Regression
     - Random Forest
     - K-Nearest Neighbors
   - Evaluated with:
     - Accuracy score
     - Confusion matrix
     - Classification report

##  Results

Each model's performance was evaluated on:
- **Accuracy**
- **Precision, Recall, F1-Score**
- **Confusion Matrix Visualization**

_Results showed that Random Forest gave the best overall performance for fire classification._

##  Future Improvements

- Use **deep learning models (CNN/LSTM)** on geospatial images if available
- Integrate **real-time data** using APIs or Google Earth Engine
- Add **geo-visualization** to map fire locations

##  How to Run

1. Clone the repository  
   ```bash
   git clone https://github.com/yourusername/fire-detection-edunet.git
   cd fire-detection-edunet
