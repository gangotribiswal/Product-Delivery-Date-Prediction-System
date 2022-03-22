# Product-Delivery-Date-Prediction-System

This project focused on how to apply Machine Learning to build a model that can accurately predict delivery dates for items sold by a retailer using a dataset with details of shipping information. For our analysis, we decided to train and implement multiple machine learning models, consisting of Linear Regression, Random Forest, Gradient Boosting Model (GBM), Support Vector Machine (SVM), and a final ensemble model. To score the model, we will be  looking at RMSE (Root-mean-square deviation).

# Data Source

The dataset is taken from eBay from the ml challenge to estimate the delivery time. The data is provided with all the shipment and delivery related details and requires us to estimate the delivery date for items purchased. Features available were -

Acceptance_scan_timestamp, Declared_handling_days, Shipment_method_id, Carrier_min_estimate, Carrier_max_estimate, Item_zip, Buyer_zip, Category_id, Package_size


# Data Pre-processing

<img width="1792" alt="Data Pre-processing" src="https://user-images.githubusercontent.com/78765097/159579361-6dec06ca-8fea-4674-a9fb-bcd34612d573.png">

# Data Transformation

1. The delivery date, payment date, and acceptance date columns were converted into a numerical format based on the month, year, and day. 
2. Columns with zip codes were converted to numeric values as well, but only the first five numbers of each zip code were used to avoid conflicts. 
3. All the columns were scaled using the minmaxscaler from Sklearn into a range from 0 to 1 to aid the model with its computational power.

# Feature Selection

<img width="1148" alt="Heatmap Feature Selection" src="https://user-images.githubusercontent.com/78765097/159579571-5fd749af-3c46-4133-8b1c-fd8d97d2eb0f.png">


# Model Comparison

As a regression problem, evaluation was done based on the Root mean squared error, mean absolute error, R2_score, and mean sum of squared error. Different models were implemented to figure out which model will be better suited to predict delivery date more accurately.

Based on the comparison among all the models, the ensemble method on random forest regression, gradient boost regression, and CatBoost regression outperforms all the others. 

<img width="845" alt="Before HT" src="https://user-images.githubusercontent.com/78765097/159580659-e3d0b838-6da7-4a27-8557-5fc118d72e1e.png">



# After Hyperparameter tuning

For the three models mentioned above, hyperparameter tuning was done to find the best parameter for higher accuracy. Used RandomizedSearchCV, GridSearchCV to fine-tune the models’ hyperparameters.

<img width="585" alt="After HT" src="https://user-images.githubusercontent.com/78765097/159580682-777302a6-203d-4467-a518-8b2effdd4cb2.png">


After the hyper tuning step, Random Forest gave about 20% more r2_score than it did before hyper tuning with 2.54 MSE, 1.59 RMSE, and 0.97 MAE scores. Since the r2_score didn't change drastically, the ensemble approach was used to get majority votes from these selected models. R2_score 0.74 with MSE 2.53 was obtained using ensemble regression, which was about 0.1% better than random forest regressor.



