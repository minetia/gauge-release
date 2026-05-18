# Gauge 0.1.13-test-public

Published: 2026-05-18

## Changes

- Fixes loading states across the four main desktop menus.
- Ensures the full market database schema exists at app startup.
- Analysis and chart APIs lazily load live market data when the local cache is empty.
- AI reading now receives klines, market signals, OI history, and fundamental data through the desktop bridge.
- Portfolio APIs continue using local user data without opening public ports.
- Adds `GaugeUpdater.exe` for automatic updates.
- `GaugeApp.exe` checks public `latest.json` at startup.
- `GaugeApp.exe` runs a temporary updater copy before replacing installed files.
- Updater downloads `GaugeSetup.exe`, verifies SHA256, installs silently, and relaunches Gauge.
- Updater relaunches Gauge through Windows Explorer for shortcut-equivalent startup.
- Public Windows desktop installer.
- Installs `GaugeApp.exe` and `GaugeUninstall.exe`.
- Desktop shortcut points directly to `GaugeApp.exe`.
- Uninstall shortcut points directly to `GaugeUninstall.exe`.
- Removes old `Gauge.url` local-port shortcut behavior.
- Uses an internal desktop bridge instead of opening developer server ports.

## Verification

- Installed from the downloaded `GaugeSetup.exe`.
- Confirmed installed version: `0.1.13-test-public`.
- Confirmed core API checks for analysis dashboard, SMC chart, AI reading, and portfolio all return HTTP 200.
- Confirmed `GaugeApp.exe` starts from the installed shortcut path.
- Confirmed `GaugeApp.exe` does not open listening ports.

## SHA256

`4E5EFF7791824DD4331106926361180C6920521C16586D5EF156D124F43E513F`
