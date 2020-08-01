# maps

## is何？

マップの置き場

## shp to geojson

- https://qiita.com/tohka383/items/d3d1bf80db2cfb416330

```bash
cd dir

docker pull osgeo/gdal:ubuntu-full-latest

docker run -v /home:[directory path] -it --rm osgeo/gdal:ubuntu-full-latest
> cd /home
> ogr2ogr -f GeoJSON [geojson file path] [shp file path]
```

## geojson to pbf

https://github.com/mapbox/tippecanoe

```bash
# install tippecanoe
brew install tippecanoe

# run convert
tippecanoe -e world -z 5 --no-tile-compression ./geojson_world/map.geojson
```

## 使用

|  ディレクトリ名  |            説明             |                                         url                                          |                                                                                       ライセンス                                                                                        |
| :--------------: | :-------------------------: | :----------------------------------------------------------------------------------: | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
|  geojson_world   |     世界地図（geojson）     |                                                                                      |                                                                [Natural Earth](https://www.naturalearthdata.com/) に帰属                                                                |
|    pbf_japan     |       日本地図（pbf）       | https://earthquake-alert.github.io/maps/pbf_japan/[distlict or pref]/{z}/{x}/{y}.pbf | [weatherbox/warning-area-vt](https://github.com/weatherbox/warning-area-vt) および、[国土地理院 行政区域データ](https://nlftp.mlit.go.jp/ksj/gml/datalist/KsjTmplt-N03-v2_3.html)に帰属 |
|  pbf_water_area  |   日本の湖沼データ（pbf）   |   https://earthquake-alert.github.io/maps/pbf_water_area/waterArea/{z}/{x}/{y}.pbf   |                                             [国土地理院 湖沼データ](https://nlftp.mlit.go.jp/ksj/gml/datalist/KsjTmplt-N03-v2_3.html)に帰属                                             |
|    pbf_world     |       世界地図（pbf）       |       https://earthquake-alert.github.io/maps/pbf_world/world/{z}/{x}/{y}.pbf        |                                                                [Natural Earth](https://www.naturalearthdata.com/) に帰属                                                                |
| water_area_japan | 日本の湖沼データ（geojson） |                                                                                      |                                             [国土地理院 湖沼データ](https://nlftp.mlit.go.jp/ksj/gml/datalist/KsjTmplt-N03-v2_3.html)に帰属                                             |

## SOURCE

- https://www.naturalearthdata.com/
- https://github.com/weatherbox/warning-area-vt
- https://nlftp.mlit.go.jp/ksj/gml/datalist/KsjTmplt-W09-v2_2.html
