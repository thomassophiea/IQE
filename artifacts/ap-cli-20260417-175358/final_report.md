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
Executed five harvest passes:
1. **Phase 1 harvest:** Top-level `?` help, full `show ?` help tree, all standard show commands, configuration help trees
2. **Phase 2 harvest:** Deep-dive into exec, save, debug subcommands, plus all remaining show families
3. **Phase 3 harvest:** `show cmds` full output (~1800 command variants with exact syntax), hidden `_` prefix probing (`_a` through `_z`), named object detail views (all SSIDs, security objects, radio profiles), missing interface details (wifi2, eth1, agg0, red0, iotgw), ARP/NDP cache, network state
4. **Phase 4 harvest:** Deep config subcommand trees (~35+ command families via `?` recursion), `no ?` complete tree, `clear ?` complete tree, output filter syntax, live ping/tracert with output capture
5. **Phase 5 harvest:** Full `show tech` capture (8102 lines)

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
| Show commands | ~110 | Fully enumerated; ~50+ executed with output |
| Exec commands | 18 | Fully enumerated |
| Save commands | 30+ | Fully enumerated (TFTP + HTTP/HTTPS variants) |
| Debug commands | 1 (debug console) | Limited access observed |
| Utility commands | 6 | Fully enumerated |
| Hidden commands | 2 (_system, _debug-adspsensor) + 19 hidden prefixes | Probed `_a`–`_z` |
| Negation (`no`) commands | 92 | Complete `no ?` tree |
| Clear commands | 28 | Complete `clear ?` tree |
| Authoritative syntax (`show cmds`) | ~1800 variants | Complete capture |

### Coverage Assessment
- **Help tree enumeration:** Complete for all top-level, first-level, and many second-level subcommands
- **Authoritative syntax:** `show cmds` captured all ~1800 command variants with exact parameter types
- **Show command execution:** ~50+ show commands executed with output captured
- **Configuration subcommand depth:** 2-3 levels enumerated via `?` for all major families (capwap, aaa, ssid, interface, radio, security-object, ip, ipv6, routing, vpn, logging, snmp, qos, forwarding-engine, hotspot, bonjour, admin, boot-param, clock, console, system, telegraf, application, etc.)
- **Named object details:** All 4 SSIDs, all 5 security objects, all 3 radio profiles captured with full detail
- **Hidden command probing:** Systematic `_a` through `_z` probing identified 19 active hidden prefixes
- **Not fully recursed:** Deep sub-sub-commands for all named object combinations were not traversed due to combinatorial explosion

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

1. **Deep subcommand recursion:** Configuration commands with named objects (e.g., `ssid <name> <param> <subparam>`) were not fully recursed due to combinatorial depth — however, `show cmds` provides the authoritative complete syntax
2. **Config mode commands:** Some commands may have additional subcommands when specific objects exist; these depend on what is configured
3. **Debug commands:** Only `debug console` was found accessible; deeper debug tree may exist in engineering modes
4. **Hidden commands:** Probing `_a`–`_z` identified 19 active hidden prefixes, but their full command trees could not be enumerated since `?` does not expose them
5. **Show tech:** Output was captured (8102 lines) but not fully parsed — it contains aggregated output of most show commands
6. **Output redaction:** Passwords and keys in `show running-config` are masked as `***`
7. **Dynamic state:** ARP cache, NDP cache, station list, and interface counters are snapshots from the time of capture

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
| `inventory.md` | Device hardware, software, interface, radio, SSID, CAPWAP, security object, radio profile inventory |
| `command_catalog.md` | Complete CLI command catalog by category with descriptions, negation tree, clear tree, deep config subcommands, hidden command probing |
| `behavior_notes.md` | CLI behavior: prompts, paging, errors, automation notes, output filters, ping/tracert examples, quirks |
| `privilege_map.md` | Privilege level assessment and denied command analysis |
| `risk_register.md` | Commands intentionally not executed with justification |
| `final_report.md` | This report |
| `evidence/raw/harvest_phase1.log` | Raw terminal output — first enumeration pass (5674 lines) |
| `evidence/raw/harvest_phase2.log` | Raw terminal output — second enumeration pass (7724 lines) |
| `evidence/raw/harvest_phase3.log` | Raw terminal output — show cmds, hidden commands, named objects (2563 lines) |
| `evidence/raw/harvest_phase4.log` | Raw terminal output — deep config trees, no/clear trees, ping/tracert (1134 lines) |
| `evidence/raw/show_tech_full.log` | Full `show tech` capture (8102 lines) |
| `evidence/raw/wing_check.log` | Verification of `_system boot-os` and `_debug-adspsensor` subcommands |
| `evidence/raw/session_start.txt` | Session metadata |

## 15. Evidence Traceability

All claims in this report are traceable to:
- `evidence/raw/harvest_phase1.log` — Lines 1-5674
- `evidence/raw/harvest_phase2.log` — Lines 1-7724
- `evidence/raw/harvest_phase3.log` — Lines 1-2563
- `evidence/raw/harvest_phase4.log` — Lines 1-1134
- `evidence/raw/show_tech_full.log` — Lines 1-8102

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
- `show cmds` (authoritative syntax): `harvest_phase3.log` lines 7-1823
- Hidden `_` prefix probing: `harvest_phase3.log` lines 1824-1906
- SSID detail views: `harvest_phase3.log` lines 1907-2098
- Security object details: `harvest_phase3.log` lines 2099-2232
- Radio profile details: `harvest_phase3.log` lines 2233-2431
- Interface wifi2/eth1/agg0/red0/iotgw: `harvest_phase3.log` lines 2432-2542
- Deep config subcommand trees: `harvest_phase4.log` lines 6-699
- `no ?` complete tree: `harvest_phase4.log` lines 866-1037
- `clear ?` complete tree: `harvest_phase4.log` lines 1039-1077
- Output filter syntax: `harvest_phase4.log` lines 1088-1091
- Ping/tracert live output: `harvest_phase4.log` lines 1092-1133
