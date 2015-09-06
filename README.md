GeoTools
========

A useful collection of Geotools. The module uses in most cases promises.

Usage:
-----
####Using FreegeoIP to get users geolocation without device functionality:####

```javascript

var GooGeoTools = require('de.appwerft.googeotools');

GooGeoTools.getPositionByIP(null).then(function(_res){
    console.log(_res);
});

```

####Retreiving region (for Ti.Map) by country:###

```javascript

var GooGeoTools = require('de.appwerft.googeotools');

GooGeoTools.getRegionByCountry('Poland').then(function(_res){
    console.log(_res);
});
```

####Retreiving elevation by position:###

```javascript

var GooGeoTools = require('de.appwerft.googeotools');

GooGeoTools.getElevationByPosition({lat:53.5,lon:10}).then(function(_res){
    console.log(_res);
});
```



####Retreiving route from source to destination, gives you list af legs and polyline for Ti.Map####

```javascript

var GooGeoTools = require('de.appwerft.googeotools');

GooGeoTools.getRoute({lat:53.5,lon:10},{lat:55,lon:8}).then(function(_res){
    console.log(_res);
});
```

####Calculating distance between two points on earth####

```javascript

var GooGeoTools = require('de.appwerft.googeotools');

var res = GooGeoTools.getDistance({lat:53.5,lon:10},{lat:55,lon:8});
console.log(res);

```

####Calculating bearing between two points on earth####

```javascript

var GooGeoTools = require('de.appwerft.googeotools');

var res = GooGeoTools.getBearing({lat:53.5,lon:10},{lat:55,lon:8});
console.log(res);

```


