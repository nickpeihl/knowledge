# gdal

## Create a jpg from an ArcGIS Server map service
``` shell
gdal_translate -of WMS "http://sjcgis.org/arcgis/rest/services/Basemaps/Aerials_2016_WM/MapServer?f=json" aerial.xml
gdal_translate -of JPEG -projwin -123.076744 48.577260 -123.053913 48.565433 -projwin_srs EPSG:4326 -outsize 500 0 aerial.xml aerial.jpg
```
_Note_: The `projwin` parameter is `upperleftx upperlefty lowerrightx lowerrighty`. The typical bounding box you'll get from a service like http://bboxfinder.com is `lowerleftx, lowerlefty, upperrightx, upperrighty`. The `upper{left|right}x` values are the same as the `lower{left|right}x` values because they share the same y-axis, so you can leave those the same. You'll have to swap the order of the y coordinates where `upperlefty` === `upperrighty` and `lowerrighty` === `lowerlefty`because they share the same x-axis.

## Drape styled parcel lines from an shapefile onto an ArcGIS Server map service and save the output as a PDF.
``` shell
gdal_translate -of WMS "http://sjcgis.org/arcgis/rest/services/Basemaps/Aerials_2016_WM/MapServer?f=json" aerial.xml
ogr2ogr -f "ESRI Shapefile" \
-sql "select *, 'PEN(c:#FF0000,w:5px)' as OGR_STYLE from parcels" \
parcel_styled.shp parcels.shp
gdal_translate -of PDF \
-projwin -123.076744 48.577260 -123.053913 48.565433 \
-projwin_srs EPSG:4326 \
-co DPI=300 \
-co WRITE_USERUNIT=YES \
-co "OGR_DATASOURCE=parcel_styled.shp" \
aerial.xml aerial.pdf
```

## See related
* [GDAL Website](http://gdal.org)
* [OSGeo4W](https://trac.osgeo.org/osgeo4w/)
* [Making geospatial PDF maps from OSM with GDAL (pdf)](http://latuviitta.org/documents/Geospatial_PDF_maps_from_OSM_with_GDAL.pdf)
* [GDAL GeoSpatial PDF Format](http://gdal.org/frmt_pdf.html)
* [OGR Feature Style Specification](http://gdal.org/ogr_feature_style.html)
