qleaflet
========

Quick "plug-and-play" implementation of leaflet.js as a jquery plugin.
Multiple map tile providers can be used, e.g. cloud layer with normal map.
Provider format is taken from https://github.com/leaflet-extras/leaflet-providers/blob/master/leaflet-providers.js.
Dynamically loads leaflet js and css.


## Usage Example
```
<div data-center="48.882780,12.128906" class="mymap"></div>
```
```
<div data-markerpos="48.882780,12.128906" data-markertext="My Markertext" class="mymap"></div>
```
```
$('.mymap').qleaflet();
```

## Advanced Options
```
providers: [{
  providerName: 'OpenStreetMap',
  variantName: false
}],
leafletJsUri    : '/js/leaflet.js',
leafletCssUri   : '/css/leaflet.css',
leafletImageUri : '/img/leaflet/',
retina          : true,
markers         : [],
mapOptions: {
    center: [48.882780,12.128906],
    zoom: 17,
    scrollWheelZoom : false
  }
```
## Advanced Example
```
$('.mymap').qleaflet({
  providers: [{
    providerName: 'MapQuestOpen',
    variantName: 'Aerial'
  }],
  leafletJsUri : '/javascripts/myfolder/leaflet.js',
  retina : false
});
```
