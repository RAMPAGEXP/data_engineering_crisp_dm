# CRISP-DM Example

This project follows the CRISP-DM (CRoss Industry Standard Process for Data Mining) and breaks down each of it's processes with the respect to the project

These are the stated processes in the methodoly:

- Business Understanding
- Data Understanding
- Data Preparation
- Modeling
- Evaluation
- Deployment

# Project Details

I have used a [dataset](https://raw.githubusercontent.com/RAMPAGEXP/data_engineering_crisp_dm/main/dataset/dataset.csv) that I have combined from multiple source like Wikipedia and Kaggle, I am trying to find strongly coupled attributes with respect to our output label. The focus of this project is to highlight how deployment would work in a Data Engineering project and optimization of models.

# Process Breakdown

- **Business Understanding**:
  Our clients are trying to make cars for a certain category and they want to see if entering a certain category with a certain model yields them profit or not, we will do this by correctly predicting the price for the hypothetical car. They are trying to assess if the car model idea will give good enough profit.

- **Data Understanding**:
  We scrape data for different car manufacturers and their models on the internet and we get prehistoric data on certain manufacturers that are our clients. The data would have features showing details on model and their sales and pricing.

- **Data Preparation**:
  Since we have scraped data from multiple sources their will be data anomalies like missing values and data inconsistencies, we will fix them using some sort of an imputer. We will also scale the data for more efficient results and categorize the nominal data.

- **Modeling**:
  We will use [RapidMiner](https://rapidminer.com/) to suggest us which algorithm would make the most sense to implement. There are few other methods to check which model would make sense but we would like to use RapidMiner as it's efficient and fast to test.

- **Evaluation**:
  Our metric for worthiness of the model would be the accuracy, RMSE (Root Mean Squared Error) as this is a regression problem. We will first try to find the optimal hyper-parameters for our model using [hyperopt](http://hyperopt.github.io/hyperopt/) to find the minimum amount of loss.

- **Deployment**:
  No matter how impressive your solution for a problem might be, if it cannot be deployed you have lost the battle. Integration is a key part of deployment. Then we will build an app which will take in inputs and predict the retail price for the model.
