=========================

##making open geo data of the new Paso Robles sub-appellations

###news article:  
http://kcbx.org/post/paso-robles-wine-growing-region-has-new-recognition-its-diversity

###data source:  
http://www.ecfr.gov/cgi-bin/text-idx?SID=b93ce2451136237633a995e00e67e21f&node=20141009y1.2

###support tools:  
* http://geojson.io
* http://qgis.org (Vector>Geometry Tools>Lines to Polygons of my josm-osm>geojsonio-geojson-line>qgis-shp-poly>qgis-geojson-poly)
* http://ogre.adc4gis.com/ (convert EPSG:2229 shapefile to geojson -> geojson.io to kml for JOSM reference via opendata plugin)
* JOSM + opendata plugin (`F` follow way tool, Create New Layer > Save As .osm > geojson.io > Save As .geojson) I finally remembered you can Save As .geojson from JOSM.
* http://www.ngs.noaa.gov/NGSDataExplorer/ (National Geodetic Survey Data Explorer, to lookup benchmarks not visible on USGS Topos)

###support data:  
* City Limits
 - http://lib.calpoly.edu/gis/browse.jsp?by=th&th=11
* Hydrography
 - http://datagateway.nrcs.usda.gov/GDGOrder.aspx
* JOSM topos
 - These are the scanned USGS topographic maps we really want, not the USA Topos
 - I used the TileLayerPlugin for QGIS with this .tsv `topos   JOSM_topos      http://a.tile.openstreetmap.us/usgs_scanned_topos/{z}/{x}/{y}.png`, borrowed/altered from JOSM/OSM-US
* OSM
 - OpenLayers plugin within QGIS
* Teale Public Land Survey System (has Land Grant boundaries)
 - http://www.atlas.ca.gov/download.html#/casil/planning/planningAndDevelopment
* (San Luis Obispo County) SLO Aerials
 - tms:`http://gis.slocounty.ca.gov/arcgis/rest/services/Aerials/2011_Combined_WGSWMAS/MapServer/tile/{zoom}/{y}/{x}`
* SLO Roads
 - http://slocountyfire.org/data.html
* USA Topo (meh)
 - what The National Map - Service Endpoints point to now. Doesn't have the same map features which are in description.

###errors encountered
1. §9.239   Creston District. 11) BM 1533 (located beside Creston Shandon Road (State Route 41)) **cannot find**
2. §9.240   El Pomar District. 22) Proceed east along the southern boundary of section 4 approximately 0.75 mile to the section line's intersection with State Route 41; then **do you mean *'Proceed west'*?**
