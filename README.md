# NYC_taxi

It is a Kaggle`s "New York City Taxi Trip Duration" challenge solution.

## Data preprocessing

This dataset contains 5 interesting columns, I can work with: ['pickup_datetime', 'pickup_longitude', 'pickup_latitude', 'dropoff_longitude', 'dropoff_latitude'].

Steps:
1) Removing 'id' column in both datasets and dropping 'dropoff datetime' in train data, because it is result of taxi trip, pickup_datetime + trip_duration = dropoff_datetime.
2) Replacing (Y, N) with (1, 0) in 'store_and_fwd_flag' dolumn.

### Let`s take a closer look at latitudes and longitudes we have.

3) Getting distance between pickup and dropoff coordinates, geopsy.distance.geodesic function will help to do it.
4) Adding a column 'weekday' that contain numbers from 0 to 6, [Monday - Sunday].
5) Adding a column 'hour' that contain numbers from 0 to 23 [00:00 - 23:00].

## Submissions

First submission is simple regression, the score is 0.56946, actually a poor result. Inputs are: ['vendor_id', 'passenger_count', 'store_and_fwd_flag', 'distance']

Adding a column 'weekday' that contain numbers from 0 to 6, [Monday - Sunday] had a small impact on model. Ther result now is: 0.56035. The column should have impact on model, because weekdays affect traffic jams, so trip ride. The way to improve accuracy - is making a model deeper, for example adding a second layer. In a result, the score is 0.50544 now. Adding 'hours' column also improved accuracy.

## Fine-tuning
