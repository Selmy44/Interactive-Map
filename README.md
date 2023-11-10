# Interactive-Map
This is an Interactive Map web
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Map</title>
    <style>
        #map {
            height: 400px;
            width: 100%;
        }
    </style>
</head>
<body>

<div id="map"></div>

<script src="https://unpkg.com/leaflet/dist/leaflet.js"></script>

<script>
    // Initialize the map
    var map = L.map('map').setView([0, 0], 2);

    // Add a tile layer
    L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
        attribution: '© OpenStreetMap contributors'
    }).addTo(map);

    // Add a marker at a specific location
    var marker = L.marker([0, 0]).addTo(map);

    // Add a popup to the marker
    marker.bindPopup("<b>Hello!</b><br>This is an interactive map.").openPopup();
</script>

</body>
</html>
