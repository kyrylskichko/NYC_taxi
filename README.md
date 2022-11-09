# NYC_taxi

It is a Kaggle`s "New York City Taxi Trip Duration" challenge solution.

## Data preprocessing

This dataset contains 5 interesting columns, I can work with: ['pickup_datetime', 'pickup_longitude', 'pickup_latitude', 'dropoff_longitude', 'dropoff_latitude'].

### Steps: 

1) Removing 'id' column in both datasets and dropping 'dropoff datetime' in train data, because it is result of taxi trip, pickup_datetime + trip_duration = dropoff_datetime.
2) Replacing (Y, N) with (1, 0) in 'store_and_fwd_flag' dolumn.
3) Getting distance between pickup and dropoff coordinates, geopsy.distance.geodesic function will help to do it.

## Submissions

First submission is simple regression, the score is 0.56946, actually a poor result. Inputs are: ['vendor_id', 'passenger_count', 'store_and_fwd_flag', 'distance']


## Fine-tuning
