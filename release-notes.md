# Gauge 0.1.18-test-public

Published: 2026-05-19

## Changes

- Stabilized the live BTC price block width so `$76,xxx / USDT / change` no longer moves left and right.
- Removed the visual flash animation from the live price number.
- Stopped transient WebSocket errors from replacing the realtime status with `오류`.
- Kept the realtime dot solid instead of blinking.
- Kept the 0.1.17 AI reading embedded chart iframe fix.

## Verification

- Built `GaugeSetup.exe` locally.
- Installed the generated setup file.
- Verified installed version: `0.1.18-test-public`.
- Opened the installed desktop app and checked the AI reading chart screen.
- Confirmed the installed runtime contains the fixed `last-upd` and WebSocket error handling code.

## SHA256

`BEAC606D93D347E3C37BC1CE8E2732726A44E6F9AF9A66DCAF91EA4A3A07C58D`
