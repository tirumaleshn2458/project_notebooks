# Air Quality Index Prediction
## Aim:- To predict the quality of Air using PM2.5(Particulate Matter)

**Dataset:-**[Click here](https://raw.githubusercontent.com/krishnaik06/AQI-Project/master/Data/Real-Data/Real_Combine.csv)

**Pickle file used for deployment:-** [Click here](https://drive.google.com/file/d/1Sddf72th-qgvajzgTDAzLZE1KYQcv1yw/view?usp=sharing)

**Deployment:-** [Click here](https://tirumaleshndeployments2022.herokuapp.com/) to check the deployment in Machine Learning Section.

<img src="https://github.com/tirumaleshn2458/project_notebooks/blob/73637f77bfdc2bc38a7ec3bb6173d416dacf43d4/assets/Screenshot%202022-01-18%20at%2011.59.03%20PM.png" width="500" height="250">

*Note:-* The dataset is taken from another github repository and called as an API. 

**Files:-** Each and every is executed in jupyter notebook(.ipynb) files. 

**About Features**
- T - Temperature in Air

- TM - Maximum Temperature

- Tm - Minimum Temperature

- SLP - Atmospheric pressure at sea level (hPa)

- H - Average relative humidity (%)

- VV - Average visibility

- V - Average wind speed (Km/h)

- VM - Maximum sustained wind speed (Km/h)

- PM 2.5 - Particulate matter 2.5

## Pipelines
- Data Analysis
- Feature Selection
- Model Training
- Hyper-parameter tuning

**Data Analysis**
- Read the downloaded dataset from kaggle.
- Plotted boxplot to check the outliers.
- Plotted distplot to check the distribution of continuos features.
- Performed line plot to check how trends are fluctuating between each category.
- Plotted joinplot using seaborn to see the relationship between numerical and target feature.

- *Libraries used:*
  - [Pandas](https://pandas.pydata.org/docs/) for data manupulation.
  - [Numpy](https://numpy.org/doc/) for mathematical computation
  - [Seaborn](https://seaborn.pydata.org/) for visualization
  - [matplotlib](https://matplotlib.org/) for plotting the figures

**Feature Selection**
- Used SelectFromModel with Lasso model from sklearn to select the features.
  - SelectFromModel
    - [Sklearn API](https://scikit-learn.org/stable/modules/generated/sklearn.feature_selection.SelectFromModel.html)
  - Lasso
    - [Concept](https://www.statisticshowto.com/lasso-regression/#:~:text=Lasso%20regression%20is%20a%20type,i.e.%20models%20with%20fewer%20parameters).&text=The%20acronym%20%E2%80%9CLASSO%E2%80%9D%20stands%20for,Absolute%20Shrinkage%20and%20Selection%20Operator.)
    - [Sklearn API](https://scikit-learn.org/0.15/modules/generated/sklearn.linear_model.Lasso.html)
- Considered all input features since, the accuracy is more when the input features are limited.

**Model Training and Evaluation**
- Splitted the data into train(70%) and test data(30%).
- Model trained:
  - Linear Regression 
    - [Sklearn API](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LinearRegression.html)
    - [Concept](http://www.stat.yale.edu/Courses/1997-98/101/linreg.htm#:~:text=Linear%20regression%20attempts%20to%20model,linear%20equation%20to%20observed%20data.&text=A%20linear%20regression%20line%20has,Y%20is%20the%20dependent%20variable.)
  - Lasso Regression
    - [Concept](https://www.mygreatlearning.com/blog/understanding-of-lasso-regression/)
    - [Sklearn API](https://scikit-learn.org/0.15/modules/generated/sklearn.linear_model.Lasso.html)
  - Ridge Regression
    - [Concept](https://ncss-wpengine.netdna-ssl.com/wp-content/themes/ncss/pdf/Procedures/NCSS/Ridge_Regression.pdf)
    - [Sklearn API](https://scikit-learn.org/0.15/modules/generated/sklearn.linear_model.Ridge.html#sklearn.linear_model.Ridge)
  - Decision Tree Regressor
    - [Concept](https://www.saedsayad.com/decision_tree_reg.htm)
    - [Sklearn API](https://scikit-learn.org/stable/modules/generated/sklearn.tree.DecisionTreeRegressor.html#sklearn.tree.DecisionTreeRegressor)
  - K-Nearest Neighbors Regressor
    - [Concept](https://www.saedsayad.com/k_nearest_neighbors_reg.htm)
    - [Sklearn API](https://scikit-learn.org/stable/modules/generated/sklearn.neighbors.KNeighborsRegressor.html)
  - Random Forest Regressor
    - [Concept](https://gdcoder.com/random-forest-regressor-explained-in-depth/)
    - [Sklearn API](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestRegressor.html)
  - XGBoost Regressor
    - [Concept](https://docs.aws.amazon.com/sagemaker/latest/dg/xgboost-HowItWorks.html)
    - [Xgboost API](https://xgboost.readthedocs.io/en/stable/python/python_api.html#xgboost.XGBRFRegressor.apply)
  - ANN(Artificial Neural Network)
    - [Concept](https://www.tutorialspoint.com/artificial_neural_network/artificial_neural_network_basic_concepts.htm)
    - [Keras API](https://keras.io/api/models/sequential/)
- Hyperparameter tuning
  - Performed Random search cv for RandomForestRegressor, XGBoost Regressor 
    - [Concept for Random Search CV](https://www.section.io/engineering-education/random-search-hyperparameters/)
    - [Sklearn API](https://scikit-learn.org/stable/modules/generated/sklearn.model_selection.RandomizedSearchCV.html)
  - Performed Grid Search CV for Decision Tree Regressor
    - [Concept for Grid Search CV](https://elutins.medium.com/grid-searching-in-machine-learning-quick-explanation-and-python-implementation-550552200596#:~:text=Grid%2Dsearching%20is%20the%20process,parameters%20for%20a%20given%20model.&text=Grid%2DSearch%20will%20build%20a,a%20model%20for%20each%20combination.)
    - [Sklearn API](https://scikit-learn.org/stable/modules/generated/sklearn.model_selection.GridSearchCV.html)
  - Performed iteration of K combination for KNN Regressor.
- Evaluation metrics
   - Performed cross validation using sklearn.cross_val_score 
     - [Concept](https://machinelearningmastery.com/k-fold-cross-validation/#:~:text=Cross%2Dvalidation%20is%20a%20resampling,k%2Dfold%20cross%2Dvalidation.)
     - [Sklearn API](https://scikit-learn.org/stable/modules/generated/sklearn.model_selection.cross_val_score.html)
   - MAE(Mean Absolute Error)
     - [Concept](https://en.wikipedia.org/wiki/Mean_absolute_error)
     - [Sklearn API](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.mean_absolute_error.html)
   - MSE(Mean Squared Error)
     - [Concept](https://www.statisticshowto.com/probability-and-statistics/statistics-definitions/mean-squared-error/#:~:text=The%20mean%20squared%20error%20(MSE,errors%E2%80%9D)%20and%20squaring%20them.&text=It's%20called%20the%20mean%20squared,of%20a%20set%20of%20errors.)
     - [Sklearn API](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.mean_squared_error.html)
    - RMSE(Root Mean Squared Error)
      - [Concept](https://www.statisticshowto.com/probability-and-statistics/regression-analysis/rmse-root-mean-square-error/)
      - [Sklearn API for MSE](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.mean_squared_error.html)
- Model selection
  - Model is selected based on metrics
  - Selected Random Forest Regressor since, it has less error than other models.

