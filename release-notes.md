# Gauge 0.1.25-test-public

Published: 2026-05-19

## Changes

- Fixed slow 1H SMC chart startup by removing the accidental 40,000-candle default load.
- Changed full chart defaults so 1H starts with 1,200 recent candles instead of loading years of data at once.
- Added `end_time`/`before` support to the web, market-read, and external kline APIs so older history can be loaded in small chunks.
- Raised automatic 1H deep-history backfill threshold to large explicit requests only, preventing normal chart clicks from triggering heavy backfill work.
- Added no-cache headers for HTML, JS, and CSS responses so installed WebView screens pick up updated chart code.
- Updated the public test installer and desktop executables to 0.1.25.

## Verification

- Verified `btc_chart.html` inline scripts compile.
- Verified Python files compile without writing pycache.
- Verified web `/api/klines/1h?limit=1200` returns 1,200 rows in 30.6 ms with Flask test client.
- Verified web `/api/klines/1h?limit=1000&end_time=1700000000000` returns 1,000 older rows in 38.2 ms.
- Verified market-read `/api/klines/1h?limit=1200` returns 1,200 rows in 11.0 ms.
- Rebuilt `GaugeSetup.exe` locally.
- Verified `latest.json` hash and size match the setup file.

## SHA256

`7628BA3D77735ED28CB1117FE4F720289A8BFEE4E4B4E266119BAFBAEE684535`
