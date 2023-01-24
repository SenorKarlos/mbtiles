# Full Planet MBTiles

This is the whole planet, ~72GB download, conveniently named for use with a default [SwiftTileServer](https://github.com/123FLO321/SwiftTileserverCache) install. I cannot currently find a way to cURL or wget this properly, let me know if anyone knows a way.

I will likely be redoing this once a month or so, last run date:

2023/01/23 - https://1drv.ms/u/s!AsKn69WQVywljRdP0tK3onKe8NX5

# Regional Files

If you want to use a smaller extract with your tileserver, you can use a node utility called tilelive-copy. The following is from the repo used to create the mbtiles, use whatever applies for your environment:
```
# install node and tilelive-copy
curl -fsSL https://deb.nodesource.com/setup_16.x | sudo -E bash -
apt-get install -y nodejs
npm install -g @mapbox/tilelive @mapbox/mbtiles
# Extract z0-4 for the world
tilelive-copy --minzoom=0 --maxzoom=4 --bounds=-180,-90,180,90 output.mbtiles demo.mbtiles
# Extract z0-14 for just southern New England
tilelive-copy --minzoom=0 --maxzoom=14 --bounds=-73.6346,41.1055,-69.5464,42.9439 output.mbtiles demo.mbtiles
```

# Credits

planetiler - https://github.com/onthegomap/planetiler
OpenStreetMap - https://openstreetmap.org
SwiftTileServerCache/tileserver-gl - https://github.com/123FLO321/SwiftTileserverCache
