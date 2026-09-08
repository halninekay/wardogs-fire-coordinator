# WARDOGS Fire Coordinator

**Version:** v0.10.0 beta  
**Copyright:** Copyright (c) 2026 halninekay

WARDOGS Fire Coordinator is a lightweight browser-based artillery coordination tool for WARDOGS. It helps players request or coordinate indirect fire by entering manual grid coordinates and reading a fast firing solution.

The app is built as a single static HTML file. No account, server, build step, or external dependency is required.

## Features

- Manual firing-position and target-position coordinate input
- L81 Mortar support, effective range 120-700 m
- SPH-2 Artillery support, effective range 735-2630 m
- Range calculation based on a 100 m grid
- Bearing and cardinal direction output
- L81 MIL output from a reference ballistic table
- SPH-2 LOW/HIGH MIL output from reference ballistic tables
- Compact coordinate stepper buttons
- Second-screen monitor layout
- Compact mode
- FDC mode for large readouts
- Fullscreen button
- Progressive Web App support
- Offline app shell after first load
- Installable on supported mobile and desktop browsers

## Ballistic Tables

The calculator now uses reference ballistic tables for supported weapons.

Values are interpolated between known distance/MIL entries. The app remains beta because the tables may still need validation against live game behavior after WARDOGS updates.

## Usage

Open `index.html` in any modern browser.

1. Select the weapon system.
2. Enter the firing-position X/Y coordinates.
3. Enter the target-position X/Y coordinates.
4. Read range, bearing, direction, and elevation or weapon solution.

## Install as App

When hosted through GitHub Pages or another HTTPS host, the tool can be installed as a Progressive Web App.

On Android/Chrome:

1. Open the hosted app URL.
2. Open the browser menu.
3. Choose **Install app** or **Add to Home screen**.

On iPhone/Safari:

1. Open the hosted app URL.
2. Tap **Share**.
3. Choose **Add to Home Screen**.

## Status

This project is currently marked as **v0.10.0 beta**.

Range, bearing, direction, L81 MIL, and SPH-2 LOW/HIGH MIL are based on reference ballistic tables. The app should still be treated as beta until it has more live-game validation.

## Attribution

Reference ballistic table data is derived from the MIT-licensed WARDOGS Artillery Calculator project by Apollyon:

https://github.com/apollyon-sys/wardogs-calculator

WARDOGS game assets, names, trademarks, and map imagery remain the property of their respective owners and are not included in this project.

## Disclaimer

This is an unofficial fan-made utility for WARDOGS. It is not affiliated with, endorsed by, or sponsored by the WARDOGS developers or publishers.
