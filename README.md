
# Car Price Prediction using Linear Regression



## Overview
This project builds a linear regression model to predict the Manufacturer's Suggested Retail Price (MSRP) of cars based on various features such as model year, fuel efficiency, premium version status, and more.



## Dataset
The dataset consists of 28,143 records with 8 main features:
- `model_year` - Year of manufacture
- `brand` - Manufacturer of the car
- `model` - Specific model name
- `type` - Car category (SUV, Sedan, etc.)
- `miles_per_gallon` - Fuel efficiency
- `premium_version` - Indicator if the car is a premium version
- `msrp` - Target variable (price in dollars)
- `collection_car` - Indicator if the car is a collectible



## Data Preprocessing
1. **Handling Missing Values**
   - Missing values in `miles_per_gallon` and `msrp` columns were dropped.
2. **Feature Engineering**
   - Categorical variables (`brand` and `type`) were encoded using One-Hot Encoding.
   - Numerical columns were kept as they were.
3. **Feature Selection**
   - The target variable was `msrp`, while all other columns served as independent features.



## Model Development
- Used **Linear Regression** from `sklearn.linear_model`.
- The dataset was split into **training (80%) and testing (20%) sets**.
- Model was trained using `LinearRegression().fit(X_train, y_train)`.



## Performance Metrics
The model's performance was evaluated using:
- **Mean Squared Error (MSE)**
- **Root Mean Squared Error (RMSE)**
- **Mean Absolute Error (MAE)**



| Metric      | Training Set | Testing Set |
|------------|-------------|-------------|
| MSE        | 1.24e+09    | 8.77e+08    |
| RMSE       | 35,249      | 29,617      |
| MAE        | 16,485      | 16,686      |



## Results & Insights
- The model shows a reasonable performance but still has room for improvement.
- Features such as car brand and type significantly influence the MSRP.
- Further improvements could involve:
  - Feature scaling and normalization.
  - Adding polynomial features to capture non-linearity.
  - Exploring other regression models (e.g., Lasso, Ridge, Decision Trees).



## How to Run the Project
1. Clone the repository:
   ```bash
   git clone https://github.com/Omkar-Gadade/car-regression.git
   cd car-regression
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Convert the Jupyter Notebook then run the Python script to train the model:
   ```bash
   jupyter nbconvert --to script Car_Regression.ipynb
   ```
   ```bash
   python Car_Regression.py
   ```



## Dependencies
- Python 3.7+
- Pandas
- NumPy
- Scikit-Learn
- Matplotlib
- Seaborn


## Acknowledgments
This project is inspired by real-world car pricing datasets and machine learning techniques for predictive modeling.


## License
This project is licensed under the MIT License - see the LICENSE file for details.







