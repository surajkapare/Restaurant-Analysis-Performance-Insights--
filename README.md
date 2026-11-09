# Restaurant Analysis & Performance | EDA (Python) + SQL + ML

End-to-end analysis of **9,551 restaurants across 141 cities and 15 countries**: data cleaning and exploratory analysis in Python, business questions answered in MySQL.

## Key findings
- **North Indian** is the most common cuisine (9.9% as an exact listing, 41.6% when multi-cuisine listings are split).
- **New Delhi** has the most restaurants (5,473, 57.3% of the dataset). Delhi NCR cities make up 83% of listings.
- The raw SQL answer for "highest average rating" is **Inner City (4.9)**, but it has only 2 restaurants. With 20+ restaurants, **London (4.54)** leads.
- **3-4** is the most common rating range (45.9%). 22.5% of restaurants are unrated (rating 0).
- Restaurants with table booking or online delivery have higher average ratings.

## Repository structure
```
restaurant-analysis-eda-sql/
|-- README.md
|-- data/
|   `-- cleaned_data.csv
|-- notebooks/
|   `-- Cognifyz_IT_Solutions.ipynb
|-- sql/
|   `-- SQL_business_answers.sql
`-- presentation/
    `-- Restaurant_Analysis_EDA_SQL_Carousel.pdf
```

## Tech stack
Python (Pandas, NumPy, Matplotlib, Seaborn), Jupyter Notebook, MySQL.

## How to run
1. Clone the repo and install: `pip install pandas numpy matplotlib seaborn jupyter`
2. Open `notebooks/Cognifyz_IT_Solutions.ipynb` and set the file path in the first `read_csv` cell to your copy of the raw dataset (or load `data/cleaned_data.csv` and skip the cleaning cells).
3. For SQL: import `data/cleaned_data.csv` into a MySQL table named `cleaned_data`, then run `sql/SQL_business_answers.sql`.

## Data cleaning summary
- Fixed encoding issues and standardised column names (snake_case)
- Filled missing `cuisines` values with the mode
- Checked duplicates (none found)
- Capped outliers in `average_cost_for_two` and `votes` using the IQR method (votes max = 320 because of this cap)
- Converted flag and rating columns to categorical types

## Limitations
Votes are capped, 22.5% of restaurants are unrated, the "review" analysis uses rating labels rather than real review text, chains are detected by name matching, and the data is about 90% India.
# 🍽️ Restaurant Rating Prediction Using Machine Learning

## 📌 Project Overview

The **Restaurant Rating Prediction System** is a Machine Learning project that analyzes restaurant data and predicts restaurant ratings based on various features such as average cost, price range, customer votes, table booking availability, online delivery, and country information.

The main objective of this project is to understand restaurant-related patterns, perform exploratory data analysis (EDA), and build regression models to predict restaurant ratings accurately.

## 🎯 Project Objectives

- Perform Exploratory Data Analysis (EDA) on restaurant data.
- Identify important factors affecting restaurant ratings.
- Analyze restaurant trends and customer preferences.
- Clean and preprocess the dataset.
- Apply categorical encoding techniques.
- Build and compare multiple Machine Learning regression algorithms.
- Identify the best-performing model for restaurant rating prediction.

## 📂 Project Workflow

1. Data Collection
2. Data Cleaning and Preprocessing
3. Exploratory Data Analysis (EDA)
4. Data Visualization
5. Feature Selection
6. Categorical Encoding
7. Train-Test Split
8. Machine Learning Model Training
9. Model Evaluation
10. Model Comparison

## 🛠️ Technologies & Tools Used

| Technology | Purpose |
|---|---|
| Python | Programming |
| Pandas | Data Manipulation |
| NumPy | Numerical Operations |
| Matplotlib | Data Visualization |
| Seaborn | Statistical Visualization |
| Scikit-learn | Machine Learning |
| Jupyter Notebook | Development Environment |
| GitHub | Project Management |

## 📊 Dataset Information

- Total Records: 9,551
- Original Features: 21
- Target Variable: `aggregate_rating`
- Problem Type: Regression

### Important Features

- `average_cost_for_two`
- `price_range`
- `votes`
- `has_table_booking`
- `has_online_delivery`
- `is_delivering_now`
- `country_code`

### Target Variable

**aggregate_rating:** Represents the overall restaurant rating and is used as the dependent variable for prediction.

## 🔍 Exploratory Data Analysis (EDA)

Performed different EDA techniques to understand the dataset:

- Univariate Analysis
- Bivariate Analysis
- Multivariate Analysis
- Distribution Analysis
- Correlation Analysis
- Outlier Detection
- Data Visualization

## ⚙️ Data Preprocessing

The following preprocessing techniques were applied:

- Handled missing values.
- Removed unnecessary columns.
- Converted categorical Yes/No values into numerical format.
- Applied One-Hot Encoding to categorical features where required.
- Separated independent and dependent variables.
- Split the dataset into training and testing sets.

## 🤖 Machine Learning Algorithms

The following regression algorithms were explored:

1. Linear Regression
2. Decision Tree Regressor
3. Random Forest Regressor
4. Gradient Boosting Regressor
5. XGBoost Regressor (if included in the final experiments)

## 📈 Model Evaluation & Results

The models were evaluated using the following metrics:

- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- R² Score

### Model Comparison

| Evaluation Metrics | Random Forest | Gradient Boosting |
|---|---:|---:|
| MAE | 0.2179 | **0.2164** |
| MSE | 0.1111 | **0.1097** |
| RMSE | 0.3336 | **0.3313** |
| R² Score | 95.12% | **95.18%** |

### 🏆 Best Performing Model: Gradient Boosting Regressor

Gradient Boosting achieved the best results among the two models evaluated so far, with an R² score of **95.18%**.

It also achieved a lower MAE and RMSE compared with Random Forest, indicating slightly better prediction performance.

## 💡 Key Insights

- Restaurant ratings can be analyzed using customer votes, pricing, and service-related features.
- Machine Learning regression algorithms can predict restaurant ratings based on available restaurant information.
- Gradient Boosting performed slightly better than Random Forest in the experiments conducted.
- Model evaluation metrics help identify the most suitable algorithm for rating prediction.


## 🔮 Future Enhancements

- Develop an interactive web application using Streamlit.
- Improve model performance through hyperparameter tuning.
- Apply advanced feature engineering techniques.
- Include cuisine and city information through appropriate encoding.
- Deploy the trained Machine Learning model.
- Provide real-time restaurant rating predictions.

## ⭐ Conclusion

This project demonstrates the complete Machine Learning workflow, from data preprocessing and exploratory data analysis to regression model development and evaluation.

The project helped develop practical experience in Python, data analysis, data visualization, feature engineering, and Machine Learning model building.

If you find this project useful, feel free to ⭐ the repository!

## 👨‍💻 Author

**Suraj Kapare**

Aspiring Data Analyst | Data Science & Machine Learning Enthusiast
