# Stamp data

Map data that the [Stamp](https://github.com/marcusbandit/stamp) app downloads when it needs it.

## Rail and road packs

`routes/v1/<CC>.bin.gz` holds one country's main railways and big roads, keyed by its ISO
3166-1 alpha-2 code. The app downloads a country's pack when a trip there has a leg by train,
car or bus, so the leg can follow the real line instead of a straight one.

Each pack keeps `railway=rail` (no sidings, yards or spurs) and `highway=motorway`, `trunk` and
their links. Ways are cut at junctions and simplified to about 30 m. The format and the builder
are in Stamp's [`tools/build_routes.py`](https://github.com/marcusbandit/stamp/blob/main/tools/build_routes.py).

## Licence

The packs are a derived database of OpenStreetMap data, © OpenStreetMap contributors, and are
available under the [Open Database License 1.0](https://opendatacommons.org/licenses/odbl/1-0/).
The extracts they are built from come from [Geofabrik](https://download.geofabrik.de/).
