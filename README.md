# NYC_taxi

It is a Kaggle`s "New York City Taxi Trip Duration" challenge solution.

## Data preprocessing

This dataset contains 5 interesting columns, I can work with: ['pickup_datetime', 'pickup_longitude', 'pickup_latitude', 'dropoff_longitude', 'dropoff_latitude'].

### Steps: 

1) Removing 'id' column in both datasets and dropping 'dropoff datetime' in train data, because it is result of taxi trip, pickup_datetime + trip_duration = dropoff_datetime.
2) Replacing (Y, N) with (1, 0) in 'store_and_fwd_flag' dolumn.
3) Getting distance between pickup and dropoff coordinates, geopsy.distance.geodesic function will help to do it.
4) Next important step for data preprocessing is converting 'pickup_datetime' column to datetime from string. Let`s analize this column a little bit deeper.

#### 'pickup_datetime'

Day and time of the week, have an impact on traffic, let`s take a look how!

