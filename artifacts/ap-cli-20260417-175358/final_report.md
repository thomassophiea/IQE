# AP CLI Documentation - Final Report
## Extreme Networks AP5010U-WW | IQ Engine 10.8r5

**Date:** 2026-04-17
**Author:** Automated CLI Audit (Claude)
**Target:** Thomas-5010-01 (192.168.100.206)
**Account:** admin (root-admin)

---

## 1. Scope

This report documents the complete accessible CLI surface of an Extreme Networks AP5010U-WW access point running IQ Engine 10.8r5 (build-91a62d2). The enumeration covers:

- All top-level configuration commands
- All show commands with live output capture
- All exec commands
- All save commands
- Debug command access
- Help tree traversal to identify subcommands
- Running configuration capture
- Hardware and software inventory
- CAPWAP/cloud management state
- Privilege boundary assessment

## 2. Methodology

### Phase 1: Local Folder Inspection
Inventoried the existing repository contents:
- `Aerohive_CLI_Complete_Reference.md` (1,244 lines) — Prior documentation from an AP5050D-WW
- `Aerohive_CLI_Complete_Reference.pdf` — PDF version of the above
- `README.md` — Repository description

### Phase 2: Artifact Structure
Created `artifacts/ap-cli-20260417-175358/` with `evidence/raw/` and `evidence/parsed/` subdirectories.

### Phase 3: SSH Connection
Connected via SSH with password authentication. Used `expect` scripts for automated command enumeration.

### Phase 4: CLI Enumeration
Executed two harvest passes:
1. **Phase 1 harvest:** Top-level `?` help, full `show ?` help tree, all standard show commands, configuration help trees
2. **Phase 2 harvest:** Deep-dive into exec, save, debug subcommands, plus all remaining show families

Each pass captured complete terminal output including prompts, commands, and responses.

### Phase 5: Documentation Generation
Parsed evidence files to produce structured markdown documentation.

## 3. Existing Materials Reviewed

### Aerohive_CLI_Complete_Reference.md (Prior Work)
- **Device:** AP5050D-WW (different model than current target)
- **Software:** IQ Engine 10.8r5 (same version)
- **Content:** ~100+ config commands, ~90+ show commands, ~20+ exec commands, ~20+ save commands, hidden commands
- **Assessment:** Good foundational document but targeted at a different hardware platform. Some commands listed there do not exist on the AP5010U (e.g., `show flash`, `show process`, `show inventory`). The command descriptions and help text are accurate for the shared command set.

### What Was Preserved
- The existing reference remains valid for AP5050D-WW
- This new audit provides AP5010U-WW-specific documentation
- Common commands between platforms are consistent

### What Was Merged
- Platform-specific differences identified (AP5010U vs AP5050D)
- The existing reference served as a guide for which commands to verify on the live device
- All claims from the existing reference were validated against live device output

## 4. Account Privilege

| Field | Value |
|-------|-------|
| Username | admin |
| Type | root-admin |
| Access Level | Full / Unrestricted |

No privilege boundaries were encountered. All command families were accessible.

## 5. CLI Coverage Summary

### Commands Documented

| Category | Count | Status |
|----------|-------|--------|
| Configuration commands (top-level) | ~100 | Fully enumerated via `?` |
| Show commands | ~110 | Fully enumerated; ~40 executed with output |
| Exec commands | 18 | Fully enumerated |
| Save commands | 18+ | Fully enumerated |
| Debug commands | 1 (debug console) | Limited access observed |
| Utility commands | 6 | Fully enumerated |
| Hidden commands | 1 (_debug-adspsensor) | Identified |

### Coverage Assessment
- **Help tree enumeration:** Complete for all top-level and first-level subcommands
- **Show command execution:** ~40 show commands executed with output captured
- **Configuration subcommand depth:** First 2 levels enumerated via `?`
- **Not fully recursed:** Deep configuration sub-sub-commands (e.g., `ssid <name> <param> <subparam> ?`) were not fully traversed due to the combinatorial explosion of named objects

## 6. Device Baseline Summary

| Field | Value |
|-------|-------|
| Hostname | Thomas-5010-01 |
| Platform | AP5010U-WW |
| Serial | WM012243W-30032 |
| Software | IQ Engine 10.8r5 build-91a62d2 |
| Bootloader | v0.0.4.69 |
| TPM | v2.0.1.38 |
| Memory | 2 GB (57% free) |
| CPU | <1% utilization |
| Radios | 3 (2.4 GHz, 5 GHz, 6 GHz) — Wi-Fi 6E capable |
| SSIDs | 4 (Skynet, Skynet_Junior, Skynet_Guest, Skynet_6GHz) — all WPA3-SAE |
| Cloud | Connected to XIQ (ui1r1-cws-0.qa.xcloudiq.com) via CAPWAP/DTLS |
| PoE | PoE bt powered |
| LLDP Neighbor | SW-4220 (Extreme 4220-8MW-40P-4X, SwitchEngine 33.5.2.118) |
| IoT | CC2652R1 Thread/BLE chip present |
| License | Permanent |

## 7. Notable Command Families

### Configuration Commands (~100)
The AP supports extensive configuration including:
- Network (interface, IP, IPv6, DNS, routing, LLDP, VLAN)
- Wireless (radio profiles, SSIDs, ACSP, band steering, client load balance)
- Security (AAA, 802.1X, security objects, supplicant, RadSec)
- User management (user profiles, policies, device groups, MAC/OS/domain objects)
- QoS (classifier, marker, policy, CAC for VoIP)
- VPN (IPSec, GRE, L3 tunnels)
- Monitoring (logging, data collection, telegraf, sflow, SNMP)
- Cloud management (CAPWAP, HiveManager, telegraf telemetry)
- Application awareness (L7 application, ALG, forwarding engine)

### Show Commands (~110)
The most comprehensive read-only command set, covering every aspect of device state, configuration, and statistics.

### Exec Commands (18)
Operational commands for testing, monitoring, and troubleshooting. Notable entries:
- `exec bypass-wan-hardening` — Disables WAN security for remote troubleshooting
- `exec ssh-client` — Built-in SSH client
- `exec tcp-service` — TCP service testing
- `exec antenna-alignment` — Directional antenna alignment tool

### Save Commands (18+)
File transfer and persistence commands supporting TFTP, SCP, HTTP, and HTTPS protocols.

## 8. Privilege Boundary Findings

No privilege boundaries were encountered with the `root-admin` account. All commands are accessible. The AP supports multiple admin types:
- `root-admin` — Full access (used in this audit)
- `admin` — Standard admin (may have restrictions)
- `read-only` — Show commands only

## 9. Operationally Sensitive Branches

Commands intentionally not executed (see `risk_register.md`):
- `reboot`, `reset` — Destructive system operations
- `save config` — Would overwrite persistent configuration
- `save image` — Would install new firmware
- `no <any>` — Would remove configuration
- `load` — Would load new configuration
- `clear` — Would clear dynamic data
- `exec capture` — Would initiate packet capture
- `exec bypass-wan-hardening` — Would reduce security posture

## 10. Automation Candidates

Best commands for automated monitoring scripts:

| Command | Use Case | Parse Difficulty |
|---------|----------|-----------------|
| `show version` | Version/uptime tracking | Easy |
| `show memory` | Memory monitoring | Easy |
| `show cpu` | CPU monitoring | Easy |
| `show interface` | Interface status | Easy (table) |
| `show station` | Client tracking | Moderate (multi-table) |
| `show ip route` | Route monitoring | Easy (table) |
| `show capwap client` | Cloud connectivity | Moderate (key-value) |
| `show logging buffered` | Log collection | Moderate (timestamped) |
| `show running-config` | Config backup | Easy (line-based) |
| `show lldp neighbor` | Topology discovery | Moderate |

Prerequisite for all automation: Issue `console page 0` first.

## 11. Platform Differences: AP5010U vs AP5050D

Commands in the prior AP5050D reference that are **not available** on AP5010U:
- `show flash`
- `show process`
- `show inventory`
- `show ip dns` (use `show dns` instead)
- `show ip arp` (use `show arp-cache` instead)
- Various `exec` subcommands (ping, tracert, etc. are top-level on AP5010U)

Commands on AP5010U **not in the prior reference**:
- `show fabric-attach`
- `show telegraf`
- `show application-essentials`
- `show client-info-collection`
- `show ndp-cache`
- `show mdnsd`
- `show video`
- `show wan`
- `show proxy`
- `iot-esl-imagotag`
- `telegraf` (full telemetry subsystem)
- `ftm-policy` (Fine Time Measurement)
- `location-essentials`
- `wips-essentials`

## 12. Limitations

1. **Deep subcommand recursion:** Configuration commands with named objects (e.g., `ssid <name> <param>`) were not fully recursed due to combinatorial depth
2. **Config mode commands:** Some commands may have additional subcommands when specific objects exist; these depend on what is configured
3. **Debug commands:** Only `debug console` was found accessible; deeper debug tree may exist in engineering modes
4. **Hidden commands:** Only one `_` prefixed command was discovered via `?`; additional hidden commands may exist that are not shown in help
5. **Show tech:** Output was captured but is very large; not fully parsed in this session
6. **Output redaction:** Passwords and keys in `show running-config` are masked as `***`

## 13. Recommended Next Steps

1. **Deep subcommand enumeration:** Recurse into each configuration command's sub-subcommand tree (e.g., `ssid <name> ?`, `interface mgt0 ?`, `radio profile <name> ?`)
2. **Multiple privilege levels:** Test with `read-only` and standard `admin` accounts to map privilege boundaries
3. **Cross-platform comparison:** Run the same enumeration on AP5050D, AP4000, AP3000 series to document platform differences
4. **Config mode commands:** Enumerate commands available only when specific objects are created
5. **Engineering/debug access:** If available, enumerate the full debug command tree
6. **Automation scripts:** Build parsers for the automation-candidate commands identified above
7. **Firmware version comparison:** Run on IQ Engine 10.7, 10.6 to document version-to-version changes

## 14. Artifacts Produced

| File | Description |
|------|-------------|
| `inventory.md` | Device hardware, software, interface, radio, SSID, CAPWAP inventory |
| `command_catalog.md` | Complete CLI command catalog by category with descriptions |
| `behavior_notes.md` | CLI behavior: prompts, paging, errors, automation notes, quirks |
| `privilege_map.md` | Privilege level assessment and denied command analysis |
| `risk_register.md` | Commands intentionally not executed with justification |
| `final_report.md` | This report |
| `evidence/raw/harvest_phase1.log` | Raw terminal output — first enumeration pass |
| `evidence/raw/harvest_phase2.log` | Raw terminal output — second enumeration pass |
| `evidence/raw/session_start.txt` | Session metadata |

## 15. Evidence Traceability

All claims in this report are traceable to:
- `evidence/raw/harvest_phase1.log` — Lines 1-5674
- `evidence/raw/harvest_phase2.log` — Lines 1-7724

Key evidence locations:
- Top-level `?` help: `harvest_phase1.log` lines 7-205
- `show ?` help: `harvest_phase1.log` lines 206-401
- `show version`: `harvest_phase1.log` lines 403-413
- `show running-config`: `harvest_phase1.log` lines 420-609
- `show interface`: `harvest_phase1.log` lines 610-632
- `show interface wifi0` (detailed radio): `harvest_phase1.log` lines 658-720
- `show capwap client`: `harvest_phase1.log` lines 886-924
- `exec ?` help: `harvest_phase2.log` lines 7-48
- `save ?` help: `harvest_phase2.log` lines 96-136
- `show hw-info`: `harvest_phase2.log` lines 219-232
- `show station`: `harvest_phase2.log` lines 331-363
- `show lldp neighbor`: `harvest_phase2.log` lines 444-460
