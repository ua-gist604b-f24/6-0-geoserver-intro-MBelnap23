What is the URL of the WMS GetCapabilities request?
https://fuzzy-spork-q7p4jpv5v7jjf4rww-8080.app.github.dev/geoserver/ows?service=WMS&version=1.3.0&request=GetCapabilities

What is the URL of the WFS GetCapabilities request?
https://fuzzy-spork-q7p4jpv5v7jjf4rww-8080.app.github.dev/geoserver/ows?service=WFS&version=1.1.0&request=GetCapabilities

Submit a screenshot of your updated WFS Layer Preview
Access to change the style was denied on multiple occasions and on all broswers

What does drawing order refer to? Which layer goes on top, the first or the last layer in the list?
The drawing order refers to how they are stacked on top of each other, and unlike Esri, the top most layer listed is the bottom-most layer in the stack.

Submit a screenshot of the Layer Preview of the Spearfish Layer Group when sf:sfdem is listed as the 3rd layer
Submitting the changes was not authorized in my codespace

What is the WMS url for the single-tiled request?

https://fuzzy-spork-q7p4jpv5v7jjf4rww-8080.app.github.dev/geoserver/wms?SERVICE=WMS&VERSION=1.1.1&REQUEST=GetMap&FORMAT=image%2Fpng&TRANSPARENT=true&STYLES&LAYERS=spearfish&exceptions=application%2Fvnd.ogc.se_inimage&SRS=EPSG%3A26713&WIDTH=1900&HEIGHT=1000&BBOX=586455.5713215427%2C4900389.464725851%2C658989.4591949271%2C4938565.195185526

What is the WMS url for one of the tiled requests? What is the image size?
https://fuzzy-spork-q7p4jpv5v7jjf4rww-8080.app.github.dev/geoserver/wms?SERVICE=WMS&VERSION=1.1.1&REQUEST=GetMap&FORMAT=image%2Fpng&TRANSPARENT=true&tiled=true&STYLES&LAYERS=spearfish&exceptions=application%2Fvnd.ogc.se_inimage&tilesOrigin=589425.9342365642%2C4913959.224611808&WIDTH=256&HEIGHT=256&SRS=EPSG%3A26713&BBOX=625471.1678513326%2C4935358.433826914%2C635244.1548490096%2C4945131.420824591

256x256

What is the URL of your coarse resolution sample of a WMTS url? What level does this tile refer to? Notice the differences. What are some of the fields that are unique to this url?
https://fuzzy-spork-q7p4jpv5v7jjf4rww-8080.app.github.dev/geoserver/gwc/service/wmts?VERSION=1.0.0&LAYER=spearfish&STYLE=&TILEMATRIX=EPSG:4326:11&TILEMATRIXSET=EPSG:4326&SERVICE=WMTS&FORMAT=image/png&SERVICE=WMTS&REQUEST=GetFeatureInfo&INFOFORMAT=text/html&TileCol=867&TileRow=518&I=106&J=61

Level 11

TileMatrixSet, TileCol, TileRow

In the zoomed-out URL, what are the TileCol and TileRow?

TileCol = 867
TileRow = 518

In the zoomed-in URL, what are the TileCol and TileRow?
https://fuzzy-spork-q7p4jpv5v7jjf4rww-8080.app.github.dev/geoserver/gwc/service/wmts?layer=spearfish&style=&tilematrixset=EPSG%3A4326&Service=WMTS&Request=GetTile&Version=1.0.0&Format=image%2Fpng&TileMatrix=EPSG%3A4326%3A20&TileCol=444446&TileRow=265205

TileCol = 444446
TileRow = 265205

Why are they so different for the same location in the map?
It is a very small subset of the original tile that has been cut up into smaller chunks that can be sent of the network and rendered quickly.

Is there a difference in the TileMatrix? %3A is an HTML encoding for a colon, :.What does the number after EPSG:4326 mean?

The difference is that %3A is used to encode character into a format that can be used over the internet. %3A is a : in encoding reference.
The number after the colon is the zoom level that the tile is from.