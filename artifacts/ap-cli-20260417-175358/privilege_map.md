# Privilege Map
## AP5010U-WW | IQ Engine 10.8r5 | Account: admin (root-admin)

**Generated:** 2026-04-17

---

## Account Privilege Level

| Field | Value |
|-------|-------|
| Username | admin |
| Type | root-admin |
| Prompt | `Thomas-5010-01#` |

The `admin` account is the highest privilege level (`root-admin`). No additional `enable` or privilege escalation was required.

## Accessible at Current Privilege Level

### Fully Accessible Command Families

All top-level configuration commands, show commands, exec commands, save commands, and utility commands listed in the command catalog are accessible from this account.

Summary:
- **~100+ configuration commands** — All accessible
- **~110+ show commands** — All accessible  
- **~18 exec commands** — All accessible
- **~18 save commands** — All accessible
- **Debug console** — Accessible
- **Utility (ping, tracert, exit, quit, etc.)** — All accessible
- **Hidden `_debug-adspsensor`** — Visible and likely accessible

## Commands That Returned Errors

These are **not privilege blocks** — they are syntax/platform issues:

| Command | Error | Likely Reason |
|---------|-------|---------------|
| `show flash` | `unknown keyword or invalid input` | Not available on AP5010U platform |
| `show process` | `unknown keyword or invalid input` | Not available on AP5010U platform |
| `show inventory` | `unknown keyword or invalid input` | Not available on AP5010U platform |
| `show ip dns` | `unknown keyword or invalid input` | Use `show dns` instead |
| `show ip arp` | `unknown keyword or invalid input` | Use `show arp-cache` instead |
| `exec ping` | `unknown keyword or invalid input` | `ping` is a top-level command |
| `exec tracert` | `unknown keyword or invalid input` | `tracert` is a top-level command |
| `exec dns-query` | `unknown keyword or invalid input` | Not available or renamed |
| `exec save-image` | `unknown keyword or invalid input` | Use `save image` instead |
| `exec dnxp` | `unknown keyword or invalid input` | Not available on this version |
| `exec radius-test` | `unknown keyword or invalid input` | Not available on this version |
| `exec capwap-test` | `unknown keyword or invalid input` | Not available on this version |
| `exec ntp-test` | `unknown keyword or invalid input` | Not available on this version |
| `exec snmpwalk` | `unknown keyword or invalid input` | Not available on this version |
| `exec iperf` | `unknown keyword or invalid input` | `iperf` is a top-level command |
| `exec iperf3` | `unknown keyword or invalid input` | `iperf3` is a top-level command |

## Privilege Boundary Assessment

**No privilege boundaries were encountered.** The `root-admin` account has unrestricted access to all CLI commands available on this firmware version and platform.

### What Would Be Different at Lower Privilege

IQ Engine supports multiple admin types:
- `root-admin` — Full access (current level)
- `admin` — Standard admin (may restrict certain exec/config commands)
- `read-only` — Show commands only

Lower privilege levels would likely restrict:
- Configuration commands (all `no` and set commands)
- `exec` commands
- `save` commands
- `debug` commands
- `reboot` and `reset` commands
- Password-related `admin` commands

### Denial Behavior

When commands fail at this privilege level, the AP returns one of:
- `^-- unknown keyword or invalid input` (command doesn't exist on this platform)
- `ERROR: Incomplete command` (syntax incomplete, not privilege denied)

No explicit "permission denied" or "insufficient privileges" messages were observed, confirming full root-admin access.
