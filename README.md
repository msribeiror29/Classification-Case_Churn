# Classification Model - Churn

The context of the problem involves a fictitious company experiencing high churn rates, meaning many customers are abandoning its products or services. This situation directly impacts the company's revenue.

The objective of this project is to build a predictive model to identify customers with a high probability of churn, following the CRISP-DM methodology. By doing so, the company can take preventive actions, such as offering special deals, to retain these customers.

The data provided contains anonymous information about thousands of the company's customers, including whether each one remained a customer or abandoned the service (churn = 1).
The available variables for each client are:

Target:

  Churn — Customer churned or not

Numeric variables:

  Tenure — Number of months the client has been on base
  MonthlyCharges — The amount consumed per customer monthly
  TotalCharges — The amount consumed per total customer

Categorical variables:

	CustomerID - client id
	Gender — M/F
	SeniorCitizen — Whether or not the citizen is elderly (0.1)
	Partner — Whether or not the client is married
	Dependents — Client has dependents (Yes, No)
	PhoneService — Customer has telephone service (Yes, No)
	MulitpleLines — Whether the customer has multiple lines or not (Yes, No, No Phone Service)
	InternetService — Type of internet service (DSL, Fiber Optic, None)
	OnlineSecurity — If the customer has online security (Yes, No, No Internet Service)
	OnlineBackup — If the customer has Online Backup (Yes, No, No Internet Service)
	DeviceProtection — Whether the customer has device protection (Yes, No, No Internet Service)
	TechSupport — If the customer has technological support (Yes, No, No Internet Service)
	StreamingTV — If the customer has streaming TV (Yes, No, No Internet Service)
	StreamingMovies — If the customer has a movie streaming service (Yes, No, No Internet Service)
	Contract — Customer contract term (Monthly, 1-Year, 2-Year)
	PaperlessBilling — Whether or not the customer has a paperless bill (Yes, No)
	PaymentMethod — Customer Payment Method(E-Check, Mailed Check, Bank Transfer (Auto), Credit Card (Auto))

This data will allow us to explore the patterns that differentiate customers with a high probability of churn.
In this step, we will clean the data and prepare it for applying the models. Some necessary transformations and normalizations include:

  1. Treatment of missing values.
  2. Conversion of the categorical variables.
  3. Normalization of numerical variables.
  4. Division between training and testing.

	
At this stage, we will experiment with different classification algorithms to predict the likelihood of each customer abandoning the company.

The main models tested will be:

Two models are tested: Logistic Regression and Random Forest.

#Logistic Regression.

Logistic Regression is a simple but effective algorithm for classification.
The model is trained and prediction is made on the test set. Next, some performance metrics are calculated:


	Accuracy (training):0.80
	Accuracy(Test): 0.79

As the training and testing accuracies are very close, there is no evidence of overfitting.

#RandomForest.

Random Forest typically performs better than Logistic Regression.
Again, the model is trained, the prediction is made on the test set and the metrics are calculated:

	Accuracy (training):0.99
	Accuracy(Test): 0.78

Significant overfitting is noticed, with a large difference between training and test performance.
To improve, hyperparameter optimization is carried out with Grid Search.

With the optimized model, we have:

	Accuracy (training):0.83
	Accuracy(Test): 0.79

The difference between training and testing is much smaller, indicating that overfitting was controlled with hyperparameter optimization.
