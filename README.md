# Animated heat map combined with choropleth map
This project introduces how to plot choropleth and heat map with folium, but raw data needs to be processed with geopandas and pandas.

The first part is to make a choropleth map dispalying population density in different districts (counties) in Shanghai, China. The tricky thing is that the original coordinate system of shapefile is WGS84, whose unit is in degree (geographical coordinate system) and cannot be used for area calculation. Therefore, I need to project it to coordinate system in distance, and then calculate the area. 

I tried two ways when mapping population density: one is simple but boring with **folium.Choropleth** which does not provide much styling and interactivity function, the other is based on **folium.GeoJson** that you could customize the color shceme, tooltips and so one. 

The second part is to plot the heat map. Folium has leaflet external plugins, which could generate them. I think the hardest parts are to figure out the data structure required for heat map and create list comprehension after cleaning up the raw data. 

## How to use
Run the `Animated heat map combined with choropleth map.ipynb` and all the data needed are stored in `/data`.

## Additional Information

* folium plugins turtorials: https://python-visualization.github.io/folium/plugins.html

* How to make a simple choropleth map: https://python-visualization.github.io/folium/quickstart.html#Choropleth-maps

* branca for colormap: https://python-visualization.github.io/branca/colormap.html

* A well-written turtorial you may want to take a look at: https://towardsdatascience.com/data-101s-spatial-visualizations-and-analysis-in-python-with-folium-39730da2adf
