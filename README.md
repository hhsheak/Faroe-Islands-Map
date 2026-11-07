# Faroe-Islands-Map

This is an attempt to improve my cartography skills by showcasing the mountainous terrain of the Faroe Islands.

## Step 1: Creating the Map
I downloaded the DTM provided by the Faroese Environmental Agency (Umhvørvisstovan) on their Føroyakort mapping portal (https://www.foroyakort.fo/tak-datur-nidur/dtm-og-dsm-haeddarmodell). I rendered the layer using a singleband psuedocolour renderer and styled it using a green–red colour ramp. Hillshade data was taken from the Føroyakort portal (https://www.foroyakort.fo/tak-datur-nidur/skuggakort) and styled following this tutorial (https://www.youtube.com/watch?v=rPrC3qOtRAk). Bathymetric data was also taken from the Føroyakort portal (https://www.foroyakort.fo/tak-datur-nidur/datur-a-sjonum). I chose to set 100 metres as the maximum depth so as to simplify the map. 

After styling the topography of the archipelago, I created a point layer for the largest settlement of each island. Black text with a white background was used to improve the readability of the labels. Tórshavn was given special styling to emphasise its special status as capital.

After styling the various layers, I then created the print layout of the map.

## Step 2: Creating the 3D Render of Vágar
I wanted to try integrating Blender with QGIS and given the dramatic topography of the Faroe Islands, I thought it would interesting to render it in 3D. Vágar, in particular, was chosen given its especially dramatic topography, such as Sørvágsvatn (the lake on a cliff).

Imported a vector layer from the QuickOSM plugin and used the "Clip Mask by Layer" tool to restrict the DTM to Vágar (and part of the surrounding islands). I then exported the DTM to Blender. 

Following the advice provided by Alexander Orlovsky (https://gis.stackexchange.com/questions/443514/disable-labeling-of-osm-in-qgis), I imported OSM data of the island and deleted most of the vector layers, leaving only the terrain layers in order to show the geographical terrain of the island, which I then exported.

I followed this tutorial (https://www.youtube.com/watch?v=J8wkghNmsWc) to render the island and styled it based on the exported OSM vector layer. The main difficulty faced was in trying to find the right angle to place the camera. The DTM exported included parts of the neighbouring island, Streymoy. However, as the remainder of the island was cut off, it appeared as though the island was smaller than it actually was. I did not want to misrepresent the geography of the island and hence, I sought to minimise its presence in the render. Additionally, part of the ocean rendered behind Streymoy and hence, I placed the title there to cover up that part of the ocean.
