# EarthquakeAnalysis-VA

----

A comprehensive academic report produced as a submission for the Visual Analytics module as part of my MSc Data Science Course at City, University of London.

Programming Languages: Python (Folium, Statsmodels, Scikit-Learn, Plotly and GeoPy including the commonly used Numpy, Pandas, Matplotlib and Seaborn)
Visualisation Software: Tableau

The report provides a spatio-temporal analysis of significant earthquakes that occured between 1965 and 2016 containing over 20,000 observations.

The following questions were investigated:

1. Is there a detectable seasonality in earthquakes or peculiar years in terms of magnitude?
2. Can we identify the most susceptible countries, and identify countries expected to receive increased impact if earthquakes exhibit temporally increasing trends?
3. Can we develop a reliable time series model to predict the expected number of earthquakes in following years?

----

Paper Abstract:

The report utilizes cluster maps and time series to identify temporal patterns, possible seasonality and peculiar time periods. Density-based clustering methods such as DBSCAN 
and OPTICS are implemented to aide in identifying oceanic hotspots, used in combination with tree maps to identify the most susceptible countries. Time-series analysis is 
implemented to identify countries expected to receive increased earthquakes in the future through assessment of plate boundaries with risk analysis implemented to locate which 
countries will become further unsafe. ARIMA models are developed to help predict the total number of earthquakes in following years with close examinations of ACF and PACF plots
as well as model diagnostics by consideration of residuals.

----

The initial dataset which contained 21 features had 13 redundant features, much of which were irrelevant to the analysis with the remaining containing 30-99% missing values and 
therefore of little use. Hence, significant feature engineering was carried out such as binning of features, using geo-enconding to extract countries from latitudes and 
longitudes and thereby the continent (which proved immensely useful - earthquakes that occurred at sea could not be tied to a country, hence naturally filtering oceanic 
earthquakes allowing for more interesting analysis), and using K-Means Clustering with a very large amount of clusters, not for the purpose of clustering, but to create many 
tight clusters of points to assign the plate boundary these earthquakes occured on, and also the type of plate boundary (which worked extremely well - all the tiny clusters 
created lied exactly on plate boundaries (via use of an additional dataset merged containing worldwide tectonic plate boundary locations) which was surprising as latitude and 
longitude was used for clustering with the algorithm implementing Euclidean distances)

As mentioned in the abstract, many complex techniques are implemented such as DBSCAN and OPTICS clustering to identify spatial hotspots, as well as risk analysis and ARIMA
modelling and prediction for time-series hence I would recommend giving this a read!
