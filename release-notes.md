# Gauge 0.1.14-test-public

Published: 2026-05-18

## Changes

- Initial chart indicators now reset once to the six public defaults shown in the reference screen: EMA, BB, RSI, OB, ZONES, and WALLS.
- AI reading avoids duplicate concurrent signal loads.
- AI reading requests 220 candles instead of 250 while keeping EMA 200 calculations available.
- Kline requests are cached for 30 seconds inside the page to reduce repeated menu and preset loading.
- Fundamental data refresh runs after the first signal render instead of blocking the first AI reading screen.
- Empty fundamental data collection now starts in the background and returns immediately.
- The desktop bridge preloads internal Flask test clients in the background so the first menu API call is faster.
- The installer removes stale runtime HTML/JS before installing an update.
- Version bumped to `0.1.14-test-public`.

## Verification

- Installed from `E:\gauge\dist\GaugeSetup.exe`.
- Confirmed installed version: `0.1.14-test-public`.
- Confirmed installed runtime regenerates with the new six-indicator defaults and AI reading optimization code.
- Confirmed Gauge runs as a desktop app without listening ports.
- Confirmed AI reading bridge checks return HTTP 200.
- Direct uninstaller tests passed.

## SHA256

`4DF06DDFC6710A47CBC2316F6AE29CACB724EDD9434C60CB9725689C42D36795`
