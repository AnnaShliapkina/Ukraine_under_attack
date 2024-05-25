# README

## Overview

This project visualizes event data using the `folium` library to create interactive maps. The data includes geographic coordinates and various event types, such as "Shelling/artillery/missile attack," "Air/drone strike," and "Remote explosive/landmine/IED." Additionally, the project demonstrates the use of heatmaps and animated maps to illustrate the temporal and spatial distribution of fatalities.

## Data

The data used in this project is stored in a CSV file named `cleaned_data.csv`. It contains the following columns:

- `latitude`
- `longitude`
- `location`
- `sub_event_type`
- `event_date`
- `fatalities`

## Requirements

To run this project, you need the following libraries:

- pandas
- numpy
- folium
- folium.plugins
- matplotlib
- seaborn
- plotly

You can install the required libraries using the following command:

```sh
pip install pandas numpy folium matplotlib seaborn plotly
```

# Event Data Visualizations

## Files

- **data/cleaned_data.csv**: The cleaned dataset containing event information.
- **charts/map.html**: A map displaying the first 10 events with markers.
- **charts/fatalities_map.html**: A map showing the total number of fatalities at different locations with scaled markers.
- **charts/monthly_fatalities_animation.html**: An animated map showing monthly fatalities.
- **charts/events_map.html**: A map displaying different event types with colored markers and a legend.
- **charts/heatmap.html**: A heatmap displaying the density of events.

## Usage

### Map with Fatalities

This map visualizes locations with fatalities using scaled markers based on the number of fatalities. The map is saved as [fatalities_map.html](https://annashliapkina.github.io/Ukraine_under_attack/charts/fatalities_map.html).

### Animated Map of Monthly Fatalities

This map shows the temporal distribution of fatalities using an animated timeline. The map is saved as [monthly_fatalities_animation.html](https://annashliapkina.github.io/Ukraine_under_attack/charts/monthly_fatalities_animation.html).

### Event Type Map

This map displays different types of events with colored markers. The legend explains the color coding. The map is saved as [charts/events_map.html](https://annashliapkina.github.io/Ukraine_under_attack/charts/events_map.html).

### Heatmap

This heatmap shows the density of events across different locations. The map is saved as [heatmap.html](https://annashliapkina.github.io/Ukraine_under_attack/charts/heatmap.html).
