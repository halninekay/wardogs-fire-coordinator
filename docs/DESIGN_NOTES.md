# WARDOGS Fire Coordinator Design Notes

Date: 2026-09-06  
Current monitor version: `v0.9.0 beta`

## Purpose

WARDOGS Fire Coordinator is a small manual artillery request and indirect-fire tool for WARDOGS. It is designed for fast second-screen use: enter manual coordinates, select a weapon, and read the firing solution at a glance.

## Current State

- Main app file: `index.html`
- PWA manifest: `manifest.webmanifest`
- Offline worker: `service-worker.js`
- App icons: `icons/`
- Product name: WARDOGS Fire Coordinator
- Copyright: Copyright (c) 2026 halninekay
- Two supported weapon systems:
  - L81 Mortar, effective range 120-700 m
  - SPH-2 Artillery, effective range 735-2630 m
- One grid square equals 100 m.
- Manual firing-position and target-position X/Y input.
- Compact up/down controls on every coordinate field.
- Automatic calculation:
  - range
  - bearing
  - cardinal direction
  - delta grid
  - range status
- SPH-2 displays range, bearing, direction, and weapon.
- L81 also displays estimated mortar elevation.
- Installable PWA behavior is available when hosted over HTTPS.

## L81 Calibration Points

Current reference values:

- 263 m = 725 mil
- 275 m = 715 mil
- 509 m = 450 mil

More calibration points can improve the curve later, especially below 263 m and above 509 m.

## Verified Cases

- L81: `109.11 / 96.67` to `107.36 / 94.71`
  - 263 m
  - 222 degrees
  - SW
  - 725 mil
- L81: `109.25 / 96.71` to `107.36 / 94.71`
  - 275 m
  - 223 degrees
  - SW
  - 715 mil
- L81: `42.6 / 18.2` to `46.1 / 21.9`
  - 509 m
  - 043 degrees
  - NE
  - 450 mil
- SPH-2: `109.25 / 96.71` to `107.36 / 80.71`
  - 1611 m
  - 187 degrees
  - S
  - weapon SPH-2

## Versioning

The current monitor build is labeled `v0.9.0 beta`.

Development milestones counted so far:

1. First manual HTML prototype with L81/SPH-2, range, bearing, and placeholder elevation.
2. L81 reference point added: 509 m = 450 mil.
3. Bearing axis corrected.
4. L81 reference point added: 263 m = 725 mil.
5. L81 reference point added: 275 m = 715 mil.
6. Coordinate steppers changed to compact up/down controls.
7. SPH-2 output changed to weapon/range/bearing/direction behavior.
8. Monitor/second-screen UI with WARDOGS theme, English text, copyright, beta label, and round vector preview.
9. Progressive Web App support with manifest, app icons, mobile metadata, and offline app shell caching.

Why beta:

- Core range and bearing calculations are stable.
- L81 elevation is calibrated with real reference points, but not fully mapped across every distance.
- SPH-2 matches the reference-calculator behavior because it does not output elevation.

## Next Useful Steps

- Add more L81 calibration points.
- Consider a quick-copy firing-solution button.
- Consider weapon toggle buttons instead of a select menu.
- Add a public preview image for GitHub.
