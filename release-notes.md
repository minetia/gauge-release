# Gauge 0.1.30-test-public

Published: 2026-05-21

## Changes

- Added the Risk Manager Rule to AI Reading auto mode.
- Entry, hold, and reversal direction still follow the Accuracy First Follow Rule.
- The risk manager only closes positions; it never decides a new LONG/SHORT entry.
- Profit protection arms after net profit reaches the configured threshold, then closes if gains are given back too far.
- Hard-loss protection closes if net loss reaches the configured threshold.
- Risk exits save `리스크청산` reasons and `risk_manager_*` monitor events.
- Explanation menu now shows the risk manager rule from shared docs data.

## Verification

- `node E:\\tmp\\gauge_check\\check_html_batch.cjs ai_trading.html explanation.html`
- `node --check gauge_auto_follow_engine.js`
- `python -m py_compile gauge_app.py gauge_installer.py gauge_updater.py`
- Rebuilt unsigned installer with `-AllowUnsigned`.
- Installed locally and verified `C:\\Users\\loves\\AppData\\Local\\Gauge\\VERSION.txt` is `0.1.30-test-public`.
- Verified installed runtime files contain `RISK_MANAGER`, `리스크청산`, `risk-manager`, and `risk_manager_profit_protect`.
- Verified `latest.json` hash and size match the setup file.

## SHA256

`CE2DE86AB975DFFCB43E444CAEC60B7515DE8D155341BF50568AF632F05BEDD6`
