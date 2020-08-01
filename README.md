# maps

## is何？

マップの置き場

## geojson to pbf

https://github.com/mapbox/tippecanoe

```bash
# install tippecanoe
brew install tippecanoe

# run convert
tippecanoe -e world -z 5 --no-tile-compression ./geojson_world/map.geojson
```

## SOURCE

- https://www.naturalearthdata.com/
- https://github.com/weatherbox/warning-area-vt
