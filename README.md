# cis2450project

Crystal Yang & Shishir Varghese

## London Airbnb Price Prediction Dashboard

This project uses Airbnb listing data and OpenStreetMap point-of-interest data to explore and predict Airbnb listing prices. The final project includes data cleaning, exploratory data analysis, spatial feature engineering, model comparison, feature importance, and an interactive Streamlit dashboard.

## Data Download Instructions

Our datasets are too large to upload directly to GitHub because they are over 25 MB. To run the project, download the datasets manually using the instructions below.

## 1. Airbnb Listings and Reviews Data

Download the Airbnb dataset from Kaggle:

https://www.kaggle.com/datasets/mysarahmadbhat/airbnb-listings-reviews?resource=download

After downloading, unzip the file and place the relevant Airbnb CSV files inside the project folder.

## 2. OSM Data - London
How to download data for osm. First, go to https://overpass-turbo.eu/

Paste in this but change for the city: 
[out:json][timeout:120];

{{geocodeArea:Paris, France}}->.searchArea;

(
  node["amenity"="restaurant"](area.searchArea);
  way["amenity"="restaurant"](area.searchArea);
  relation["amenity"="restaurant"](area.searchArea);

  node["amenity"="cafe"](area.searchArea);
  way["amenity"="cafe"](area.searchArea);
  relation["amenity"="cafe"](area.searchArea);

  node["amenity"="bar"](area.searchArea);
  way["amenity"="bar"](area.searchArea);
  relation["amenity"="bar"](area.searchArea);

  node["amenity"="pub"](area.searchArea);
  way["amenity"="pub"](area.searchArea);
  relation["amenity"="pub"](area.searchArea);

  node["leisure"="park"](area.searchArea);
  way["leisure"="park"](area.searchArea);
  relation["leisure"="park"](area.searchArea);

  node["tourism"="attraction"](area.searchArea);
  way["tourism"="attraction"](area.searchArea);
  relation["tourism"="attraction"](area.searchArea);

  node["tourism"="museum"](area.searchArea);
  way["tourism"="museum"](area.searchArea);
  relation["tourism"="museum"](area.searchArea);

  node["highway"="bus_stop"](area.searchArea);
  way["highway"="bus_stop"](area.searchArea);
  relation["highway"="bus_stop"](area.searchArea);

  node["railway"="station"](area.searchArea);
  way["railway"="station"](area.searchArea);
  relation["railway"="station"](area.searchArea);

  node["public_transport"](area.searchArea);
  way["public_transport"](area.searchArea);
  relation["public_transport"](area.searchArea);
);
out center;

Once your data is good go to export, GeoJSON, and download. 


The explanation of our design choices are found in the text of our IPYNB file. Enjoy!
