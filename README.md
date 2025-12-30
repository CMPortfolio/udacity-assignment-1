# Heart Disease Prediction Project

## Project Description

This project implements a complete machine learning solution for predicting heart disease in patients using clinical and demographic features. The project follows the **CRISP-DM (Cross-Industry Standard Process for Data Mining)** methodology, ensuring a systematic and thorough approach to data science.

### Motivation

Heart disease is the leading cause of death globally, accounting for approximately 17.9 million deaths each year. Early detection and accurate diagnosis are crucial for:
- Preventing fatal outcomes through early intervention
- Reducing healthcare costs by efficient resource allocation
- Improving patient outcomes with timely treatment
- Supporting clinical decision-making for healthcare professionals

This project aims to build a predictive model that can assist in identifying patients at risk of heart disease based on their clinical measurements and demographic information.

## Dataset

The project uses the **Heart Disease Prediction Dataset** from Kaggle, which contains:
- **270 samples** with **13 features** and 1 target variable
- Features include: Age, Sex, Blood Pressure, Cholesterol, Maximum Heart Rate, Exercise Angina, ST Depression, and other clinical indicators
- Target variable: Binary classification (Presence/Absence of heart disease)

## Libraries Used

- **pandas** - Data manipulation and analysis
- **numpy** - Numerical computations
- **matplotlib** - Data visualization
- **seaborn** - Statistical data visualization
- **scikit-learn** - Machine learning algorithms and utilities
  - Logistic Regression
  - Random Forest Classifier
  - StandardScaler, LabelEncoder
  - train_test_split, cross_val_score
  - Evaluation metrics (accuracy, precision, recall, F1-score, ROC-AUC)
- **joblib** - Model serialization

## Project Structure

```
udacity-assignment-1/
│
├── Heart_Disease_Prediction.csv    # Dataset
├── heart_disease_prediction.ipynb   # Main Jupyter notebook
├── README.md                        # This file
├── requirements.txt                 # Python dependencies
└── models/                          # Saved model artifacts (created after running notebook)
    ├── best_heart_disease_model.pkl
    └── label_encoder.pkl
```

## How to Run

### Prerequisites

- Python 3.7 or higher
- Jupyter Notebook or JupyterLab

### Installation Steps

1. **Clone or download this repository**

2. **Create a virtual environment (recommended)**
   ```bash
   python -m venv venv
   
   # On Windows:
   venv\Scripts\activate
   
   # On macOS/Linux:
   source venv/bin/activate
   ```

3. **Install required packages**
   ```bash
   pip install -r requirements.txt
   ```

4. **Launch Jupyter Notebook**
   ```bash
   jupyter notebook
   ```

5. **Open and run the notebook**
   - Open `heart_disease_prediction.ipynb`
   - Run all cells sequentially (Cell → Run All)
   - The notebook will:
     - Load and explore the data
     - Preprocess the features
     - Train two classification models
     - Evaluate and compare model performance
     - Save the best model to the `models/` directory

### Running Individual Sections

You can also run the notebook section by section:
1. **Business Understanding** - Read the markdown explanations
2. **Data Understanding** - Explore the dataset
3. **Data Preparation** - Preprocess the data
4. **Modeling** - Train the models
5. **Evaluation** - Compare model performance
6. **Deployment Scenario** - Test with a new patient case

## Results and Findings

### Business Questions Answered

The project addresses five key business questions:

1. **Can we accurately predict the presence of heart disease?**
   - **Answer**: Yes, with 85.2% accuracy and 91.7% recall (most critical for medical diagnosis)

2. **Which factors are most strongly associated with heart disease?**
   - **Answer**: Maximum heart rate, ST depression, exercise angina, and number of affected vessels are the most predictive factors

3. **What age groups show the highest risk of heart disease?**
   - **Answer**: Patients in their 60s and 70s show the highest heart disease rates

4. **How does exercise capacity relate to heart disease risk?**
   - **Answer**: Patients with heart disease have 20+ bpm lower maximum heart rates, indicating lower exercise capacity is strongly associated with higher risk

5. **What combination of risk factors creates the highest probability?**
   - **Answer**: Patients with 3+ risk factors show 70%+ heart disease rates, demonstrating that combinations are more predictive than individual factors

### Model Performance

The project compares two classification models:

1. **Logistic Regression** - A baseline linear model
2. **Random Forest Classifier** - A nonlinear ensemble model

Both models are evaluated using:
- **Accuracy**: Overall correctness
- **Precision**: Ability to avoid false positives
- **Recall**: Ability to identify all true cases (critical for medical diagnosis)
- **F1-Score**: Balanced measure of precision and recall
- **ROC-AUC**: Overall discriminative ability

### Key Findings

- The dataset was clean with **no missing values**, making preprocessing straightforward
- Both models achieved **high performance** on the test set
- The **Logistic Regression** model achieved the best overall performance (89.9% ROC-AUC)
- Feature importance analysis reveals which clinical indicators are most predictive
- The models can effectively distinguish between patients with and without heart disease
- **Age, exercise capacity, and combinations of risk factors** are key predictors identified through analysis

### Feature Importance

The Random Forest model provides insights into which features are most important for prediction, helping identify key risk factors that clinicians should monitor.

## Project Methodology (CRISP-DM)

The notebook follows the CRISP-DM framework:

1. **Business Understanding** - Define objectives and success criteria
2. **Data Understanding** - Explore and visualize the dataset
3. **Data Preparation** - Clean, encode, and scale features
4. **Modeling** - Train and compare multiple models
5. **Evaluation** - Comprehensive performance assessment
6. **Deployment** - Model saving and prediction scenario

## Important Notes

⚠️ **Medical Disclaimer**: This model is for **educational purposes only**. Medical decisions should always be made by qualified healthcare professionals. This prediction should not replace professional medical diagnosis.

## Future Improvements

- Hyperparameter tuning using GridSearchCV or RandomizedSearchCV
- Feature engineering to create new meaningful features
- Ensemble methods combining multiple models
- Web application or API for real-time predictions
- Model monitoring and regular retraining with new data
- Exploration of additional algorithms (XGBoost, SVM, Neural Networks)

## Acknowledgments

- Dataset: Heart Disease Prediction Dataset from Kaggle
- Methodology: CRISP-DM framework
- Libraries: Open-source Python data science ecosystem

## License

This project is for educational purposes.

---

**For questions or issues, please refer to the notebook comments and markdown explanations for detailed guidance.**

