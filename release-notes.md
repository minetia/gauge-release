# Gauge 0.1.29-test-public

Published: 2026-05-21

## Changes

- Added live lag correction to the Accuracy First Follow Rule.
- If the current accuracy-ranked first indicator value and live price move together in the opposite direction, Gauge records a `실시간 지연보정` reason and can react before the selected timeframe candle fully flips.
- Prevented `gauge_auto_follow_engine.js` from running inside iframes, so AI Reading's embedded chart cannot run a second trading engine.
- Kept AI Reading as the single trading authority while the AI Reading page is open.
- Updated version constants to `0.1.29-test-public`.

## Verification

- `node --check gauge_auto_follow_engine.js`
- `node E:\\tmp\\gauge_check\\check_html_batch.cjs ai_trading.html explanation.html`
- `python -m py_compile gauge_app.py gauge_installer.py gauge_updater.py`
- Rebuilt unsigned installer with `-AllowUnsigned`.
- Installed locally and verified `C:\\Users\\loves\\AppData\\Local\\Gauge\\VERSION.txt` is `0.1.29-test-public`.
- Verified installed runtime files contain `실시간 지연보정`, `liveOverride`, and iframe engine blocking.
- Verified `latest.json` hash and size match the setup file.

## SHA256

`3A60DD8838E42E45CDD800868A18FA68B61696A885A3B1E5B23F285C92446943`
