## Classification - Online Shoppers Purchasing Intention

The purpose of this project is to analyze the purchasing behavior patterns of e-commerce visitors and to increase the conversion rate to purchase.

**Tools**: Python, JupyterLab, Git

**Libraries**: Pandas, Numpy, Feature-engine, Scikit-learn, Imbalanced-learn

**Dataset**: Online Shoppers Purchasing Intention, UCI Machine Learning, 2018 [[source]](https://www.kaggle.com/datasets/imakash3011/online-shoppers-purchasing-intention-dataset)

**Summary**
* This dataset has 12330 observations and 18 variables with 10 numerical variables, 7 categorical variables and one target variable.
* All numerical variables have a right-skewed distribution and contain a lot of outliers. 
* Revenue is the target variable that labels a visitor's purchase decision either make a purchase (class 1) or not make a purchase (class 0). The current condition is only 15% of total visitors who make a purchase. 
* From exploratory data analysis, visitors with low exit and bounce rates and high page values, tend to make a purchase.
* Based on data characteristics, the selected algorithm to build a classification model is tree-based or ensemble. The classification model with the random forest algorithm is able to correctly predict 62% of visitors who make a purchase.
* The result shows that page values, a number of visited pages, are the biggest impact on visitors' purchase decisions. The conversion rate to purchase increases up to 60% by applying an actionable recommendation from insights that boost page values of visitors.


