# Product-Delivery-Date-Prediction-System

This project focused on how to apply Machine Learning to build a model that can accurately predict delivery dates for items sold by a retailer using a dataset with details of shipping information. For our analysis, we decided to train and implement multiple machine learning models, consisting of Linear Regression, Random Forest, Gradient Boosting Model (GBM), Support Vector Machine (SVM), and a final ensemble model. To score the model, we will be  looking at RMSE (Root-mean-square deviation).

# Data Source

The dataset is taken from eBay from the ml challenge to estimate the delivery time. The data is provided with all the shipment and delivery related details and requires us to estimate the delivery date for items purchased. Features available were -

Acceptance_scan_timestamp
Declared_handling_days
Shipment_method_id
Carrier_min_estimate
Carrier_max_estimate
Item_zip
Buyer_zip
Category_id
Package_size


# Data Pre-processing

<img width="1792" alt="Data Pre-processing" src="https://user-images.githubusercontent.com/78765097/159579361-6dec06ca-8fea-4674-a9fb-bcd34612d573.png">

# Data Transformation

1. The delivery date, payment date, and acceptance date columns were converted into a numerical format based on the month, year, and day. 
2. Columns with zip codes were converted to numeric values as well, but only the first five numbers of each zip code were used to avoid conflicts. 
3. All the columns were scaled using the minmaxscaler from Sklearn into a range from 0 to 1 to aid the model with its computational power.

# Feature Selection

<img width="1148" alt="Heatmap Feature Selection" src="https://user-images.githubusercontent.com/78765097/159579571-5fd749af-3c46-4133-8b1c-fd8d97d2eb0f.png">


# Model Comparison

<img width="1792" alt="Model Comparison" src="https://user-images.githubusercontent.com/78765097/159579495-bd1b7c15-833d-4af0-9059-f53823949a4a.png">
