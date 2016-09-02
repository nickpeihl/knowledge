# Geo Web

## GeoJSON
An interchange format for geographic data on the web.
Only WGS84 projections are supported.

### Creating GeoJSON files

When converting shapefiles to GeoJSON with `ogr2ogr` (<http://gdal.org>) use the `-lco COORDINATE_PRECISION` flag to reduce the number of decimal places in the latitude and longitude coordinates. This also helps reduce file sizes of GeoJSON files which can get very large and unwieldy for rendering on web maps. I think five or six is a good number for ensuring data consistency while understanding the limits of GPS and accuracy of most GIS data.

`ogr2ogr` also does not handle the reprojection of data to WGS84 automatically. You should probably always include the `t_srs "EPSG:4326"` flag to ensure your data is reprojected to WGS84.

For example: `ogr2ogr -f GeoJSON -t_srs "EPSG:4326" -lco COORDINATE_PRECISION=5 shape.geojson shape.shp`

### Sharing GeoJSON files

Upload to <http://gist.github.com> No account is required, but I recommend having one.

DON'T upload very large GeoJSON files to Gist. Anything over 2-3MB can take a long time to render. If you want to share very large files, consider that GeoJSON might not be the best way to share.

### Viewing GeoJSON files

For small GeoJSON files (up to 2-3MB)
* <http://geojson.io>
* <http://dropchop.io>
* <https://gist.github.com>
* <https://github.com>

For larger GeoJSON files (up to 100MB)
* <https://github.com/anandthakker/gjv>


### Links
* <http://geojson.org>
* <https://github.com/tmcw/awesome-geojson>
