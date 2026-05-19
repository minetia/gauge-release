# Gauge 0.1.24-test-public

Published: 2026-05-19

## Changes

- Fixed 1H chart candle separation caused by realtime WebSocket candles updating the chart without updating the underlying `rawData` candle array.
- Added realtime gap detection: if a live candle is more than one timeframe ahead of the loaded DB candles, Gauge reloads the timeframe instead of drawing an isolated live candle.
- Expanded full SMC chart history limits so 1H can load back to 2022 when data exists.
- Added automatic 1H history backfill to the web, market-read, and external API servers when a large 1H range is requested and local DB history is not deep enough.
- Updated the public test installer and desktop executables to 0.1.24.

## Verification

- Verified current local 1H DB range: 2022-01-01 00:00 UTC through 2026-05-19 11:00 UTC.
- Verified modified market-read server returns 38,387 1H rows for a 40,000-row request.
- Verified `btc_chart.html` inline scripts compile.
- Verified Python server files compile with `py_compile`.
- Rebuilt `GaugeSetup.exe` locally.
- Verified `latest.json` hash and size match the setup file.

## SHA256

`F7D8B6ED998B5D79C48B0C2BF3BA77EAE3307F5948F70567D664375A7E446BF3`
