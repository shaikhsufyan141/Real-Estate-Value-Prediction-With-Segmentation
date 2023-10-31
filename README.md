# Real-Estate-Value-Prediction-With-Segmentation

### Suppose there is an investment fund planning to invest in properties at hundreds of locations. 🏠 Based on the previous millions of property sales over the past few years, the fund house wants to identify the property which can result in a higher gain on investment. 💰 They can not go by analyzing all the properties one by one. 🤔 So they want the segmentation of properties so that they can look into their target segments. 🎯 So this challenge is going to help them by easily identifying their target properties using advanced AI and Analytics. 🔍

### In the first week, you will receive a dataset of real estate properties with locality, estimated price, and selling price for the last 23 years. 📊 The task is to identify the input features in the dataset and use them to predict the sale price of a property. 🔮 After this modelling of input and output features, predict the sale price of all the properties in the test dataset. 💵 Once the sale prices for the test data are predicted, put these properties into 4 segments. 🔢 These segments can be formed according to the gain. 💹 The gain is calculated based on the estimated price and predicted sale price (Gain = (Sale price - Estimated price)/100).

## Input features


Year: The year in which the property was sold or valued.

Date: The date on which the property was sold or valued.

Locality: The name of the town where the property is located.

Address: The complete address of the property.

Estimated Value: The estimated market value of the property, which is based on factors such as its location, size, and condition.

Property: A categorical feature indicating the type of property. There are six different categories.
Condo
Single-Family
Three Family
Two Family
Four Family
Residential

Residential: A categorical feature which further explains the category in which a certain property falls. There are five different types of categories.
Condominium
Detached House
Triplex
Duplex
Fourplex

num_rooms: A numerical feature which defines the number of rooms (e.g. bedrooms, living rooms, etc.) in the property.

carpet_area: The carpet area of the property, refers to the area of the floor that could be used for the flooring.

property_tax_rate: The rate at which property taxes are assessed on the property, which may vary based on its location and year.

Sale Price: The actual price at which the property was sold, which may be higher or lower than the estimated value.


 ## Target Variable

Segment: It is a categorical feature which is encoded based on the forecast. There are four segments.

Segment 0 (Premium Properties): The segment likely includes high-gain 

Segment 1 (Valuable Properties): The segment likely includes apartments that are more affordable for people on a budget.

Segment 2 (Standard Properties): The segment likely includes smaller homes that are affordable for first-time homebuyers with negligible gain 

Segment 3 (Budget Properties): The segment likely includes properties that are not great investment




### Approach 

## EDA 
-> Focused how every variable affects the Supervised Part Target Variable ( Sale Price ) and if there are any relations the derived insights and cited them 

## Data Engineering 
-> Mostly Concentrated are there any patterns in those observations that show a lot of contrast between the Sale Price and the Estimated Price if not the removed such values so these values does not create discrepancy in the Model's Predictions
-> Perfomed Chi-Square Test to determine the unwanted relationships between the categorical variables , also did the same for numerical vars by using Pearson Correlation Matrix .

### Supervised 

## Model Building
-> As there were multiple variables and the basic models  weren't performing good enough so focused more on Bagging and Boosting Models like Random Forest , Extra Trees , AdaBoost , Gradient Boost  and XG Boost 
-> Also tried using Ensemble Models like Stacking and Voting Models

### Unsupervised 
->  Applied a K-Means Model by simply using Trial and Error Method using a set of variables focusing more over Gain as it defines the whole Segmentation with the perspective of the investors and Segregated the Clusters on the basis of it .
