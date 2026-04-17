# Risk Register - Commands Not Executed
## AP5010U-WW | IQ Engine 10.8r5

**Generated:** 2026-04-17

---

## Commands Intentionally Not Executed

| Command | Risk Level | Reason |
|---------|-----------|--------|
| `reboot` | **CRITICAL** | Would reboot the AP and disrupt all connected clients |
| `reset` | **CRITICAL** | Returns configuration to defaults; destroys all settings |
| `reset-button` | **HIGH** | Modifies physical reset button behavior |
| `save config current` | **HIGH** | Would overwrite the current saved configuration |
| `save config bootstrap` | **HIGH** | Would overwrite the bootstrap configuration |
| `exec capture` | **MODERATE** | Would initiate packet capture; may impact performance |
| `exec antenna-alignment` | **MODERATE** | Would change radio behavior during alignment |
| `exec bypass-wan-hardening` | **MODERATE** | Would disable WAN security hardening |
| `exec delay-execute` | **LOW** | Would delay subsequent command execution |
| `clear` | **HIGH** | Would clear dynamic system information |
| `load` | **HIGH** | Would load a new configuration file |
| `no <anything>` | **HIGH** | Would remove existing configuration |
| Any configuration `set` command | **HIGH** | Would modify running configuration |
| `debug console` | **LOW** | Would enable debug output; may flood console |
| `_debug-adspsensor` | **MODERATE** | Hidden debug command; behavior uncertain |
| `save image <url>` | **HIGH** | Would download and install a new firmware image |
| `exec active-alarms-resending` | **LOW** | Would flood HiveManager with alarm resends |

## Safe Commands Executed

All commands executed during this session were **read-only show commands** and the **help tree (`?`) enumeration**. No configuration changes were made.

The only non-show command executed was:
- `console page 0` — Disables output paging (non-destructive, session-scoped)

## Risk Mitigation

- All evidence was collected via read-only commands
- No configuration was saved or modified
- No firmware operations were performed
- The AP remained operational throughout the session
- CAPWAP connection to XIQ was maintained throughout
