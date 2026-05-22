# Gauge 0.1.34-test-public

- 자동모드 보호청산 리스크 관리자 복구.
- SL, TP, 트레일링, 리스크 손실제한/수익보호 청산을 포지션 보호 전용으로 다시 활성화.
- 보호청산 후 현재 선택 시간봉 캔들에 isk_closed를 저장해 같은 캔들 재진입을 금지.
- DB에 포지션이 이미 없으면 화면 포지션을 비우고 반전 청산 경합을 중단.
- uto_monitor_events에 uto_protection_reentry_block, ule_wait_after_protection_close 이벤트 저장.
- 설명 메뉴와 규칙 문서를 보호청산 복구 기준으로 갱신.

SHA256: 8C4F33E551EC0CA3870A60B7E4D442D9F26D8365A2C304F8F384A7E57103D12F
SIZE: 72987415 bytes
