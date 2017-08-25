# day one

## Building the capital planning platform
http://capitalplanning.nyc.gov

docker-carto on GitHub

Jane Maps on npm - UI and layout

## React Native
Android and iOS

One code base

### react-native-maps by Airbnb
Supports tile overlays using tile URLs

No offline support

Performance lags with 1000s of features

### react-native-mapbox-gl
Supports offline

Experimental

### boundless mobile
Spatialconnect

Offline with geopackages

## GPUs in geovisualization
MapD - organization

Middleware between db and output data

## Discovering open data
Opendatasoft

http://Singulardata.net

Singulardata on GitHub

## Browser geoprocessing with turf


## offline mobile maps with sqlite
Sqlite incremental update using sqldiff

Sync would work by timestamp

Probably native app only

## offline first mapping
http://calvinmetcalf.github.io/offline-talk

Service worker to check if server is offline and display contact info to user

Idea to use Service worker to serve content from indexeddb

## open source job

# day two

## data for digital services in state government
Focus on user experience.

Guide the user to the endpoint the same way amazon guides users to a purchase

Analytics.usa.gov

Net performer score

Treejack

Chalkmark

Crazyegg

Superset

Massgov on GitHub

## coding as a first resort
Understanding a task means being able to teach someone else how to do it

Abstracting a complex task into a simple task is even better

## transforming data for d3
Transportation planners

Pavement condition as gradiant horizontal straight linear plot

https://ctps.org/dv/lrtp_dashboard

## why 3D

## data driven styling in Mapbox-GL
Webgl not part of browser Dom

Uniforms -vertez and fragment shaders

Attributes - vertex shaders

Varying - passed from vertex to fragment shader

## how vector maps work Mapbox-GL
Why vector maps?

* Smooth zoom
* Perspective view
* 3d capabilities
* Data driven styling
* Full control of styling in browser
* Any map object is interactive
* Render millions of features
* Add video to maps
* Less bandwidth than raster

Triangles are the basis for opengl

Webgl used by 94% of user's browsers in USA

Earcut library splits polygons into triangles

GeoJSON can be too large to parse in the browser so they convert it to protocol-buffers

Pbf is 3-4 times smaller and 5-7 times faster than gj

Labels are placed using grid-index

# day three

## migrating to vector tiles
Nbt solutions

They wrote their own leaflet plugin called leaflet.vectortiles

## raster disaster, vector Spectre
Grout - Rust library for tiling - not os yet

## Local government using mapjunction for Boston history
Mapjunction - four way slider for map comparison

Story map that compares historical maps with current maps of Boston.

## last mile problem - trimet
Funded by Federal Mobility on demand sandbox program

Using opentripplanner

Integrated with Lyft

Using pelias for geocoder improvements

Trimet.org/mod

## tracking blight from archival documents
Book "visitation of God" potato famine

Search for "potato" in text and nearby geo names

Build a manual classifier as useful, not useful, etc

Used pdfminer to convert PDF to text

Use Peter norvig's library for spelling correction

Search text with nltk Python module

Use text dispersion plots to identify correlation

Keytermsearcher Python module

Clavin geoparser

Ngram viewer

Gdalt project

## metric geometry and gerrymandering
District builder by azevea

Local optimization - software improvement

"Pareto optimality"

Sampling/mcmc

on GitHub
* District-genius
* Qgis-compactness
* python-mander

## the rise of big data (build it, hack it, share it)
How to find ghost cities in China
1. Scrape pois from Google and calculate amenity score (distance from restaurants or stores, Yelp ratings, etc)
2. Cluster
3. Ground truth

http://civicdatadesignlab.org
