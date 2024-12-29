# Predictive Modeling for Agriculture

## Project Overview
This machine learning project helps farmers optimize crop selection based on soil measurements. Using data from soil_measures.csv, the system predicts optimal crop types given key soil metrics: nitrogen (N), phosphorous (P), potassium (K), and pH levels.

## Dataset
- **Source**: soil_measures.csv
- **Features**: 
  - N: Nitrogen content ratio
  - P: Phosphorous content ratio  
  - K: Potassium content ratio
  - pH: Soil pH value
- **Target**: Crop type (categorical)

## Technical Workflow

### 1. Data Import & Preprocessing
- Load and inspect dataset
- Handle any missing values or anomalies
- Split data into training (80%) and test (20%) sets using stratified sampling
- Scale features using StandardScaler

### 2. Initial Feature Analysis
- Individual feature evaluation using Logistic Regression
- F1 score calculation for each soil measurement
- Identification of best predictive feature

### 3. Model Development

#### Random Forest Classifier
- Base implementation with default parameters
- Performance evaluation using:
  - Classification report
  - F1 score
  - Feature importance analysis

#### Logistic Regression with Feature Interactions
- Polynomial feature generation (degree=2)
- Model training on scaled data
- Performance evaluation with classification report

### 4. Model Optimization
- GridSearchCV implementation for Random Forest
- Hyperparameter tuning:
  - n_estimators: [100, 200]
  - max_depth: [None, 10, 20]
  - min_samples_split: [2, 5, 10]

### 5. Performance Analysis
- Model comparison using F1 scores
- Feature importance ranking
- Best model selection based on performance metrics

## Technologies Used
- Python
- scikit-learn
- Pandas
- NumPy

## Key Outputs
- Best predictive soil measurement
- Model performance metrics
- Feature importance rankings
- Optimized model parameters

## Business Value
- Helps farmers make data-driven decisions for crop selection
- Identifies most important soil measurements
- Reduces cost by prioritizing crucial soil tests
- Optimizes crop yield through better planning
