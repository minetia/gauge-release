# Gauge 0.1.16-test-public

Published: 2026-05-19

## Changes

- AI reading embedded chart now opens as `btc_chart.html?embed=ai`.
- Embedded AI chart uses a fast mode for 15M, 30M, 1H, 4H, 1D, weekly, and monthly switching.
- Fast chart mode calculates only the public six defaults needed on the AI reading screen instead of all hidden indicators.
- Multi-timeframe AI signal loading is parallelized.
- Automatic trading state is persisted to the internal database via `trade_engine_state`.
- If the WebView window closes while auto-trading is active or a paper position is open, Gauge keeps a background trade guardian loop alive.
- The guardian loop continues paper-position SL, TP, liquidation, trailing-stop, and backend auto-trading checks.
- Installer continues clearing stale runtime files before update.

## Verification

- Built `GaugeSetup.exe` locally.
- Installed the generated setup file.
- Verified installed version: `0.1.16-test-public`.
- Verified installed AI reading runtime contains `embed=ai`.
- Verified installed chart runtime contains `FAST_AI_CHART`.
- Verified Gauge process has zero listening ports.
- Verified `trade_engine_state` API persists auto-trading state.
- Verified backend trade guard condition remains active when an open position exists.

## SHA256

`08B195DB8CD89DD4F96C6B246ECF6CD55CEB5044D526EF3FD4224A47E8445F03`
