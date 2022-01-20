# Real Estate Sales

## Aim:- **To Predict the Sale Amount of the house valued featured with certain values.**

**Dataset:-** https://catalog.data.gov/dataset/real-estate-sales-2001-2018

### Modified data files:- https://drive.google.com/drive/u/1/folders/1kU17gDX3RzGqgaigHfh2n37qR0F75qnC

## Deployed link:- To be deployed

**Features Overview**
- Serial Number:- Represents the recorded value index of that house.
- List Year:- Value of the year in which the house is listed in.
- Date Recorded:- Specific Date, the assest's property was recorded.
- Town:- Name of the town the house is located in.
- Address:- The Complete address of the house.
- Assessed Value:- The Estimated value which is assessed to the house.
- Sale Amout:- The value of amount at which the house was sold.
- Sales Ratio:- The Ratio between the assessed value and sale amount.
- Property Type:- Type of property to which it is suitable for.
- Residential Type:- Type of residency which suits for different category of who live in.
- Non Use Code:- The code which is used to represent a property.
- Assessor Remarks:- The remarks given by assessor who measures the value of house.
- OPM Remarks:- Remarks from the Office of Personnel Management.
- Location:- The geo-location values i.e x-axis, y-axis.


## Pipelines
- Data Analysis
- Feature Engineering
- Model Training

**Data Analysis**
- Identified the features which have more null values.
- Removed the features which have null values more than 25 percentage.
- Checked the correlation between the null valued features and target feature.
**Feature Engineering**
- Dropped the rows which have null values in the record.
- Transformed the categorical features into numerical features.
- Changed the year values in temporal features into normal integers by subtracting the year value with the current year.
**Model Training and Evaluation**
- Trained the data with different algorithms
- RandomForestRegressor
  - [Concept](https://gdcoder.com/random-forest-regressor-explained-in-depth/)
  - [Sklearn API](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestRegressor.html)
  - After fitting the model, evaluated it by checking the error rate using KFold cross validation model
    - [Concept](https://machinelearningmastery.com/k-fold-cross-validation/#:~:text=Cross%2Dvalidation%20is%20a%20resampling,is%20to%20be%20split%20into.)
    - [Sklearn API](https://scikit-learn.org/stable/modules/generated/sklearn.model_selection.KFold.html)
- Linear Regression 
    - [Sklearn API](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LinearRegression.html)
    - [Concept](http://www.stat.yale.edu/Courses/1997-98/101/linreg.htm#:~:text=Linear%20regression%20attempts%20to%20model,linear%20equation%20to%20observed%20data.&text=A%20linear%20regression%20line%20has,Y%20is%20the%20dependent%20variable.)
- Lasso Regression
    - [Concept](https://www.mygreatlearning.com/blog/understanding-of-lasso-regression/)
    - [Sklearn API](https://scikit-learn.org/0.15/modules/generated/sklearn.linear_model.Lasso.html)
- XGBoost Regressor
    - [Concept](https://docs.aws.amazon.com/sagemaker/latest/dg/xgboost-HowItWorks.html)
    - [Xgboost API](https://xgboost.readthedocs.io/en/stable/python/python_api.html#xgboost.XGBRFRegressor.apply)    


