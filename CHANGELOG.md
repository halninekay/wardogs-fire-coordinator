# Changelog

## v0.10.0 beta - 2026-09-08

- Replaced the small L81 calibration subset with the full reference ballistic table.
- Added SPH-2 LOW/HIGH MIL output from reference ballistic tables.
- Updated weapon ranges to match the reference data:
  - Mortar: 132-684 m
  - SPH-2: 780-2629 m
- Added attribution for MIT-licensed reference ballistic table data.

## v0.9.0 beta - 2026-09-07

- Added Progressive Web App support.
- Added web app manifest.
- Added service worker for offline app shell caching.
- Added app icons.
- Added mobile web app metadata for installable behavior.
- Updated project version from v0.8.0 beta to v0.9.0 beta.

## v0.8.0 beta - 2026-09-06

- Renamed the project to WARDOGS Fire Coordinator.
- Added WARDOGS-inspired industrial UI theme.
- Added second-screen monitor layout.
- Added Compact mode.
- Added FDC mode.
- Added fullscreen control.
- Added visible version badge.
- Added copyright notice for halninekay.
- Converted the monitor app UI to English.
- Fixed vector preview scaling so the range circle stays round.
- Matched SPH-2 output behavior to the reference calculator.
- Added L81 reference calibration points:
  - 263 m = 725 mil
  - 275 m = 715 mil
  - 509 m = 450 mil

## Early prototype

- Built first single-file manual calculator.
- Added L81 and SPH-2 weapon selection.
- Added range, bearing, direction, delta-grid, and range-status outputs.
- Added compact coordinate stepper controls.
