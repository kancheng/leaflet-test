# leaflet-test
Test leaflet &amp; Map

詳見 index.html

當中匯入 `leaflet.css` & `leaflet.js` ，使用 OpenStreetMap。

## Demo

https://codemercs.github.io/page/leaflet-test/


## CSS

```
<link rel="stylesheet" href="leaflet.css" crossorigin=""/>
```

## JS

```
<script src="leaflet.js" crossorigin=""></script>
```

## index.html

```
<!DOCTYPE html>
<html>
<head>
    <title>OX</title>
    <meta charset="utf-8" />
    <link rel="stylesheet" href="leaflet.css"
    crossorigin=""/>
    <script src="leaflet.js"
    crossorigin=""></script>

</head>
<body>

    <div id="mapid" style="width: 600px; height: 600px;"></div>
    <script>
        var mymap = L.map('mapid').setView([25.041723, 121.550367], 17);
        L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
            maxZoom: 20,
            attribution: '&copy; <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a> contributors'
        }).addTo(mymap);
    
        L.marker([25.041723, 121.550367]).addTo(mymap)
            .bindPopup("<b>Hello world!</b><br />OxBridge Consulting Inc. ").openPopup();

        </script>
</body>
</html>

```
