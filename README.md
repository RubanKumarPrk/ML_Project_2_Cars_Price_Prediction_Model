# ML_Project_2_Cars_Price_Prediction_Model

Cars Price Prediction Regression Model 
========================================

Table of Content :
========================================

Step 1 : Importing Libraries and Importing Data
=================================================
=================================================
		In this step we are importing libraries like pandas,matplotlib,seaborn to upload the cars_price.csv data to the workbook and tried to explore the data using pandas.

Step 2 : Data Cleaning
=========================
=========================
		In this step I done exploratory Data Analysis to check missing values,null values,symbols are other misleanous thing in data after that I tried to correct the row and also splitting the data to x and y to further the process.
	Handelling Outliers
	------------------------
		We can see that there are (205-88)= 117 records, which are outliers in the dataset.
	Checking Data Imbalance
	------------------------
		We can see that there is data imbalance in below columns:-

	symboling - There are very few with rating -2.
	fuletype - All the cars fule type is Gas, as Diesel cars were removed while removing outliers..
	aspiration - Lesser number of turbo than std.
	engineloaction - All the engine location is in front, as all the rear engine cars were removed while removing outliers.
	enginetype - Considerably more number of ohc than others.
	cylindernumber - Large number of four cyliners than others.
	fulesystem - mpfi and 2bbl fulesystem cars are more comparitavely others.
	CarCompany - Most of the Toyata company cars were surveyed.
	Visualising the data to check the possiblity of linear regression model
	------------------------------------------------------------------------
		We can see that there are few columns that have linear relationship with the target variable "price". So, we can build a linear regression model here.
	Visualising the categorical variables
	-------------------------------------
		CarCompany - Porsche has very high median price compared to other cars,though the number of Porsche cars is very less. Volvo, alfa-romero, audi and BMW are also high median price than others. Saab has wide rage of price, with high median price.
	aspiration - std has lower median than turbo.
	carbody - convertible has higher median that others.
	symboling - -2 and -1 have higher median price than others.
	enginelocation - rear has very high median price than fromt.
	cylindernumber - Four has lower median than others.
	fulesystem - 1bbl and 2bbl have lower median price than others.
Now atleast we know that what are the variables have impact on the price. So as which variables are important for the model building.

Step 3 : Preparing the data for model building
================================================
================================================

	Encoding
	---------
		Converting categorical variables (fueltype, aspiration, doornumber, drivewheel, enginelocation) with two levels to binary variables.
	Dummy variables
	---------------
		Converting other categorical variables with more than two levels to dummy variables. We have to create (n-1) dummy variables by removing the base status. n is the number of levels of the variables.

	Splitting Data into Train and test
	----------------------------------
		In this step we importing train_test_split library and then we are training the model x_train,x_test,y_train,y_test.


Step 4 : Data Processing
=========================
=========================

		In this step we first check the outliers in data because if we have outliers our end result will be affected to clear then and any inconsistency between the data I use MinMax Scaler method to standardised the data and then there is a drastic change in the data.

Step 5 : Model Creation
========================
========================

	After Standardizing the data I created a 9 Models like 
		Linear Regression
		Random Sample Consensus - RANSAC
		Ridge Regression
		Lasso Regression
		Elastic Net
		Polynomial Regression
		Stochastic Gradient Descent
		Random Forest Regressor
		Support Vector Machine
				
 	I created all this model on default and also with different parameters value which this libraries are have then out of all this model I select the best model which produces the best result out by checking their Score 
		MAE == Mean Absoulte Error
		MSE == Mean Square Value
		RMSE == Square Root of Mean Square Error
		R2 Square == R2 Score

Step 6 : Model Comparison
==========================
==========================

		To check which Model is best out of all 9 Model with all the scores we have calculated.
		Out of All the Model Random Forest Regressor is the Best Model.
