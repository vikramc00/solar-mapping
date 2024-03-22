# Solar Mapping

## Description
Assessing solar energy potential of building roofs, evaluating solar panel suitability and associated benefits

Technologies: Python, NumPy, pandas, geopy, PyTorch, ArcGIS API, Google OR Tools

## Process
- Compute optimal path for volunteers to congregate at a convenient public location (park), travel to pertinent locations and return
- Train GeoAI image analyst deep learning model to identify areas with high solar panel usage (number of buildings)

## Optimal path algorithm: Travelling Salesman Problem
- append_coordinates(): append relevant coordinates
- find_public_locations(): locate public areas for volunteers to congregate (parks)
- find_n_closest(): finds top n closest houses to the public place
- append_place(): adds location to stop
- find_distances(): make 2d-array of all pairs’ distances

## Train deep learning model
- ArcGIS API to prepare geospatial datasets, satellite imagery, aerial photography, other spatial data
- Explore geospatial data using ArcGIS tools
- Create GeoAI dataset: define a custom dataset class that inherits from arcgis.learn.Predictor
- Initialize + train data with fit method
- Evaluate with validation/test set

## Results
- Model Learning rate: 0.0017, 10 epochs
- Tested on Toole, Utah: 80% confidence level, 4000 image tiles: 5426 solar panel locations, 3563 buildings on 1st attempt
- Cut down volunteer travel time by 41%: computed difference between overall travel time spent by volunteers in Toole, Utah and estimated time that would be taken with the model, algorithm, and Maps estimation.






