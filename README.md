# mapas

link to site: https://pbenavidesec.github.io/mapas/

Explore this data story...

<!DOCTYPE html>
<html>
  <head>
  <style>
    #map-canvas { width:400px; height:400px; }
    .layer-wizard-search-label { font-family: sans-serif };
  </style>
  <script type="text/javascript"
    src="http://maps.google.com/maps/api/js?sensor=false">
  </script>
  <script type="text/javascript">
    var map;
    var layer_0;
    var layer_1;
    function initialize() {
      map = new google.maps.Map(document.getElementById('map-canvas'), {
        center: new google.maps.LatLng(-2.1749666725072423, -79.92665048059337),
        zoom: 14
      });
      var style = [
        {
          featureType: 'all',
          elementType: 'all',
          stylers: [
            { saturation: 99 }
          ]
        },
        {
          featureType: 'administrative.province',
          elementType: 'all',
          stylers: [
            { visibility: 'off' }
          ]
        },
        {
          featureType: 'administrative.locality',
          elementType: 'all',
          stylers: [
            { visibility: 'off' }
          ]
        },
        {
          featureType: 'administrative.neighborhood',
          elementType: 'all',
          stylers: [
            { visibility: 'off' }
          ]
        }
      ];
      var styledMapType = new google.maps.StyledMapType(style, {
        map: map,
        name: 'Styled Map'
      });
      map.mapTypes.set('map-style', styledMapType);
      map.setMapTypeId('map-style');
      layer_0 = new google.maps.FusionTablesLayer({
        query: {
          select: "col2",
          from: "1S2MoR-NDMzItkvJzqVd4mRkNHpLgBQi8RcjBkc4k"
        },
        map: map,
        styleId: 2,
        templateId: 2
      });
      layer_1 = new google.maps.FusionTablesLayer({
        query: {
          select: "col3",
          from: "1__ozaR0RF6ehVld5_G3C9O143NaXyl_hlGrmskfG"
        },
        map: map,
        styleId: 2,
        templateId: 2
      });
    }
    google.maps.event.addDomListener(window, 'load', initialize);
  </script>
  </head>
  <body>
    <div id="map-canvas"></div>
  </body>
</html>
