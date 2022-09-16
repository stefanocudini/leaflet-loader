Leaflet Control Loader
==============

Simple control to show a gif loader to the center of the map

**demo:**

[opengeo.tech/maps/leaflet-loader](https://opengeo.tech/maps/leaflet-loader/)


![Image](https://raw.githubusercontent.com/stefanocudini/leaflet-loader/master/images/leaflet-loader-demo.jpg)


## example of usage with jquery ajax

```javascript
...
const controlLoader = L.control.loader().addTo(map);
$.ajaxSetup({
 beforeSend: e => {
    controlLoader.show()
 },
 complete: e => {
    controlLoader.hide()
 }
});
const geoLayer = L.geoJson([]).addTo(map);

$.getJSON(`mygeojson.json`, geoj => {

	geoLayer.addData(geoj);

});

```
