# Gauge 0.1.27-test-public

Published: 2026-05-19

## Changes

- Corrected indicator analysis from future-direction prediction accuracy to same-time candle alignment accuracy.
- The top-ranked indicator is now the one whose LONG/SHORT direction most closely matches the candle's own up/down movement.
- Clarified UI labels: `지표 LONG=캔들 LONG`, `지표 SHORT=캔들 SHORT`, and `같은 시점 캔들`.
- Recent direction changes now explicitly show both `지표 LONG/SHORT` and the same-time `캔들 LONG/SHORT`.
- Updated the public test installer and desktop executables to 0.1.27.

## Verification

- Verified `indicator_analysis.html` inline scripts compile.
- Verified `btc_chart.html` inline scripts still compile.
- Verified version constants are 0.1.27.
- Rebuilt `GaugeSetup.exe` locally.
- Verified `latest.json` hash and size match the setup file.

## SHA256

`9F9A42E832E4EDE6D2E710B0B4EFFEE02B574B474EE4EB0C1ADD0C82F2634366`
