# Employee Attrition

## Aim: To predict whether the employ should be attrited or retained.

**Dataset:-** https://www.kaggle.com/pavansubhasht/ibm-hr-analytics-attrition-dataset

*Note:-* Both Feature Engineering and Feature Selection are included in Feature Engineering file itself.
#### Features overview:

- Age: Age of the employee(Integer type)
- Atrrition: Whether the employee is fired or not
- Business Travel: How often does the employee travel on business basis
- Daily rate: The amount payed to the employee daily i.e (Monthly Rate X 12) / Total working days in a year
- Department: Type of department the employee is working
- DistanceFromHome: The total distance from the employee's stay
- Education: Educational background
- EmployeeCount: Count of employee
- EmployeeNumber: Employee's unique number
- EnvironmentSatisfaction: Rate of environment satisfaction
- Gender: Gender of the employee
- HourlyRate: How much does the employee is payed on hourly based
- JobInvolvement: How well the employee is dedicated towards their job
- JobLevel: Level of the job
- JobRole: Role of the job
- JobSatisfaction: Employee's rating for his job satisfaction
- MartialStatus: Is employee married or not
- MonthlyIncome: Employee's fixed income per month
- MonthlyRate: Employee's total daily rate in a month
- NumCompaniesWorked: Number of companies does the employee worked in
- Over18: Is the employee is above 18 or not
- OverTime: Does the employee works overtime or not
- PercentSalaryHike: Increase in employee's salary in percentage
- PerformanceRating: Rating given for employee's overall performance
- RelationshipSatisfaction: How well the employee's relationship within organization/company
- StandardHours: A standard hour is the amount of work achievable, at the expected level of efficiency, in an hour
- StockOptionLevel: Level and the period of time granted to the employee to buy stocks 
- TotalWorkingYears: Number of years worked in their profession
- TrainingTimesLastYear: Number of times does the employee got trained in last year
- WorkLifeBalance: How well the employee balances their life
- YearsAtCompany: Number of years worked in the company
- YearsInCurrentRole: How many does the employee worked in a particular role
- YearsSinceLastPromotion: How many years are completed sinse their last promotion
- YearsWithCurrManager: How many does the employee worked under thier current manager

## Pipelines
- Data Analysis
- Feature Engineering
- Feature Selection
- Model training

**Data Analysis**
- The features in dataset are with combination of numerical and categorical type.
- Plotted distplot for numerical features.
- Plotted countplot for categorical features to find the relationship between the target feature and the categorical features.
- Checked out the correlation between numerical features in the dataset and plotted heatmap to check with visualization.
- *Libraries used:*
  - [Pandas](https://pandas.pydata.org/docs/) for data manupulation.
  - [Numpy](https://numpy.org/doc/) for mathematical computation
  - [Seaborn](https://seaborn.pydata.org/) for visualization
  - [matplotlib](https://matplotlib.org/) for plotting the figures

**Feature Engineering**
- Since, the dataset is imbalanced. I performed random sampling to make it balanced.
- Converting the categorical features into numerical features using label encoding. 
- Transformed the values of 'MonthlyIncome' into log values feature to remove outliers.
- Scaled the values using MinMaxScaler to get the better for the ML model.

**Feature Selection**
- Checked the value of the features using SelectKBest and ExtraTreeClassifier model.
- Finally, selected the features using SelectKBest model whose score is greater than or equal to 1.
- ExtraTreeClassifier
  - [Concept](https://www.geeksforgeeks.org/ml-extra-tree-classifier-for-feature-selection/)
  - [Sklearn API](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.ExtraTreesClassifier.html)
- SelectKBest
  - [Sklearn API](https://scikit-learn.org/stable/modules/generated/sklearn.feature_selection.SelectKBest.html)

**Model training**
- Trained the data with various algorithms
- LogisticRegression 
  - [Concept](https://searchbusinessanalytics.techtarget.com/definition/logistic-regression#:~:text=Logistic%20regression%20is%20a%20statistical,observations%20of%20a%20data%20set.&text=A%20logistic%20regression%20model%20predicts,or%20more%20existing%20independent%20variables.)
  - [Sklearn API](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LogisticRegression.html)
- RandomForestClassifier
  - [Concept](https://www.analyticsvidhya.com/blog/2021/06/understanding-random-forest/)
  - [Sklearn API](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestClassifier.html)
- DecisionTreeClassifier
  - [Concept](https://www.saedsayad.com/decision_tree.htm#:~:text=Decision%20Tree%20%2D%20Classification,decision%20tree%20is%20incrementally%20developed.&text=Decision%20trees%20can%20handle%20both%20categorical%20and%20numerical%20data)
  - [Sklearn API](https://scikit-learn.org/stable/modules/generated/sklearn.tree.DecisionTreeClassifier.html)
- XGBClassifier
  - [Concept](https://www.linkedin.com/pulse/xgboost-classifier-algorithm-machine-learning-kavya-kumar)
  - [XGBoost API](https://xgboost.readthedocs.io/en/stable/python/python_api.html)
- GradientBoostingClassifier
  - [Concept](https://www.displayr.com/gradient-boosting-the-coolest-kid-on-the-machine-learning-block/#:~:text=Gradient%20boosting%20is%20a%20type,minimizes%20the%20overall%20prediction%20error.&text=reduce%20the%20error.-,If%20a%20small%20change%20in%20the%20prediction%20for%20a%20case,of%20the%20case%20is%20zero.)
  - [Sklearn API](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.GradientBoostingClassifier.html)
- KNeighborsClassifier
  - [Concept](https://learn.g2.com/k-nearest-neighbor)
  - [Sklearn API](https://scikit-learn.org/stable/modules/generated/sklearn.neighbors.KNeighborsClassifier.html)

- Measured the accuracy using r2_score which returns the coefficient of determination of the prediction.
- Presented the reports using classification_report from sklearn.
  [Classification Report](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.classification_report.html)
