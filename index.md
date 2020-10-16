<html>

<head>
  <title>Studio Week 2</title>
  <!-- Adding in the Leaflet CSS file -->
  <link rel="stylesheet" href="https://unpkg.com/leaflet@1.6.0/dist/leaflet.css" />
  <!-- Adding Leaflet JavaScript file -->
  <script src="https://unpkg.com/leaflet@1.6.0/dist/leaflet.js"></script>
  <!-- Adding styling info for the map -->
  <style type="text/css">
  #mapId {
     height: 600px;
   }
	  a:link {
  color: green;
  background-color: transparent;
  text-decoration: none;
}

a:visited {
  color: yellow;
  background-color: transparent;
  text-decoration: none;
}

a:hover {
  color: red;
  background-color: transparent;
  text-decoration: underline;
}

a:active {
  color: yellow;
  background-color: transparent;
  text-decoration: underline;
}
    /* Add a CSS rule that selects an element with the ID "mapId" and gives it a height of 600 pixels */
  </style>
  <!-- Adding styling info for page layout by reading in a CSS file -->
  <link rel="stylesheet" href="styles.css">
</head>

<body>
  <h1 style="font-family:'Courier New'">Arpan's Studio Week 2 submission</h1>
  <!-- Add multiple pages to web page-->
  <!-- active class displays the grey box around current page-->
  <ul>
  	<li><a class="active" href="index.html" target="_self">Output 1</a></li>
    <li><a href="Mapbox-gl-js-cwm.html" target="_self">Output 2</a></li>
    <li><a href="Mapbox-gl-js-ct.html" target="_self">Output 3</a></li>
    <li><a href="Mapbox-gl-js-bm.html" target="_self">Output 4</a></li>
  </ul>
  <br>

  <!-- Add a div with id="mapId" to give the map somewhere to go -->
  <div id="mapId"></div>
  <script>
    // Create a variable called "map" to house your Leaflet map and all of its functionality
    var map = L.map('mapId').setView([37.754700, -122.420790], 14);
    /* 
     * Use Leaflet's tileLayer method to create a new tile layer, then add it to the map 
     ** Reference: https://leafletjs.com/reference-1.6.0.html#tilelayer
     */ 
  var OpenStreetMap_HOT = L.tileLayer('https://{s}.tile.openstreetmap.fr/hot/{z}/{x}/{y}.png', {
	maxZoom: 19,
	attribution: '&copy; <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a> contributors, Tiles style by <a href="https://www.hotosm.org/" target="_blank">Humanitarian OpenStreetMap Team</a> hosted by <a href="https://openstreetmap.fr/" target="_blank">OpenStreetMap France</a>'
}).addTo(map);
    /* Try changing out the tile source for something else. Hint: you can find 
     * lots of tile sources here: https://leaflet-extras.github.io/leaflet-providers/preview/ 
     */
      L.tileLayer('https://{s}.tile.opentopomap.org/{z}/{x}/{y}.png', {
	maxZoom: 17,
	attribution: 'Map data: &copy; <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a> contributors, <a href="http://viewfinderpanoramas.org">SRTM</a> | Map style: &copy; <a href="https://opentopomap.org">OpenTopoMap</a> (<a href="https://creativecommons.org/licenses/by-sa/3.0/">CC-BY-SA</a>)'
}).addTo(map);
    

  </script>
</body>

</html>
