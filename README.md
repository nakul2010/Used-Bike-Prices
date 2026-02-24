Used Bike Price Prediction
Project Overview :-

The used vehicle market often has inconsistent pricing. Two bikes with similar specifications can have very different resale values depending on condition, brand perception, engine performance, and age.

In this project, I built a machine learning model to predict the resale price of used bikes using technical specifications and historical data. The project covers the complete workflow — from raw data cleaning to feature engineering, exploratory data analysis, model building, and performance evaluation.

The final model achieved strong predictive performance and provided meaningful insights into what truly drives resale value.

Dataset :-

The dataset used in this project contains 7,857 records of used bikes listed for sale.

You can find the dataset here:


Final Project Report of Used Bi…

Features Included

Model Name

Manufacturing Year

Kilometres Driven

Owner Type

Location

Mileage (kmpl)

Power (BHP)

Engine Capacity (CC – extracted)

Brand (extracted)

Price (Target Variable)

The price is measured in Indian Rupees.

Data Cleaning & Preprocessing :-

The raw dataset required significant preprocessing before modeling.

Some of the major steps included:

Cleaning text-based numeric fields like:

"35 kmpl" → 35

"19 bhp" → 19

"17000 Km" → 17000

Extracting engine capacity (cc) from model names using pattern matching.

Creating a new feature:

bike_age = current_year - model_year

Standardizing inconsistent brand names (e.g., Yamaha/yamaha).

Handling missing values using:

Brand-wise median imputation

Manual corrections where required

Converting power values from different units (PS, kW, HP) into BHP.

Removing extreme outliers (e.g., bikes older than 40 years).

Encoding categorical variables using one-hot encoding.

After preprocessing, the final dataset contained 7,845 clean records ready for modeling.

Exploratory Data Analysis (EDA)

EDA helped identify the strongest drivers of resale price.

Key Observations :-

Engine power has the strongest positive correlation with price.

Engine capacity (cc) also significantly increases resale value.

Bike age shows a clear negative correlation (depreciation effect).

Kilometres driven has less impact compared to engine performance.

Brand matters, but technical specifications matter more.

Visualizations Created

Correlation Heatmap

Price vs Bike Age (Depreciation Curve)

Feature Importance Plot

Actual vs Predicted Price Scatter Plot

These visuals helped validate modeling decisions and supported business interpretation.

Model Development :-

Three regression models were implemented and compared.

1. Linear Regression :-

R² ≈ 0.67

MAE ≈ 29,000

2. Ridge Regression :-

R² ≈ 0.66

Similar performance to Linear Regression

3. Random Forest Regressor (Final Model) :-

R² ≈ 0.72

MAE ≈ 19,400

The Random Forest model performed better, indicating that the relationship between bike specifications and price is non-linear.

Model Evaluation :-

The final Random Forest model:

Captured depreciation trends effectively

Handled non-linear relationships between engine specs and price

Produced balanced prediction accuracy across different bike segments

The Actual vs Predicted plot shows predictions closely following the ideal diagonal line, indicating strong model fit.

Key Business Insights :-

Engine power is the strongest driver of resale value.

Higher engine capacity significantly increases price.

Age impacts resale more than kilometres driven.

Fuel efficiency has limited influence compared to performance metrics.

Brand name plays a smaller role than technical specifications.

These insights suggest that performance-related features dominate pricing decisions in the used bike market.

Folder Structure :-

This project folder includes:

Jupyter Notebook (Complete EDA + Modeling)

Dataset (CSV file)

Final Project Report (PDF & DOCX)

Supporting visualizations

Feature engineering implementation

Future Improvements :-

Hyperparameter tuning using GridSearchCV

Trying Gradient Boosting / XGBoost

Log transformation for price to reduce skewness

Deployment as a pricing estimator API

Adding external market demand indicators

Conclusion :-

This project demonstrates an end-to-end machine learning pipeline for price prediction.

From raw, messy real-world data to a production-ready regression model, the workflow highlights strong skills in:

Data cleaning

Feature engineering

Statistical analysis

Regression modeling

Model evaluation

Business interpretation

The final Random Forest model achieved an R² of approximately 0.72, showing strong predictive capability for a real-world resale dataset.
