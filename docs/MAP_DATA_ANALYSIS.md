# Map Data Analysis

Date: 2026-09-08

## Source Reviewed

- Live site: https://wardogs-artillery.com/
- Source repository: https://github.com/apollyon-sys/wardogs-calculator

The reviewed project is an MIT-licensed open-source artillery calculator. Its own legal notes state that WARDOGS game assets, map imagery, icons, textures, logos, trademarks, names, and other third-party materials are not covered by the MIT license.

## Practical Result

For WARDOGS Fire Coordinator, it is safe to use the publicly visible coordinate model and reference ballistic data with attribution. It is not a good idea to copy the actual map imagery/tiles into this repository without separate permission or a clear asset license.

## Coordinate Model

- One coordinate unit equals 100 m.
- Azimuth uses 0 degrees north, 90 degrees east, 180 degrees south, and 270 degrees west.
- Distance is calculated from coordinate deltas with Euclidean distance.

## Available Map Metadata

The source project currently exposes two map presets:

| Map | Width | Height | Bounds X | Bounds Y |
| --- | ---: | ---: | --- | --- |
| Bakurani | 16 km | 16 km | 23.35 to 133.60 | 19.34 to 129.65 |
| Ozeti | 32 km | 32 km | 57.58 to 143.07 | 21.81 to 99.56 |

Both maps use:

- coordinateMetersPerUnit: 100
- tileSize: 256
- minZoom: 0
- maxZoom: 7
- tile extension: webp

The tile pyramids are publicly served by the original project, but the map imagery should be treated as third-party game-related material, not as MIT-licensed source code.

## Implementation Recommendation

For this project:

1. Keep the current manual coordinate workflow as the main app.
2. Store map metadata separately in `data/map-metadata.json`.
3. Do not bundle third-party map imagery.
4. If a map view is added later, either:
   - ask the original maintainer for permission,
   - use user-provided map images,
   - or link out to the existing map tool instead of copying its tiles.
