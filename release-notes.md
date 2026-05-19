# Gauge 0.1.21-test-public

Published: 2026-05-19

## Changes

- Fixed AI reading timeframe loading for 15M through monthly views.
- Added stale local DB detection and Binance refresh before chart data is returned.
- Fixed disconnected realtime candle display caused by old desktop-local klines.
- Updated the public test installer and desktop executables to 0.1.21.

## Verification

- Built `GaugeSetup.exe` locally.
- Verified local desktop DB 15M candles now run through `2026-05-19 17:15` with gap count 0.
- Opened the rebuilt desktop app and confirmed the chart no longer shows disconnected candles after data refresh.
- Verified `latest.json` hash matches the uploaded setup file.

## SHA256

`15D2FFA9B5198CCA03BB649225BBEF0B7C0948F5C9C52D1924E4B993838629C0`
