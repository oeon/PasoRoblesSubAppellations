# ❗️use this instead: https://github.com/UCDavisLibrary/ava

I wasn't able to finish this project and some other people have done it better ☝️

=========================

## making open geo data of the new Paso Robles sub-appellations

### I'm using JOSM Editor with OpenStreetMap data to digitize textual descriptions of boundaries, using JOSM to trace along OSM vector data and referencing (imagery & USGS topo) basemaps - along with various other open geo tools and data.

### news article:  
http://kcbx.org/post/paso-robles-wine-growing-region-has-new-recognition-its-diversity

### data source(s):  

http://www.regulations.gov/#!documentDetail;D=TTB-2013-0009-0060

*broken* http://www.ecfr.gov/cgi-bin/text-idx?SID=b93ce2451136237633a995e00e67e21f&node=20141009y1.2

### support tools:  
* http://geojson.io
* http://qgis.org (Vector>Geometry Tools>Lines to Polygons of my josm-osm>geojsonio-geojson-line>qgis-shp-poly>qgis-geojson-poly)
* http://ogre.adc4gis.com/ (convert EPSG:2229 shapefile to geojson -> geojson.io to kml for JOSM reference via opendata plugin)
* JOSM + opendata plugin (`F` follow way tool, Create New Layer > Save As .osm > geojson.io > Save As .geojson)
* http://www.ngs.noaa.gov/NGSDataExplorer/ (National Geodetic Survey Data Explorer, to lookup benchmarks not visible on USGS Topos)
* Paletton - The Color Scheme Designer: http://paletton.com/

### support data:  
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
 - http://www.atlas.ca.gov/download.html#/casil/planning/planningAndDevelopment, `"LANDGRANT" IS NOT NULL`
* (San Luis Obispo County) SLO Aerials
 - tms:`http://gis.slocounty.ca.gov/arcgis/rest/services/Aerials/2011_Combined_WGSWMAS/MapServer/tile/{zoom}/{y}/{x}`
* SLO Roads
 - http://slocountyfire.org/data.html
* USA Topo (meh)
 - what The National Map - Service Endpoints point to now. Doesn't have the same map features which are in description.

### errors encountered
1. §9.239   Creston District. 11) BM 1533 (located beside Creston Shandon Road (State Route 41)) **cannot find**
2. §9.240   El Pomar District. 22) Proceed east along the southern boundary of section 4 approximately 0.75 mile to the section line's intersection with State Route 41; then **do you mean *'Proceed west'*?**
3. §9.244   Willow Creek District 7) Jack Creek Road does not intersect Highway 46 (any longer, only on USGS topo map)
4. § 9.245 San Juan Creek 1) to the road's intersection with the San Luis Obispo-Kern County boundary line at the eastern boundary line of section 12, T28S/R16E, which is also concurrent with the R16E/R17E common boundary line; **Kern County boundary is nowhere near here** 2) to the boundary line's intersection with anunnamed unimproved road locally known as Navajo Creek Road, immediately south of the 1,340-foot elevation line, section 13, T28S/R16E; **unimproved road no longer exists, only exists on topo map**
