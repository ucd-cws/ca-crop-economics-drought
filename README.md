# ca-crop-economics
Web application displaying crop water usage information for California.


## Data Prep

CSV data was joined to the CVPM shapefile in ArcGIS. Then, the shapefile was exported with the additional attribute table as new shapefile. The shapefile with attributes was then converted to geojson using `ogr2ogr -f GeoJSON -t_srs crs:84 [name].geojson [name].shp`.

The attribute names for the data should follow the pattern of {variable}_{year} (ie "total_irrigated_crop_area_2000").

irrig = irrigation crop area (units acres)
app = applied water (units acre-feet)
grev = gross revenue (dollars)
dirjobs = direct jobs (change in number of jobs)


## Dev

To run locally with python, `python -m SimpleHTTPServer` and page will be available at `localhost:8000`
