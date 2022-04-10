![Screenshot](../main/graphics/ames_iowa.png)


## Regression Modeling: Predicting House Prices in Ames, Iowa


### Project Obective
The purpose of this project is to analyze and predict house prices in Ames, Iowa using a dataset which incorporates housing data from 2006 - 2010.

### Project Description
The objective for this analysis is to identify which housing features have the most impact on the sales price of a house, then build a model to predict said price. The modeling featured will include Ordinary Least Squares (OLS) Linear Regression models, Ridge, and Lasso.

The success metric that will be used for this problem is the root mean squared error (RMSE).

This project uses the [`train.csv`](../main/datasets/train.csv) dataset to train the model; however, the final dataset, which was generated from the [top performing model](../main/model_submissions/09_Model_leaderboard.ipynb), titled [`model_nine_leaderboard.csv`](../main/clean_data/model_nine_leaderboard.csv), can be found in the `clean_data` folder. Descriptions of the final dataset can found in the [`Data Dictionary`](../main/Data_Dictionary.md):

### File Structure

```
project
│   Data_Dictionary.md
│   README.md
│
│
└──clean_data
│     Contains CSV outputs from each model
│         
│   
└──datasets
│     test.csv
│     train.csv
│  
│
└──graphics
│     Contains visualizations generated in modeling
│      
│   
│   
└──kaggle_submissions
│     Contains CSV's that were submitted to Kaggle
│     
│          
└──model_submissions
      Contains 10 different Linear Regression models.
      Differing approaches are within each notebook,
      to include Ridge, Lasso, and Polynomial methods.        
```

### Brief Analysis

In order to predict an array of sales prices within this dataset, differing methods and models were applied. To evaluate these approaches, it is important to have a benchmark, or baseline, to compare against. In this case, we can use the Root Mean Squared Error (RMSE) of the Sale Price as the baseline model for evaluation purposes. Using the RMSE, which indicates how divergent the prediction is from the actuals, we will assign the baseline model a value of \$79,277.

As stated previously, differing methods were used to predict the sale price with the highest accuracy. To start, Ordinary Least Squares (OLS) Linear Regression models were fit to the data, with an increasing number of Feature Engineered columns, in the attempt of flushing out the strongest linear relationships from the dependent variables to the independent variable. This process lead to many important discoveries that became large contributors to the model, such as multiplying the Overall Quality field with the Year Remodeled/Added or computing the entire house' square footage, for just a couple of examples. After exploring these relationships manually, the next step was to fit [Sklearn's PolynomialFeatures](https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.PolynomialFeatures.html) model to the data, to generate many more relationships. Finally, both Ridge and Lasso models were fit; however, the most useful model did not utilize either of these methods.


### Conclusion

In evaluating the models, each proved to be substantially more useful than the aforementioned baseline model. The model which provided the most accurate results was fit using Linear Regression, leveraging many Feature Engineered columns, and was aided with a log function to normalize the distribution of the Sales Price column. The Root Mean Squared Error of the this model indicated that the errors were roughly \$27,194 off from the actual sale price.


#### Sources

Image Source: https://nycdatascience.com/blog/student-works/predicting-home-prices-in-ames-ia-using-regression-models/
