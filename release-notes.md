# Gauge 0.1.31-test-public

Published: 2026-05-21

## Changes

- Fixed a critical loop where risk-manager close was followed by immediate same-side reentry.
- After `리스크청산`, the closed side is locked until the accuracy-first 1st indicator flips direction once.
- Added DB monitor events: `risk_manager_reentry_lock`, `risk_manager_reentry_block`, `risk_manager_reentry_unlock`.
- Hard-loss calculation now uses the larger value between the configured seed loss and roundtrip fee plus a minimum movement buffer.
- Explanation menu and risk-manager rule document now describe the same-side reentry lock.

## Verification

- `node E:\\tmp\\gauge_check\\check_html_batch.cjs ai_trading.html explanation.html`
- `node --check gauge_auto_follow_engine.js`
- `python -m py_compile gauge_app.py gauge_installer.py gauge_updater.py`
- Rebuilt unsigned installer with `-AllowUnsigned`.
- Installed locally and verified `C:\\Users\\loves\\AppData\\Local\\Gauge\\VERSION.txt` is `0.1.31-test-public`.
- Verified installed runtime files contain `risk_manager_reentry_lock`, `risk_manager_reentry_block`, `risk_manager_reentry_unlock`, and the fee-buffered hard-loss logic.
- Verified local DB recorded `risk_manager_reentry_block` after the risk exit, stopping same-side reentry.

## SHA256

`517D497AFE640F230D4955EE17BF9011EEEFCF5D7B729D9ADC1965534259B243`
