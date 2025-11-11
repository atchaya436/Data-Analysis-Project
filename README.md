# DATA ANALYSIS ON HOUSING PRICING DATA SET
## House Sales in King County, USA

### Project Objectives
The main goals of this project are:
* Perform data wrangling to handle missing and irrelevant data.
* Conduct exploratory data analysis (EDA) to understand feature relationships.
* Develop predictive models using Linear Regression and Ridge Regression.
* Evaluate and refine model performance using R² and other metrics.
* Visualize trends and correlations using Matplotlib and Seaborn.
  
### About the Dataset
  The dataset contains real-world housing sale records from May 2014 to May 2015. Each record represents a house sold in King County, along with multiple descriptive attributes.
Key columns include:

  * price: The target variable representing the sale price.
  * bedrooms, bathrooms, floors: Indicators of house size and layout.
  * sqft_living, sqft_lot: The interior and land area.
  * waterfront, view, condition, grade: Quality and environmental features.
  * yr_built, yr_renovated: Historical data on construction and improvements.
  * lat, long, zipcode: Geographical information for location-based analysis.
  This dataset provides an ideal foundation for practicing data cleaning, visualization, and regression-based prediction.

### Tools and Technologies Used
* Python: Main programming language.
* Pandas & NumPy: For data cleaning, analysis, and manipulation.
* Matplotlib & Seaborn: For data visualization.
* Scikit-learn: For regression modeling and evaluation.
* Jupyter Notebook: To integrate code, visualizations, and documentation.

### Process and Workflow
1. **Importing and Exploring Data**
    The dataset is first loaded into a Pandas DataFrame and explored using functions like head() and dtypes() to inspect its structure and identify data types. A statistical summary using describe() helps in understanding numerical feature distributions.

2. **Data Wrangling**
    Unnecessary columns such as "id" and "Unnamed: 0" are removed using drop(). Missing values in bedrooms and bathrooms are replaced with their respective column means. These steps ensure the dataset is clean and consistent for further analysis.

3. **Exploratory Data Analysis (EDA)**
    EDA is performed to uncover relationships between variables:
      Value counts of floors are computed to see distribution.
      Boxplots compare housing prices with and without waterfront views to detect outliers.
      Regplots visualize correlations between features like sqft_above and price.
      The correlation matrix identifies which numerical features are most related to house prices.

4. **Model Development**
    Several regression models are created to predict house prices:
      A simple linear regression is built using a single feature (sqft_living).
      A multiple linear regression includes several predictors such as bedrooms, bathrooms, and grade.
      The R² score is calculated to evaluate how well each model explains price variation.

5. **Model Evaluation and Refinement**
    Data is split into training and testing sets using train_test_split().
    A Ridge Regression model is trained with regularization (alpha=0.1) to prevent overfitting.
    Next, PolynomialFeatures (degree 2) are applied to capture non-linear relationships, and the model’s R² is recalculated for comparison.

### Results and Insight
  Features like sqft_living, grade, and bathrooms have the highest impact on price. Houses with waterfront views and higher grades show significantly higher prices.The Ridge Regression model with polynomial transformation achieves improved predictive performance, balancing bias and variance effectively.
