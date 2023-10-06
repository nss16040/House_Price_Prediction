# Bengaluru House Price Prediction

This is a Python project that aims to predict house prices in Bengaluru, India. It involves data preprocessing, feature engineering, and model building using machine learning techniques.

## Getting Started

1. **Importing Libraries and Loading Data**: We begin by importing necessary libraries and loading the dataset from a CSV file.

2. **Preprocessing**: Data preprocessing is performed, which includes handling missing values, cleaning data, and converting features like `total_sqft` into a numerical format.

3. **Feature Engineering**: We create new features, such as `bhk` (number of bedrooms/hall/kitchen) and `price_per_sqft`. We also handle outliers in the data.

4. **Model Building**: We split the data into training and testing sets, build a Linear Regression model, and evaluate its performance. The best model is selected using GridSearchCV.

5. **Saving the Model**: Once the best model is found, it is saved to a pickle file (`model.pkl`) for future use.

## Usage

You can use this model to predict house prices in Bengaluru. Here's an example of how to make predictions:

```python
from model import predict_price

# Example usage
location = '1st Phase JP Nagar'
sqft = 1500
bath = 2
bhk = 3

predicted_price = predict_price(location, sqft, bath, bhk)
print(f"The predicted price for a house in {location} with {bhk} BHK, {sqft} sqft area, and {bath} bathrooms is ₹{predicted_price:.2f} Lakhs.")
