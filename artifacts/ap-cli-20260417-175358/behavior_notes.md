# CLI Behavior Notes
## AP5010U-WW | IQ Engine 10.8r5

**Generated:** 2026-04-17

---

## Prompt Behavior

| Context | Prompt Format | Example |
|---------|---------------|---------|
| Root admin mode | `<hostname>#` | `Thomas-5010-01#` |
| No sub-modes observed | N/A | CLI is flat (no `configure terminal` or `config` sub-mode) |

The IQ Engine CLI uses a **flat command structure** — all configuration, show, exec, and save commands execute from a single `#` prompt. There is no `enable` / `configure` / `config-if` mode hierarchy like Cisco IOS.

## Paging Behavior

- **Default:** Paging is enabled (output pauses at screen boundaries)
- **Disable paging:** `console page 0`
- **Persistence:** Setting survives the session but is not saved to config by default
- **Recommendation:** Always issue `console page 0` before scripted/automated sessions

## Command Completion & Abbreviation

- **Tab completion:** Supported
- **Abbreviation:** Partial command matching is supported
- **Ambiguous input:** When an abbreviation matches multiple commands, the CLI returns `^-- Ambiguous input`
- **Unknown keyword:** When a keyword is completely wrong: `^-- unknown keyword or invalid input`
- **Incomplete command:** When mandatory parameters are missing: `ERROR: Incomplete command`
- **Caret position:** The `^--` error marker indicates the exact position of the error

## Error Messages

| Error | Meaning |
|-------|---------|
| `^-- unknown keyword or invalid input` | Command or parameter not recognized |
| `ERROR: Incomplete command` | Required parameters missing |
| `^-- Ambiguous input` | Abbreviation matches multiple commands |
| `doesn't exist!` | Named object not found |

## Output Formatting

- **Tables:** Fixed-width columns with header rows and `-` separator lines
- **Key-value:** `Key: Value` or `Key=Value` format
- **Multi-line values:** Some values wrap with consistent indentation
- **Masked values:** Passwords/keys shown as `***`
- **Empty results:** Some commands return nothing when no data exists (e.g., `show filter`, `show mobility-policy`)

## Output Modifiers

All `show` commands support:
- `| <word>` — Filter output to lines containing the specified word
- `> <server>` — Redirect output to an external server (tftp/scp/http)

## Automation Suitability

### Excellent for Automation
- `show version` — Clean key-value, easily parsed
- `show hw-info` — Clean key-value
- `show memory` — Simple 3-line output
- `show cpu` — Simple 3-line output
- `show interface` — Consistent table format
- `show ip route` — Consistent table format
- `show station` — Structured per-SSID tables
- `show running-config` — Deterministic line-based config
- `show clock` — Single line, parseable date format
- `show dns` — Clean key-value

### Moderate for Automation
- `show interface <name>` — Large output, key-value but with complex sub-sections
- `show capwap client` — Many key-value pairs, some with nested indentation
- `show logging buffered` — Variable-length log output, timestamps parseable
- `show lldp neighbor` — Semi-structured, variable number of neighbors

### Poor for Automation
- `show tech` — Massive compound output of multiple show commands; includes embedded log data
- `show running-config` with passwords — Passwords masked as `***`

## Command Hangs / Timeouts

No commands were observed to hang during this session. All commands returned within expected timeframes (< 2 seconds).

## Truncation

- `show logging buffered` — Output is naturally limited to buffer size
- `show tech` — Very large output; may be truncated in automated collection if timeout is too short

## Sensitive / Redacted Output

The following show commands redact sensitive information:
- `show running-config` — Passwords displayed as `***`
- `show security-object <name>` — Keys displayed as `***`

## Session Behavior

- **SSH:** Standard SSHv2; supports key auth and password auth
- **Login banner:** `Copyright (c) 2006-2025 Extreme Networks, Inc.`
- **Login logging:** Each login is logged: `Admin "<admin>" successfully logged in`
- **Each command logged:** Syslog records every command execution with username
- **Concurrent sessions:** Multiple SSH sessions are supported simultaneously
- **Exit:** `exit` or `quit` terminates the session

## Notable Quirks

1. **`exec` subcommands:** Many commands listed in prior documentation as `exec` subcommands (ping, tracert, dns-query, etc.) are actually **top-level commands** on this platform, not under the `exec` prefix. Attempting `exec ping ?` returns `unknown keyword or invalid input`.

2. **Duplicate `show` and `interface` entries in help:** The `?` help output shows `show` listed 4 times and `interface` listed twice with different descriptions. This is because the same keyword has multiple contexts (e.g., `show` for standard show commands, `show` for ADSP sensor tables).

3. **`save web`:** Returns `Ambiguous input` because it matches both `web-page` and `web-server-key`.

4. **`show flash` and `show process` and `show inventory`:** Return `unknown keyword or invalid input` on this platform/version. These may be available on other AP models.

5. **No `configure` mode:** Unlike Cisco IOS, there is no separate configuration mode. All config commands execute at the root prompt.

6. **`_debug-adspsensor`:** Hidden command (underscore prefix) visible in top-level `?` help. Likely debug-only functionality for ADSP wireless intrusion detection.
