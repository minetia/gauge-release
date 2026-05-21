# Gauge 0.1.32-test-public

Published: 2026-05-21

## Changes

- Added Telegram notifications for important Gauge trading events.
- Sends notifications for entries, closes, reversals, risk exits, reentry locks, reentry blocks, unlocks, failed entries, warnings, and errors.
- Stores Telegram credentials only in local configuration or environment variables, not in Git.
- Desktop internal API and local internal server both send notifications after DB save succeeds.
- Default spam protection avoids sending repeated `rule_ok` hold events every 15 seconds.

## Verification

- Telegram local configuration was loaded successfully.
- Test message was sent successfully.
- Repository scan confirmed the bot token and chat id are not stored in committed files.
- `python -m py_compile telegram_notify.py gauge_app.py gauge_installer.py gauge_updater.py btc_db\\internal_server.py`
- `node E:\\tmp\\gauge_check\\check_html_batch.cjs ai_trading.html explanation.html`
- `node --check gauge_auto_follow_engine.js`
- Rebuilt unsigned installer with `-AllowUnsigned`.
- Installed locally and verified `C:\\Users\\loves\\AppData\\Local\\Gauge\\VERSION.txt` is `0.1.32-test-public`.

## SHA256

`1C5C81B3DC5D3E1B5138760FF7B0EA7BFCCE66168D734E446C67D3672AA36EA6`
