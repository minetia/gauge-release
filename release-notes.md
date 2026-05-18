# Gauge 0.1.11-test-public

Published: 2026-05-18

## Changes

- Adds `GaugeUpdater.exe` for automatic updates.
- `GaugeApp.exe` checks public `latest.json` at startup.
- Updater downloads `GaugeSetup.exe`, verifies SHA256, installs silently, and relaunches Gauge.
- Public Windows desktop installer.
- Installs `GaugeApp.exe` and `GaugeUninstall.exe`.
- Desktop shortcut points directly to `GaugeApp.exe`.
- Uninstall shortcut points directly to `GaugeUninstall.exe`.
- Removes old `Gauge.url` local-port shortcut behavior.
- Uses an internal desktop bridge instead of opening developer server ports.

## Verification

- Installed from the downloaded `GaugeSetup.exe`.
- Confirmed installed version: `0.1.11-test-public`.
- Confirmed `GaugeApp.exe` starts from the installed shortcut path.
- Confirmed `GaugeApp.exe` does not open listening ports.

## SHA256

`1FB61E5AB082D598ACB4D75A94F1DB2BF026079B7C629ABBF6CBEE02EE2154DB`
