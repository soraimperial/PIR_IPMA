# PIR_IPMA Archive
First ever coding project. Might suck. Also, LLM-assisted coding.

The PIR (Wildfire Meterological Danger) wms service from IPMA is quite unstable.
It is set as a dynamic temporal layer that is not correctly configured and quite often times out during high traffic hours, making it unusable for decision support in operational context. Also, the IPMA service provides a raster, which is not very useful if you quickly need a list.

This small .py aims to create a daily archive of PIR, by taking the IPMA json API and joining it with any geopackage that has a "Dico" field (e.g. CAOP). This way, you have a vectorised layer for all your needs, effectively recreating the PIR maps from the IPMA website.

Just replace your paths in the file for the geopackage and output locations.

Also, it is also meant to be used by people who have never used a lot of GIS. I am aware this is easily done by other methods with dynamic joins.

Use cases: mostly identifying restrictions in activities according to PIR (e.g. forestry work).


