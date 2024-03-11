# project-4-life-expectancy

Team names:
- Lauren Pescarus
- Liana Hamacher
- Michael Krebs
- Mitchell Brian

Synopsis:
We are using data on life expectency provided from Data.gov as joined with county specific demographic data and the longitude and latitude details for each county to break down the models further. We hope to use this data to predict the life expectancy based on various details as shown in the data file. We will use a neural network machine and linear regression learning models to make our preditions and will further explore the data via Tableau to showcase the findings. Our presentations will be shared in a slide deck hosted on Google Slides.  

Hypothesis:
We believe the average life expectancy of individuals in the US will be impacted by the following factors:
- Income
- Education
- Comparison over time
- Population density
And we intend to demonstrate this using data, linear regression models, and a neural network machine learning algorithm.

Data Resources:
Three different data sources were found and used from several different resources:
SimpleMaps: US County latitude and longitude data (https://simplemaps.com/data/us-counties)
Census data: US Life Expectancy from birth by county (https://catalog.data.gov/dataset/u-s-life-expectancy-at-birth-by-state-and-census-tract-2010-2015)
Corgis Edu: County demographic data (https://corgis-edu.github.io/corgis/csv/county_demographics/)
Resulting in a combined data file with 65,459 rows and 57 columns!

Data Cleaning:
- Grabbing data: Loading 3 datasets in CSV format: US Life Expectancy, county geolocation, and county demographics using Pandas. 
- Merging and cleaning: The life expectancy and updated county columns were merged, then that combined dataset merged again with the state identifier. Rows with NaN were removed and life expectancy was split into high and low value columns.
- Transformation and prep: Column names are standardized with renaming, unneeded columns removed. Categorical columns are created based on racial and gender composition data. Pie charts are generated.
- Saving: Cleaned and transformed data is saved to a CSV.

Machine Learning Processes:
- Linear Regression
    - Tested four variables against Life Expectancy
        - Income
        - Education
        - Population levels in 2010
        - Population levels in 2020
Deep Learning Neural Network process:
- Imported libraries and data file to use 
- Cleaned and trimmed the data by dropping irrelevant columns
- Split the dataset into features (x) and target (y, life expectancy mean) sets with various combinations of features for different models
- Standardized the feature sets using ‘StandardScaler’
- Defined, compiled, and trained four different deep neural network models with varying input features using a simple architecture with two hidden layers.
- Evaluates each model on a test dataset to compute the mean squared error.

- Tableau visualization: https://public.tableau.com/app/profile/liana.hamacher/viz/LifeExpectancy_17101050462560/Dashboard1

Results:

Linear Regression:
Median household income has the most noticeable trend line, followed by education.
	2010 and 2020 population trend line is harder to notice

-Each variable test by linear regression showed different degrees of variance
-The R2 scores were quite low: 
> income = .16 (the regression explains 16% of the variation in our y-variable)
> education = .11 (the regression explains 11%% of the variation in our y-variable)
> 2010 and 2020 Populations = .02

Neural Network:
All models achieve similar MSE values after training, with the 4th model (including per capita income, population per square mile, bachelor’s degree or higher, and white percentage as features) performing slightly better than the others.

Suggests: The inclusion of these specific factors could have a slightly more significant impact on predicting life expectancy.

Summary: 
Our primary goal was to predict life expectancy using various factors. We used methods of Machine learning creating 4 neural network models and also focused on linear regression approach. 

The result indicates that Model 4 with the lowest lost statistic, can effectively utilize a broad range of factors to predict a life expectancy.
linear regression approach highlighted the percentage of  the population with a Bachelor's degree as having the most impact on life expectancy, suggesting that higher education level are strongly associated with longer life expectancy .This factore alone was shown to increase the mean life expectancy by 0.1176 years for each %1 increase in the population with higher education level. Impact of income on life expectancy is also positive but smaller.  Population 2010 and 2020 have positive 
 

Steps:
- Find data - Lauren
- Clean and join data - Lauren
- Send over the writeup of the project to the TAs - Lauren
- Create 1 prediction model - using neural network machine learning model - Mitchell, Michael
- Input the 3 predictions to see results - Mitchell, Michael
- Record prediction results - Liana
- Set up tableau visualizations - Liana
- Create slide deck to walk through process + results - All team, divide up slides

- Presentation: https://docs.google.com/presentation/d/1NaJ1nFheCKZyJWs8qn0Q78x6HNBJvasiSKRcSwz-8k4/edit#slide=id.g1f3aee39af7_0_150
