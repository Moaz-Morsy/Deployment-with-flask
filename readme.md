# Automobile Analysis and Model Development

## Dataset

### Context
This dataset consist of data From 1985 Ward's Automotive Yearbook. Here are the sources

Sources:

1. 1985 Model Import Car and Truck Specifications, 1985 Ward's Automotive Yearbook.
2. Personal Auto Manuals, Insurance Services Office, 160 Water Street, New York, NY 10038
3. Insurance Collision Report, Insurance Institute for Highway Safety, Watergate 600, Washington, DC 20037

### Content
This data set consists of three types of entities: (a) the specification of an auto in terms of various characteristics, (b) its assigned insurance risk rating, (c) its normalized losses in use as compared to other cars. The second rating corresponds to the degree to which the auto is more risky than its price indicates. Cars are initially assigned a risk factor symbol associated with its price. Then, if it is more risky (or less), this symbol is adjusted by moving it up (or down) the scale. Actuarians call this process "symboling". A value of +3 indicates that the auto is risky, -3 that it is probably pretty safe.

The third factor is the relative average loss payment per insured vehicle year. This value is normalized for all autos within a particular size classification (two-door small, station wagons, sports/speciality, etc…), and represents the average loss per car per year.

Note: Several of the attributes in the database could be used as a "class" attribute.

### Sources:
- Dataset source: https://www.kaggle.com/toramky/automobile-dataset

## Data Preprocessing

### Quality:
- 'normalized-losses' column contains about 40 missing values (nan values), replace them with average of the existing values of the column
- 'num-of-doors' column contains about 2 missing values, replace them with most frequent value in column
- 'bore' column contains about 4 missing values, replace them with average of the existing values of the column
- 'stroke' column contains about 4 missing values, replace them with average of the existing values of the column
- 'horsepower' column contains about 2 missing values, replace them with average of the existing values of the column
- 'peak-rpm' column contains about 2 missing values, replace them with average of the existing values of the column
- "fuel-type","aspiration", "num-of-doors","body-style","drive-wheels","engine-location","engine-type","num-of-cylinders","fuel-system" columns are object type, change them to category type
- "normalized-losses","horsepower","peak-rpm" are float type, change them to int type
- 'price' column contains about 4 missing values, replace them with average of the existing values of the column

### Data Cleaning
- 'normalized-losses' column contains about 40 missing values (nan values), replace them with average of the existing values of the column
- 'bore' column contains about 4 missing values, replace them with average of the existing values of the column
- 'stroke' column contains about 4 missing values, replace them with average of the existing values of the column
- 'horsepower' column contains about 2 missing values, replace them with average of the existing values of the column
- 'peak-rpm' column contains about 2 missing values, replace them with average of the existing values of the column
- 'price' column contains about 4 missing values, replace them with average of the existing values of the column

### Feature Engineering
- transform 'city-mpg'(mile per gallon) to 'city-l/100km'(liter per 100km)
- transform 'highway-mpg'(mile per gallon) to 'highway-l/100km'(liter per 100km)
- transform 'horsepower' from continous values to discrete categorical values

## Exploration Analysis

### Univariate Exploration
- Categorical Variables
- Numerical Variables
### bivariate Exploration
- Categorical variables vs. price
- Numerical variables vs. price

## Model Development and Deployment
- Simple Linear Regression
- Multi-Linear Regression
- Polynomial Regression
- Ridge Regression
- SVR
- Decision Tree Regressor
- Random Forest Regressor
- XGBRegressor
- Model Evaluation
- Grid Search and Final Model
- Model Deployment with Flask: https://automobile-price-predictor.herokuapp.com/

