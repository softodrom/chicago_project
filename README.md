# chicago_project

Based on: https://github.com/ageron/handson-ml/blob/master/02_end_to_end_machine_learning_project.ipynb

Based on the dataset from Kaggle: https://www.kaggle.com/datasets/currie32/crimes-in-chicago

## Questions (brainstorming so far)

- The likelihood of a crime in a specfic season/area
- How likely are we to get arrested doing a specific crime, at a specific place in a specific date and time
- Based on year, months day and district predict the crime rate

## Resource bookmarks, to get help and inspiration

About frequencies: https://towardsdatascience.com/pandas-sidetable-how-you-calculate-frequencies-the-easy-way-d56afa90973c

About pandas and timeseries:

- https://ourcodingclub.github.io/tutorials/pandas-time-series/
- https://machinelearningmastery.com/basic-feature-engineering-time-series-data-python/
- https://machinelearningmastery.com/time-series-forecasting/

Classical timeseries forecasting models:

- https://machinelearningmastery.com/time-series-forecasting-methods-in-python-cheat-sheet/
- https://machinelearningmastery.com/backtest-machine-learning-models-time-series-forecasting/
- Train ARIMA: https://machinelearningmastery.com/arima-for-time-series-forecasting-with-python/
- Tune ARIMA https://machinelearningmastery.com/grid-search-arima-hyperparameters-with-python/

Machine Learning models for timeseries:

- https://machinelearningmastery.com/time-series-forecasting-supervised-learning/
- https://machinelearningmastery.com/multivariate-time-series-forecasting-lstms-keras/
- https://machinelearningmastery.com/how-to-develop-convolutional-neural-network-models-for-time-series-forecasting/
- https://machinelearningmastery.com/how-to-develop-lstm-models-for-time-series-forecasting/

About timeseries forecasting, classical vs machine learning algorithms:

- https://machinelearningmastery.com/convert-time-series-supervised-learning-problem-python/
- https://machinelearningmastery.com/findings-comparing-classical-and-machine-learning-methods-for-time-series-forecasting/

Relevant tutorials based on our dataset:

- https://medium.com/@namanjain2050/hands-on-machine-learning-with-chicago-crime-data-3657b713d62c
- https://github.com/avi30ch/chicagoCrimeAnalysis/blob/main/ChicagoCrimeForecastingArima.ipynb
- http://reach4ml.org/using-data-science-along-with-machine-learning-to-predict-the-future-theft-crime-rates-in-chicago/
- https://github.com/Jashu-MJ/Chicago-Crime-Data-Analysis/blob/master/Crime%20Analysis%20Final.ipynb
- https://github.com/Ravisutha/CrimePrediction
- https://medium.com/analytics-vidhya/predicting-arrests-looking-into-chicagos-crime-through-machine-learning-78697cc930b9
- https://github.com/rahulbordoloi/Predict-Crime-Rate-in-Chicago/blob/master/Predict_Crime_Rate_in_Chicago.ipynb

## Dataset Info:

About the geographical districts: From bigger to smaller: District > Community Area > Ward > Blocks (basically a building block)

- ID - Unique identifier for the record.
- Case Number - The Chicago Police Department RD Number (Records Division Number), which is unique to the incident.
- Date - Date when the incident occurred. this is sometimes a best estimate.
- Block - The partially redacted address where the incident occurred, placing it on the same block as the actual address.
- IUCR - The Illinois Unifrom Crime Reporting code. This is directly linked to the Primary Type and Description. See the list of IUCR codes at https://data.cityofchicago.org/d/c7ck-438e.
- Primary Type - The primary description of the IUCR code.
- Description - The secondary description of the IUCR code, a subcategory of the primary description.
- Location Description - Description of the location where the incident occurred.
- Arrest - Indicates whether an arrest was made.
- Domestic - Indicates whether the incident was domestic-related as defined by the Illinois Domestic Violence Act.
- Beat - Indicates the beat where the incident occurred. A beat is the smallest police geographic area – each beat has a dedicated police beat car. Three to five beats make up a police sector, and three sectors make up a police district. The Chicago Police Department has 22 police districts. See the beats at https://data.cityofchicago.org/d/aerh-rz74.
- District - Indicates the police district where the incident occurred. See the districts at https://data.cityofchicago.org/d/fthy-xz3r.
- Ward - The ward (City Council district) where the incident occurred. See the wards at https://data.cityofchicago.org/d/sp34-6z76.
- Community Area - Indicates the community area where the incident occurred. Chicago has 77 community areas. See the community areas at https://data.cityofchicago.org/d/cauq-8yn6.
- FBI Code - Indicates the crime classification as outlined in the FBI's National Incident-Based Reporting System (NIBRS). See the Chicago Police Department listing of these classifications at http://gis.chicagopolice.org/clearmap_crime_sums/crime_types.html.
- X Coordinate - The x coordinate of the location where the incident occurred in State Plane Illinois East NAD 1983 projection. This location is shifted from the actual location for partial redaction but falls on the same block.
- Y Coordinate - The y coordinate of the location where the incident occurred in State Plane Illinois East NAD 1983 projection. This location is shifted from the actual location for partial redaction but falls on the same block.
- Year - Year the incident occurred.
- Updated On - Date and time the record was last updated.
- Latitude - The latitude of the location where the incident occurred. This location is shifted from the actual location for partial redaction but falls on the same block.
- Longitude - The longitude of the location where the incident occurred. This location is shifted from the actual location for partial redaction but falls on the same block.
- Location - The location where the incident occurred in a format that allows for creation of maps and other geographic operations on this data portal. This location is shifted from the actual location for partial redaction but falls on the same block.
