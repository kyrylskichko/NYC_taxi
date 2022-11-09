# NYC_taxi

It is a Kaggle`s "New York City Taxi Trip Duration" challenge solution.

# Data preprocessing

This dataset contains 5 interesting columns, I can work with: ['pickup_datetime', 'pickup_longitude', 'pickup_latitude', 'dropoff_longitude', 'dropoff_latitude'].

### First step: 

Getting distance between pickup and dropoff coordinates, geopsy.distance.geodesic function will help to do it. 
