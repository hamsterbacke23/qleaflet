qleaflet
========

Quick "plug-and-play" implementation of leaflet.js as a jquery plugin. 
* Mobile use: Maps are responsive, leaflet.js also allows for touch events.
* Multiple map tile providers can be used, e.g. cloud layer with normal map.
* Adding map providers: Provider format is taken from https://github.com/leaflet-extras/leaflet-providers/blob/master/leaflet-providers.js.
* Dynamically "lazy-loads" leaflet js and css via CDN or if you want locally.

## Demo
http://codepen.io/anon/pen/KchJa (not neccessarily up to date)

## Usage 
include qleaflet.jquery.js in website
```
<script src="/js/qleaflet.jquery.js"></script>
```
Then:
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
  providerName: 'MapQuestOpen',
  variantName: false
}],
leafletJsUri    : 'http://cdn.leafletjs.com/leaflet-0.6.4/leaflet.js',
leafletCssUri   : 'http://cdn.leafletjs.com/leaflet-0.6.4/leaflet.css',
leafletImageUri : false,
retina          : true,
markers         : [],
mapOptions: {
  center: [48.882780,12.128906],
  zoom: 13,
  scrollWheelZoom : false
  //  ... more leaflet.js options ...
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
