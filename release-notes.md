# Gauge 0.1.22-test-public

Published: 2026-05-19

## Changes

- Added the new `지표분석` top-menu screen.
- Ranks GAUGE/SMC indicators by how accurately each LONG/SHORT signal matched the later real chart direction.
- Default analysis is 1H with 15M, 30M, 4H, 1D, weekly, and monthly controls prepared for expansion.
- Includes SMC/AI signal indicators plus chart indicators such as VWAP, Ichimoku, SAR, CCI, Williams %R, CMF, Aroon, Vortex, ROC, and Momentum.
- Updated the public test installer and desktop executables to 0.1.22.

## Verification

- Built `GaugeSetup.exe` locally.
- Verified `indicator_analysis.html` script compilation.
- Verified `http://localhost:5012/indicator_analysis.html` returns 200.
- Verified `http://localhost:5012/api/klines/1h?limit=160` returns 200.
- Ran the indicator analysis logic against live 1H API data and confirmed ranked results render.
- Verified `latest.json` hash matches the setup file.

## SHA256

`19A926D94E2169CDEE8CE3D9E82A5EAB587114978839C9BDC490844F58E86D23`
