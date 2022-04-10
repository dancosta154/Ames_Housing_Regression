![Screenshot](../main/graphics/ames_iowa.png)

# Ames, Iowa House Cost Predictions
## Regression Analysis

#### Project Status: [Completed]

## Project Obective
The purpose of this project is to analyze and predict house prices in Ames, Iowa using a dataset which incorporates housing data from 2006 - 2010.

## Project Description
I was hired by a Construction Firm based in Ames, Iowa, who is looking to invest in a new development. In order to feel confident in their potential future investment, they would first like to evaluate existing homes and their sale price, to be able to identify the types of house features that drive the cost of sale pricing in the area. As the Data Scientist hired for this contract, my intent is to analyze housing data for the years of 2006 - 2010, and build a predictive Linear Regression model to identify those features that correlate strongest with the sale price. In providing this scope of work, my intent is to reinforce their decision that including the features that I suggest, they will be able to build highly profitable homes.

This project uses the [`train.csv`](../datasets/train.csv) dataset to train the model; however, the final dataset, titled [`modeleight_log.csv`](../clean_data/modeleight_log.csv) can be found in the clean_data folder. Descriptions of the final dataset can found in the [`Data Dictionary`](../Data_Dictionary.md):

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

### Conclusion
By fitting Linear Regression, LASSO, and Ridge models against the housing datasets, I was able to identify a number of unique characteristics, aka features, that strongly correlated to sales price. The model that I chose to present to the Construction Firm utilized a Linear Regression model, aided with a log function to normalize the distribution of the Sales Price, which the model uses as its target. Utilizing the existing and/or engineered features, I was able to predict the sales price of a house within $29k.


Image Source: https://nycdatascience.com/blog/student-works/predicting-home-prices-in-ames-ia-using-regression-models/
