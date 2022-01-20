# Water Quality Prediction
## Aim:- To predict whether the water is potable or not.
**Dataset:-** [Here](https://raw.githubusercontent.com/amankharwal/Website-data/master/water_potability.csv)

**Deployment:-** [Here](https://tirumaleshndeployments2022.herokuapp.com/)

<img src="https://github.com/tirumaleshn2458/project_notebooks/blob/water_quality_prediction/assets/Screenshot%202022-01-20%20at%208.25.21%20PM.png" width="500" height="250">

**Features overview:-**
- *ph-* ph value that determines the acidity and basicity.
- *Hardness-* The value of hardness in the water.
- *Solids-* The amount of solids in water.
- *Chloramines-* The amount chloramines used as disinfectants to treat drinking water.
- *Sulfate-* The concentration value of Sulfate.
- *Conductivity-* This is directly linked to total dissolved solids (TDS).
- *Organic carbon-* This is the measure of the amount of organic compounds contained in a water sample.
- *Trihalomethanes-* The group of disinfection byproducts that form when chlorine compounds that are used to disinfect water react with other naturally occurring chemicals in the water.
- *Turbidity-* Level of Turbidity in water.
- *Potability-* Is the water safe to drink or not.

### Pipelines
**Data Analysis**
- Checked out the null values and plotted the null values in the dataframe using heatmap.
- Created a function to find the relationship between null valued features and target feature.
- Plotted pairplot to check the relationship between features in the dataframe.
- Plotted the displot to check the distribution of continuos features.
- Plotted boxplots to see the outliers in continuos features.
- *Libraries used:*
  - [Pandas](https://pandas.pydata.org/docs/) for data manupulation.
  - [Numpy](https://numpy.org/doc/) for mathematical computation
  - [Seaborn](https://seaborn.pydata.org/) for visualization
  - [matplotlib](https://matplotlib.org/) for plotting the figures

**Feature Engineering**
- Handled null values by imputating a function to replace them with median value of that particular feature.
- Scaled the values using MinMaxScaler to get the best fit of the model.

**Feature Selection**
- Used LogisticRegression with RFE(Recursive Feature Elimination) to get the rank importances using ranks.
- Used ExtraTreesClassifier to get the feature importance values.

**Model Training and Evaluation**
Trained the data using Various Algorithms and tuned them to get the best fit.
- LogisticRegression 
  - [Concept](https://searchbusinessanalytics.techtarget.com/definition/logistic-regression#:~:text=Logistic%20regression%20is%20a%20statistical,observations%20of%20a%20data%20set.&text=A%20logistic%20regression%20model%20predicts,or%20more%20existing%20independent%20variables.)
  - [Sklearn API](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LogisticRegression.html)
- KNeighborsClassifier
  - [Concept](https://learn.g2.com/k-nearest-neighbor)
  - [Sklearn API](https://scikit-learn.org/stable/modules/generated/sklearn.neighbors.KNeighborsClassifier.html)
- Naive Bayes Classifier
  - [Concept](https://www.kdnuggets.com/2020/06/naive-bayes-algorithm-everything.html)
  - [Sklearn API](https://scikit-learn.org/stable/modules/naive_bayes.html)
- DecisionTreeClassifier
  - [Concept](https://www.saedsayad.com/decision_tree.htm#:~:text=Decision%20Tree%20%2D%20Classification,decision%20tree%20is%20incrementally%20developed.&text=Decision%20trees%20can%20handle%20both%20categorical%20and%20numerical%20data)
  - [Sklearn API](https://scikit-learn.org/stable/modules/generated/sklearn.tree.DecisionTreeClassifier.html)
- RandomForestClassifier
  - [Concept](https://www.analyticsvidhya.com/blog/2021/06/understanding-random-forest/)
  - [Sklearn API](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestClassifier.html)
- Support Vector Machines-Support Vector Classifier
  [Concept](https://www.analyticsvidhya.com/blog/2017/09/understaing-support-vector-machine-example-code/)
  [Sklearn API](https://scikit-learn.org/stable/modules/generated/sklearn.svm.SVC.html)
    
