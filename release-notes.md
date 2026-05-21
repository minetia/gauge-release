# Gauge 0.1.28-test-public

Published: 2026-05-21

## Changes

- Applied the Accuracy First Follow Rule to AI Reading auto trading.
- The selected timeframe recalculates the current accuracy-ranked first indicator on every cycle.
- If the current first indicator direction matches the open position, Gauge records `rule_ok` and keeps the position.
- If the current first indicator direction is opposite, Gauge records `rule_reverse_detected`, saves `규칙청산`, then opens the new direction with `규칙진입`.
- Applied the same rule wording and DB event snapshots to the background auto-follow engine.
- Added the current rule to the Explanation menu through shared `activeRule` documentation data.
- Kept the build unsigned by using the existing `-AllowUnsigned` flow.

## Verification

- `node --check gauge_auto_follow_engine.js`
- `node E:\\tmp\\gauge_check\\check_html_batch.cjs ai_trading.html explanation.html indicator_analysis.html`
- `python -m py_compile gauge_app.py gauge_installer.py gauge_updater.py btc_db\\collector.py btc_db\\internal_server.py`
- `node tests\\gauge_indicator_follow.test.js`
- Rebuilt `GaugeSetup.exe` locally with version `0.1.28-test-public`.
- Installed the build locally and verified `C:\\Users\\loves\\AppData\\Local\\Gauge\\VERSION.txt` is `0.1.28-test-public`.
- Verified installed runtime files contain `accuracy-first-follow`, `현재 정확도 1등 재계산`, and `정확도 1등 반복 추종`.
- Verified `latest.json` hash and size match the setup file.

## SHA256

`CD802EF7C790081B51B6812AEDB03A34FF46A40A7C6B24D66BE53C55A3BC7053`
