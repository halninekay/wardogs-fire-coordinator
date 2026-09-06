# WARDOGS Fire Coordinator

**Version:** v0.8.0 beta  
**Copyright:** Copyright (c) 2026 halninekay

WARDOGS Fire Coordinator is a lightweight browser-based artillery coordination tool for WARDOGS. It helps players request or coordinate indirect fire by entering manual grid coordinates and reading a fast firing solution.

The app is built as a single static HTML file. No account, server, build step, or external dependency is required.

## Features

- Manual firing-position and target-position coordinate input
- L81 Mortar support, effective range 120-700 m
- SPH-2 Artillery support, effective range 735-2630 m
- Range calculation based on a 100 m grid
- Bearing and cardinal direction output
- L81 elevation estimate based on current reference calibration points
- SPH-2 weapon/range/bearing/direction workflow
- Compact coordinate stepper buttons
- Second-screen monitor layout
- Compact mode
- FDC mode for large readouts
- Fullscreen button

## Current Calibration

L81 elevation currently uses these reference points:

| Range | Elevation |
| ---: | ---: |
| 263 m | 725 mil |
| 275 m | 715 mil |
| 509 m | 450 mil |

Values outside the confirmed points are interpolated or extrapolated and should be treated as beta until more in-game or reference-calculator data is collected.

## Usage

Open `index.html` in any modern browser.

1. Select the weapon system.
2. Enter the firing-position X/Y coordinates.
3. Enter the target-position X/Y coordinates.
4. Read range, bearing, direction, and elevation or weapon solution.

## Status

This project is currently marked as **v0.8.0 beta**.

Range, bearing, direction, and SPH-2 behavior are stable against the available reference values. L81 elevation is useful, but still needs more calibration points before a v1.0 release.

## Disclaimer

This is an unofficial fan-made utility for WARDOGS. It is not affiliated with, endorsed by, or sponsored by the WARDOGS developers or publishers.
