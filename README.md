# Seoul Bike Sharing Demand

## Aim:- To predict the count of bike shared in the duration of every 1 hour.

**Deployment:-** [Click here](https://tirumaleshndeployments2022.herokuapp.com/)

<img src="https://github.com/tirumaleshn2458/project_notebooks/blob/243e4ce26a9b20ac19f792984cf569af606ca279/assets/Screenshot%202022-01-20%20at%205.28.38%20PM.png" width="500" height="250">

###Pipelines**
- Data Analysis 
- Data Validation and Testing
- Feature Engineering and Selection
- Model Training and Selection

**Data Analysis**
- Summarized the relationship between the categorical features and target feature.
- Summarized the relationship between the numerical features and target feature.
- Plotted pairplot for visualizing the relationship and trends between the features.
- Checked the correlation for numerical features.
- Created a function to get the features that are correlated in a certain threshold and above.
- Plotted outliers using boxplot.

**Data Validation and Testing**
- Performed one sample ttest for each numerical features.
- Two sample ttest for two independent numerical features.
- Paired t-test for 2 different samples from the same group(population).
- Chi-Square test for finding the association between 2 categorical features.

**Feature Engineering and Feature Selection**
- Performed label encoding to transform the categorical features into numerical features.
- Used ExtraTreeClassifier for to get feature importance.

**Model Training**
Trained data using various algorithms.
- Linear Regression
  - [Sklearn API](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LinearRegression.html)
  - [Concept](http://www.stat.yale.edu/Courses/1997-98/101/linreg.htm#:~:text=Linear%20regression%20attempts%20to%20model,linear%20equation%20to%20observed%20data.&text=A%20linear%20regression%20line%20has,Y%20is%20the%20dependent%20variable.)
- Random Forest Regressor
    - [Concept](https://gdcoder.com/random-forest-regressor-explained-in-depth/)
    - [Sklearn API](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestRegressor.html)
- Decision Tree Regressor
    - [Concept](https://www.saedsayad.com/decision_tree_reg.htm)
    - [Sklearn API](https://scikit-learn.org/stable/modules/generated/sklearn.tree.DecisionTreeRegressor.html#sklearn.tree.DecisionTreeRegressor)
- XGBoost Regressor
    - [Concept](https://docs.aws.amazon.com/sagemaker/latest/dg/xgboost-HowItWorks.html)
    - [Xgboost API](https://xgboost.readthedocs.io/en/stable/python/python_api.html#xgboost.XGBRFRegressor.apply)  
- Neural Networks
  - [Concept](https://www.tutorialspoint.com/artificial_neural_network/artificial_neural_network_basic_concepts.htm)
  - [Sklearn API](https://scikit-learn.org/stable/modules/generated/sklearn.neural_network.MLPRegressor.html)
