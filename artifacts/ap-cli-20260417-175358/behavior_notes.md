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

## Output Modifiers (Confirmed via Phase 4)

All `show` commands support piped filters:

| Syntax | Description |
|--------|-------------|
| `show <cmd> \| include <word>` | Show only lines containing `<word>` |
| `show <cmd> \| exclude <word>` | Show only lines NOT containing `<word>` |
| `show <cmd> > <server>` | Redirect output to external server (tftp/scp/http/https) |

The pipe syntax requires a space before and after the `|` character. When `?` is entered after `|`, the CLI shows:
```
    exclude   exclude input
    include   include input
```

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

## Ping / Tracert Output Examples (Phase 4)

### Ping (local gateway)
```
Thomas-5010-01#ping 192.168.100.1
PING 192.168.100.1 (192.168.100.1): 56 data bytes
64 bytes from 192.168.100.1: seq=0 ttl=64 time=0.705 ms
64 bytes from 192.168.100.1: seq=1 ttl=64 time=0.524 ms
64 bytes from 192.168.100.1: seq=2 ttl=64 time=0.784 ms
64 bytes from 192.168.100.1: seq=3 ttl=64 time=0.640 ms
64 bytes from 192.168.100.1: seq=4 ttl=64 time=0.556 ms

--- 192.168.100.1 ping statistics ---
5 packets transmitted, 5 received, 0% packet loss
round-trip min/avg/max = 0.524/0.641/0.784 ms
```

### Ping (internet, with count)
```
Thomas-5010-01#ping 1.0.0.1 count 3
PING 1.0.0.1 (1.0.0.1): 56 data bytes
64 bytes from 1.0.0.1: seq=0 ttl=55 time=22.165 ms
64 bytes from 1.0.0.1: seq=1 ttl=55 time=15.954 ms
64 bytes from 1.0.0.1: seq=2 ttl=55 time=15.800 ms

--- 1.0.0.1 ping statistics ---
3 packets transmitted, 3 received, 0% packet loss
round-trip min/avg/max = 15.800/17.973/22.165 ms
```

### Tracert
```
Thomas-5010-01#tracert 1.0.0.1
traceroute to 1.0.0.1 (1.0.0.1), 30 hops max, 46 byte packets
 1  192.168.100.1 (192.168.100.1)  0.594 ms  0.380 ms  0.475 ms
 2  syn-072-031-136-181.inf.spectrum.com (72.31.136.181)  8.934 ms  7.914 ms  7.455 ms
 3  int-0-5-1-8.orld12-ser1.netops.charter.com (71.46.8.241)  9.975 ms  7.400 ms  7.955 ms
 ...
10  one.one.one.one (1.0.0.1)  16.464 ms  16.090 ms  16.205 ms
```

### Ping Syntax Options
```
ping <ip_addr> [count <n>] [size <n>] [ttl <n>] [timeout <n>]
ping <ipv6_addr> [interface <string>] [count <n>] [size <n>] [ttl <n>] [timeout <n>]
ping <string> [interface <string>] [count <n>] [size <n>] [ttl <n>] [timeout <n>]
```

### Tracert Syntax Options
```
tracert <ip_addr|string> [max-hops <n>] [timeout <n>] [no-resolve]
```

**Observations:**
- Default ping sends 5 packets (not ICMP, uses standard BusyBox ping)
- Output format is standard BusyBox — easy to parse
- Tracert uses standard format (hop number, hostname, IP, three RTTs)
- Both support IPv4 and hostname resolution
- Ping supports IPv6 with optional interface binding

## Named Object Error Behavior

When trying to create a named object that already exists:
- SSIDs: `"<name>" cannot be used because it matches an existing SSID or Hive name.`
- Radio profiles: `Radio profile <name> already exists!`
- Security objects: `Create/delete security object failed! ERROR: Invalid parameter(s)`

These messages are important for automation — they indicate the named object already exists but allow `?` traversal to show subcommands.

## Notable Quirks

1. **`exec` subcommands:** Many commands listed in prior documentation as `exec` subcommands (ping, tracert, dns-query, etc.) are actually **top-level commands** on this platform, not under the `exec` prefix. Attempting `exec ping ?` returns `unknown keyword or invalid input`.

2. **Duplicate `show` and `interface` entries in help:** The `?` help output shows `show` listed 4 times and `interface` listed twice with different descriptions. This is because the same keyword has multiple contexts (e.g., `show` for standard show commands, `show` for ADSP sensor tables).

3. **`save web`:** Returns `Ambiguous input` because it matches both `web-page` and `web-server-key`.

4. **`show flash` and `show process` and `show inventory`:** Return `unknown keyword or invalid input` on this platform/version. These may be available on other AP models.

5. **No `configure` mode:** Unlike Cisco IOS, there is no separate configuration mode. All config commands execute at the root prompt.

6. **`_debug-adspsensor`:** Hidden command (underscore prefix) visible in top-level `?` help. Likely debug-only functionality for ADSP wireless intrusion detection.

7. **Hidden underscore commands:** Probing `_a` through `_z` revealed 19 out of 26 prefixes have hidden commands (returning "Ambiguous input" or "Incomplete command"). Only `_system` and `_debug-adspsensor` are documented in help. The rest are engineering/debug commands.

8. **`_e` executes silently:** Entering `_e` returns no output and no error, suggesting a hidden command matched and executed (possibly a no-op or status query).

9. **Config rollback:** `config rollback` supports automatic rollback on CAPWAP disconnect, next reboot, manual timer, or immediate execution. This is a safety feature for remote management.

10. **`show cmds` is authoritative:** The `show cmds` command outputs the complete CLI command index with full syntax for every command. This is the definitive source — it shows ~1800+ command variants with exact parameter syntax including types (`<ip_addr>`, `<string>`, `<number>`, `<mac_addr>`, etc.).

11. **Thread/BLE interfaces:** The AP has `threadx` and `blex` interfaces for IoT (CC2652R1 chip). Thread supports dataset configuration, commissioner mode, NAT64, and OT-CTL passthrough. BLE supports iBeacon and generic BLE monitoring.
