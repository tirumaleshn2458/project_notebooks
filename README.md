# Store Sales Prediction in Big Mart

## Dataset link:- https://www.kaggle.com/brijbhushannanda1979/bigmart-sales-data

## Aim: ML model to predict the sales of the different stores of Big Mart according to the provided dataset.

## Description: 
Nowadays, shopping malls and Big Marts keep track of individual item sales data in
order to forecast future client demand and adjust inventory management. In a data
warehouse, these data stores hold a significant amount of consumer information and
particular item details. By mining the data store from the data warehouse, more
anomalies and common patterns can be discovered.


### Features overview:
- Item_Identifier: Unique product ID
- Item_Weight: Weight of product
- Item_Fat_Content: Whether the product is low fat or not
- Item_Visibility: The % of total display area of all products in a store allocated to the particular product
- Item_Type: The category to which the product belongs
- Item_MRP: Maximum Retail Price (list price) of the product
- Outlet_Identifier: Unique store ID
- Outlet_Establishment_Year: The year in which store was established
- Outlet_Size: The size of the store in terms of ground area covered
- Outlet_Location_Type: The type of city in which the store is located
- Outlet_Type: Whether the outlet is just a grocery store or some sort of supermarket
- Item_Outlet_Sales: Sales of the product in the particulat store. This is the outcome variable to be predicted.

*Note:-* Each and every is executed in jupyter notebook(.ipynb) files.

## Pipelines
- Data Analysis
- Feature Engineering
- Feature Selection
- Model Training

**Data Analysis**
- Read the downloaded dataset from kaggle.
- Plotted boxplot to check the outliers.
- Plotted distplot to check the distribution of continuos features.
- Performed line plot to check how trends are fluctuating between each category.
- Plotted jointplot using seaborn to see the relationship between numerical and categorical features.

- *Libraries used:*
  - [Pandas](https://pandas.pydata.org/docs/) for data manupulation.
  - [Numpy](https://numpy.org/doc/) for mathematical computation
  - [Seaborn](https://seaborn.pydata.org/) for visualization
  - [matplotlib](https://matplotlib.org/) for plotting the figures

**Feature Selection**
- Used SelectFromModel with Lasso from sklearn library to select the features based on alpha value.
  - SelectFromModel
    - [Sklearn API](https://scikit-learn.org/stable/modules/generated/sklearn.feature_selection.SelectFromModel.html)
  - Lasso
    - [Concept](https://www.mygreatlearning.com/blog/understanding-of-lasso-regression/)
    - [Sklearn API](https://scikit-learn.org/0.15/modules/generated/sklearn.linear_model.Lasso.html)

**Model Training**
- Splitted the data into train(70%) and test data(30%).
- Model trained:
  - Random Forest Regressor
    - [Concept](https://gdcoder.com/random-forest-regressor-explained-in-depth/)
    - [Sklearn API](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestRegressor.html)
