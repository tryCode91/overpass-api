Download latest Sweden extract from -> http://download.geofabrik.de/europe/sweden-latest.osm.pbf

clip out vastra_gotaland or preferred region of country
osmconvert sweden.osm.pbf -B=vastra_gotaland.poly --complete-ways -o=vastra_gotaland.pbf

use osmconvert to make it into osm format
osmconvert vastra_gotaland.pbf -o=vastra_gotaland.osm

Make it into bzip2 format
bzip2 -9 vastra_gotaland.osm

Ready

3-5 can be automated to run service every x days
or not


docker compose down && docker volume rm overpass_overpass-db