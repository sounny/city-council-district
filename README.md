# Detroit City Council District Map

## Overview

This application displays an interactive map of Detroit City Council Districts using the ArcGIS API for JavaScript. It features a full-screen map, search functionality, and interactive widgets such as a basemap gallery, search widget, and a home button. Additionally, it integrates a feature to log search results (address, latitude, longitude) to an ArcGIS Online (AGOL) table when a search result is selected.

## Features

- **Full-Screen Map View**: Displays the Detroit City Council districts.
- **Search Functionality**: Allows users to search for locations. Selected search results are automatically logged to an AGOL table.
- **Interactive Widgets**:
  - **Basemap Gallery**: Allows users to switch between different basemaps.
  - **Home Button**: Resets the map to the initial view.
  - **Expandable Containers**: For the basemap gallery and search widget, improving the user interface by minimizing screen clutter.
- **Logging Search Results**: Automatically adds search results to an AGOL table, capturing address, longitude, and latitude.

## Technology

- **ArcGIS API for JavaScript**: Utilizes version 4.25 for mapping and GIS functionalities.
- **HTML/CSS**: For structuring and styling the webpage.

## Setup and Configuration

1. **API Key**: Ensure you have a valid ArcGIS API key configured in the `esriConfig` object. Replace `"YOUR_API_KEY_HERE"` with your actual API key.
2. **AGOL Table URL**: The current setup points to a table intended for tracking search results. Ensure the URL and field names in the `FeatureLayer` configuration match your AGOL table setup.

## Code Structure

- **HTML**: Sets up the basic structure and links to the ArcGIS API CSS and JavaScript files.
- **CSS**: Defines styles for full-screen map display and custom styles for interactive buttons.
- **JavaScript**:
  - **Module Loading**: Loads necessary ArcGIS modules using the `require` function.
  - **Map and View Setup**: Configures the map view, basemap, and initial zoom level.
  - **Widgets**: Initializes and configures widgets like the Basemap Gallery, Search, and Home button.
  - **Event Handling**: Adds functionality to log selected search results to an AGOL table using the `applyEdits` method of `FeatureLayer`.

## Usage

To use this application:
- Open the HTML file in a web browser with JavaScript enabled.
- Use the search bar to find locations within Detroit. Selected locations will automatically be logged to the configured AGOL table.

## Customization

- **Basemap and Initial View**: Customize the initial basemap and view settings by modifying the `basemap` and `center` properties in the `Map` and `MapView` configurations.
- **AGOL Table**: Adjust the URL and fields of the `trackerTable` `FeatureLayer` as per your AGOL table's schema.

