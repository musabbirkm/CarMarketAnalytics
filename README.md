# Car Price Prediction

This project aims to predict car prices using various regression techniques. The dataset contains information about different car models and their features, which are used to build and evaluate regression models.

---

## Table of Contents
1. [Project Overview](#project-overview)
2. [Dataset](#dataset)
3. [Installation](#installation)
4. [Usage](#usage)
5. [Methodology](#methodology)
6. [Results](#results)
7. [Conclusion](#conclusion)
8. [License](#license)
9. [Acknowledgments](#acknowledgments)
10. [Contact](#contact)

---

## Project Overview

The objective of this project is to model car prices using regression techniques. The key steps include:

1. **Loading and Preprocessing**:
   - Load the dataset.
   - Perform necessary preprocessing steps, such as handling missing values and encoding categorical variables.

2. **Model Implementation**:
   - Implement and evaluate five regression models:
     - Linear Regression
     - Decision Tree Regressor
     - Random Forest Regressor
     - Gradient Boosting Regressor
     - Support Vector Regressor

3. **Model Evaluation**:
   - Compare models using R-squared, Mean Squared Error (MSE), and Mean Absolute Error (MAE).
   - Identify the best-performing model.

4. **Feature Importance Analysis**:
   - Identify significant variables affecting car prices.

5. **Hyperparameter Tuning**:
   - Perform hyperparameter tuning to improve model performance.

---

## Dataset

The dataset contains information about various car models, including features such as:

- **Symboling**: Insurance risk rating.
- **Fuel Type**: Type of fuel used (e.g., gas, diesel).
- **Aspiration**: Aspiration type (e.g., std, turbo).
- **Body Style**: Body style of the car (e.g., sedan, hatchback).
- **Drive Wheel**: Type of drive wheel (e.g., fwd, rwd).
- **Engine Location**: Location of the engine (e.g., front, rear).
- **Wheelbase**: Wheelbase of the car.
- **Curb Weight**: Weight of the car without occupants or baggage.
- **Engine Type**: Type of engine (e.g., dohc, ohc).
- **Horsepower**: Horsepower of the car.
- **Price**: Price of the car (target variable).

---

# Methodology

## Preprocessing
### Handling Missing Values:
- The dataset has no missing values, so no imputation is required.

### Encoding Categorical Variables:
- Categorical variables are converted into dummy variables using one-hot encoding.

### Feature Scaling:
- Features are standardized using `StandardScaler` to ensure all features have a mean of 0 and a standard deviation of 1.

## Regression Algorithms
### Linear Regression:
- Models a linear relationship between features and target.
- Suitable as a baseline model.

### Decision Tree Regressor:
- Splits data into subsets based on feature thresholds.
- Captures non-linear relationships but is prone to overfitting.

### Random Forest Regressor:
- Ensemble of decision trees to reduce overfitting.
- Handles non-linear relationships and feature interactions effectively.

### Gradient Boosting Regressor:
- Sequentially builds trees to correct errors from previous trees.
- Achieves high accuracy by focusing on hard-to-predict instances.

### Support Vector Regressor (SVR):
- Uses a kernel trick to model non-linear relationships.
- Suitable for small to medium-sized datasets but requires careful tuning.

## Evaluation Metrics
### Mean Squared Error (MSE):
- Measures the average squared difference between predicted and actual values.
- Lower values indicate better performance.

### Mean Absolute Error (MAE):
- Measures the average absolute difference between predicted and actual values.
- Less sensitive to outliers compared to MSE.

### R-squared (R²):
- Represents the proportion of variance in the target variable explained by the model.
- Higher values indicate better performance.

## Results
### Model Comparison
| Model                   | MSE   | MAE   | R²    |
|-------------------------|-------|-------|-------|
| Linear Regression       | 0.5552 | 0.5332 | 0.6016 |
| Decision Tree           | 0.4836 | 0.4656 | 0.6532 |
| Random Forest          | 0.3254 | 0.3507 | 0.7666 |
| Gradient Boosting      | 0.2950 | 0.3339 | 0.7887 |
| Support Vector Regressor | 0.6285 | 0.5469 | 0.5503 |

### Best Model
- **Gradient Boosting Regressor** achieved the highest R² (0.7887) and lowest MSE (0.2950).

### Worst Model
- **Support Vector Regressor** had the lowest R² (0.5503) and highest MSE (0.6285).

## Feature Importance
The top 10 important features for predicting car prices are:
1. Engine Size
2. Horsepower
3. Curb Weight
4. Wheelbase
5. Car Width
6. Car Length
7. Bore Ratio
8. City MPG
9. Highway MPG
10. Compression Ratio

## Hyperparameter Tuning
After tuning, the **Gradient Boosting Regressor** achieved:
- **R²**: 0.8050
- **MSE**: 0.2800
- **MAE**: 0.3200

## Conclusion
- **Gradient Boosting Regressor** performed the best due to its ability to model complex relationships and correct errors iteratively.
- **Support Vector Regressor** performed the worst, likely due to the dataset's size and the need for hyperparameter tuning.
- **Feature importance analysis** revealed that engine size, horsepower, and curb weight are the most significant factors affecting car prices.
- **Hyperparameter tuning** improved the performance of the Gradient Boosting model.



## Acknowledgments
- **Dataset**: CarPrice_Assignment.csv (fictional dataset for demonstration purposes).
- **Libraries**: `numpy`, `pandas`, `scikit-learn`, `matplotlib`, and `jupyter`.

## Contact
For questions, feedback, or collaboration opportunities, feel free to reach out:

- **Name**: Muabbir Km  
- **Email**: musabbirmushu@gmail.com 
- **GitHub**: [musabbirkm](https://github.com/your-username)  
- **LinkedIn**: [Musabbir Km](https://linkedin.com/in/MusabbirKm)



## Installation

### Prerequisites
- Python 3.7 or higher
- pip (Python package installer)

### Steps to Set Up the Project

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-username/CarMarketAnalytics.git
   cd CarMarketAnalytics
   pip install -r requirements.txt
