# Resume Classification using Machine Learning and NLP

## Overview
This project implements a machine learning-based resume classification system that automatically categorizes resumes into predefined job roles using Natural Language Processing (NLP) techniques.

The system processes raw resume text, performs text cleaning and feature extraction using TF-IDF, and applies a One-vs-Rest K-Nearest Neighbors (KNN) classifier for multi-class classification.

---

## Problem Statement
Recruitment processes often involve manual screening of resumes, which is time-consuming and inefficient. This project aims to:

- Automate resume classification
- Reduce manual effort in candidate screening
- Improve recruitment efficiency using machine learning

---

## Dataset Description

The dataset consists of resumes labeled across multiple job categories.

### Key Features:
- `Resume`: Raw text of resumes
- `Category`: Job category label
- `cleaned_resume`: Preprocessed text used for modeling

### Categories Include:
- Data Science
- HR
- Java Developer
- DevOps Engineer
- Business Analyst
- Mechanical Engineer
- Web Designing
- And more (25+ categories)

---

## Exploratory Data Analysis

- Distribution of resume categories visualized using count plots
- Pie chart representation of category proportions
- Word frequency analysis performed using NLTK
- Word cloud generated to identify dominant terms in resumes

---

## Methodology

### 1. Data Preprocessing
- Removal of URLs, mentions, hashtags, and special characters
- Conversion to lowercase
- Removal of non-ASCII characters
- Tokenization and stopword removal using NLTK

---

### 2. Feature Extraction
- TF-IDF Vectorization applied
- Maximum features limited to 1500
- English stopwords removed

---

### 3. Label Encoding
- Categorical labels converted into numerical format using LabelEncoder

---

### 4. Model Training

- Train-test split: 80/20
- Classifier: OneVsRestClassifier with K-Nearest Neighbors

---

## Model Details

- Algorithm: K-Nearest Neighbors (KNN)
- Strategy: One-vs-Rest for multi-class classification
- Feature Representation: TF-IDF
- Feature Size: 1500

---

## Results

### Model Performance

- Training Accuracy: 0.87
- Test Accuracy: 0.79

### Evaluation Metrics

- Precision, Recall, and F1-score calculated for each class
- Weighted F1-score indicates good overall performance
- Some classes show lower recall due to class imbalance

---

## Key Insights

- TF-IDF effectively captures important resume keywords
- KNN performs reasonably well for multi-class text classification
- Performance varies across categories due to imbalance and limited samples
- Common resume terms include "experience", "project", "management", and "data"

---

## Limitations

- Dataset imbalance across categories
- KNN is sensitive to feature space dimensionality
- No hyperparameter tuning performed
- Limited dataset size affects generalization

---

## Future Improvements

- Apply advanced models such as:
  - Logistic Regression
  - Support Vector Machines
  - Transformer-based models (BERT)

- Perform hyperparameter tuning
- Use larger and more balanced datasets
- Implement dimensionality reduction (PCA, LSA)
- Deploy as a web application

---

## Project Structure
├── resume_dataset.csv
├── resume_classifier.py
├── README.md

---

## Installation

### 1. Clone the Repository
git clone https://github.com/your-username/resume-classification.git
cd resume-classification

### 2. Install Dependencies
pip install -r requirements.txt

---

## Running the Project

python resume_classifier.py

---

## Conclusion

This project demonstrates how machine learning and NLP techniques can be applied to automate resume classification. The approach provides a scalable solution for recruitment systems, though further improvements in model selection and dataset quality are necessary for production-level deployment.

---

## Author

Sandeep S L  
MSc Data Analytics (Computational Science)  
Digital University of Kerala  

---

## License

This project is open-source and available under the MIT License.
