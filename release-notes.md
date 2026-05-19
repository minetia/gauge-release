# Gauge 0.1.26-test-public

Published: 2026-05-19

## Changes

- Added background 2022 history prefetch for 15M, 30M, 1H, 4H, 1D, weekly, and monthly charts.
- Kept first chart render fast by loading only the recent window first.
- Added 1,000-row older candle page loading when the user scrolls left into older chart history.
- Added `/api/history_prefetch` to the web, market-read, and external servers.
- Kept `end_time` chunk loading so repeated historical views come from local DB cache instead of repeatedly fetching the same remote data.
- Updated the public test installer and desktop executables to 0.1.26.

## Verification

- Verified `btc_chart.html` inline scripts compile.
- Verified Python server files compile without writing pycache.
- Verified `/api/klines/1h?limit=1200` returns 1,200 rows.
- Verified `/api/klines/1h?limit=1000&end_time=1700000000000` returns 1,000 older rows.
- Verified `/api/history_prefetch?intervals=1M` responds.
- Rebuilt `GaugeSetup.exe` locally.
- Verified `latest.json` hash and size match the setup file.

## SHA256

`A11C204901B1FC62DA16998EB4DC1200890A3F49C63A21E616C9DC1D2DEC4FD9`
