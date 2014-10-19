PasoRoblesSubAppellations
=========================

###data source:  
http://www.ecfr.gov/cgi-bin/text-idx?SID=b93ce2451136237633a995e00e67e21f&node=20141009y1.2

###news article:  
http://kcbx.org/post/paso-robles-wine-growing-region-has-new-recognition-its-diversity

###support tools:  
* http://geojson.io
* http://qgis.org

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
* Public Land Survey (filled)
 - http://www.atlas.ca.gov/download.html#/casil/planning/planningAndDevelopment
* (San Luis Obispo County) SLO Aerials
 - http://gis.slocounty.ca.gov/arcgis/rest/services/Aerials/2011_Combined_WGSWMAS/MapServer/tile/{zoom}/{y}/{x}
* SLO Roads
 - http://slocountyfire.org/data.html
* USA Topo (meh)
 - what The National Map - Service Endpoints point to now. Doesn't have the same map features which are in description.
