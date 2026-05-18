# Gauge 0.1.12-test-public

Published: 2026-05-18

## Changes

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
- Confirmed installed version: `0.1.12-test-public`.
- Confirmed `GaugeApp.exe` starts from the installed shortcut path.
- Confirmed `GaugeApp.exe` does not open listening ports.

## SHA256

`47F64B27A12B820F8A8F02F8D957620DEFE63EDDF66573D4664ABABBB1CA3C5A`
