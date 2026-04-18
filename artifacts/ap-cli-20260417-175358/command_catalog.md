# IQ Engine CLI Command Catalog
## AP5010U-WW | IQ Engine 10.8r5 | Admin Privilege Level

**Generated:** 2026-04-17
**Method:** Live enumeration via SSH with `?` help tree traversal
**Prompt:** `Thomas-5010-01#` (root admin mode, no config sub-mode)

---

## Table of Contents
1. [Top-Level Configuration Commands](#1-top-level-configuration-commands)
2. [Show Commands](#2-show-commands)
3. [Exec Commands](#3-exec-commands)
4. [Save Commands](#4-save-commands)
5. [Debug Commands](#5-debug-commands)
6. [Utility / Navigation Commands](#6-utility--navigation-commands)
7. [Hidden / Underscore Commands](#7-hidden--underscore-commands)

---

## 1. Top-Level Configuration Commands

These commands configure the AP from the root `#` prompt. Prefix with `no` to negate.

### Network & Interface

| Command | Description |
|---------|-------------|
| `interface` | Set interface parameters / Set Energy Efficient Ethernet |
| `ip` | Set IP parameters |
| `ipv6` | Set IPv6 parameters |
| `dns` | Set DNS (Domain Name System) parameters |
| `routing` | Set routing parameters |
| `route` | Set a MAC address route |
| `lldp` | Set LLDP (Link Layer Discovery Protocol) parameters |
| `vlan-group` | Set a VLAN group |

### Wireless & Radio

| Command | Description |
|---------|-------------|
| `radio` | Set radio profile parameters |
| `ssid` | Set SSID (Service Set Identifier) parameters |
| `acsp` | Set parameters for ACSP (Advanced Channel Selection Protocol) |
| `client-mode` | Set wireless client parameters for local device association |
| `client-load-balance` | Client load balancing parameters |
| `band-steering` | Band steering parameters in the WLAN |
| `sdr-profile` | Set SDR (Software Defined Radio) profile parameters |

### Security & AAA

| Command | Description |
|---------|-------------|
| `aaa` | Set parameters for AAA (authentication, authorization, accounting) |
| `802.1x-mac-table` | Set parameters for the client MAC address table for 802.1X/EAP |
| `security` | Set the security parameters |
| `security-object` | Set parameters for a security object controlling network access |
| `supplicant` | Set parameters for a supplicant object for HiveOS |
| `radsec-proxy` | Set parameters for RadSec proxy servers (TLS tunnel to ID Manager) |

### User & Profile Management

| Command | Description |
|---------|-------------|
| `user` | Add one user or change user parameters |
| `user-group` | Set user group parameters |
| `user-profile` | Set parameters for a user profile |
| `user-profile-policy` | Set the user profile mapping policy |
| `admin` | Set the administrator parameters |
| `login` | Set parameters for the CLI login |

### Policy & Firewall

| Command | Description |
|---------|-------------|
| `network-firewall` | Set a Layer 3 firewall policy (Max: 1024 rules) |
| `mac-policy` | Set MAC policy parameters |
| `ip-policy` | Set IP policy parameters |
| `ip-filter` | *(blocked — see note under mac-filter)* |
| `mac-filter` | *(see security mac-filter)* |
| `library-sip-policy` | Set a SIP policy for library patron user profiles |
| `mobile-device-policy` | Set a policy assigning user profiles based on device attributes |
| `mobility-policy` | Set parameters for a mobility policy |
| `mobility-threshold` | Set parameters for tunneling mobile user traffic |

### Object Definitions

| Command | Description |
|---------|-------------|
| `device-group` | Set a device group for classifying client devices (Max: 64) |
| `domain-object` | Set domain object for user profile assignment (Max: 64) |
| `mac-object` | Set MAC object for user profile assignment (Max: 128) |
| `os-object` | Set OS object for user profile assignment (Max: 64) |
| `mdm-object` | Set MDM (mobile device management) object |
| `time-object` | Set a time object |
| `service` | Set a custom service |
| `schedule` | Set a schedule to control user profiles and SSID availability |

### QoS

| Command | Description |
|---------|-------------|
| `qos` | Set QoS (Quality of Service) parameters |
| `cac` | Set CAC (Call Admission Control) parameters for VoIP |

### VPN & Tunneling

| Command | Description |
|---------|-------------|
| `vpn` | Set parameters for VPN tunneling |
| `ssh-tunnel` | Set SSH tunnel parameters for remote support access |

### Hive / Mesh

| Command | Description |
|---------|-------------|
| `hive` | Create a hive or set hive parameters |
| `amrp` | Set AMRP (Advanced Mobility Routing Protocol) parameters |
| `roaming` | Set roaming parameter |

### Management & Cloud

| Command | Description |
|---------|-------------|
| `capwap` | Set parameters for CAPWAP |
| `hivemanager` | *(see capwap client server name)* |
| `hostname` | Set the hostname of the AP |
| `management` | Set management service parameters |
| `telegraf` | Set telegraf configuration parameters |
| `snmp` | Set SNMP parameters |

### Monitoring & Logging

| Command | Description |
|---------|-------------|
| `logging` | Set logging parameters |
| `report` | Set parameters for gathering traffic statistics |
| `data-collection` | Set parameters for collecting device/application data |
| `client-monitor` | Set parameters for Client Monitor |
| `location` | Set parameters for location tracking |
| `location-essentials` | Location Essentials feature |
| `wips-essentials` | WIPS Essentials feature |
| `performance-sentinel` | Set performance sentinel parameters for throughput moderation |
| `sflow` | Set sflow related parameters |

### System & Boot

| Command | Description |
|---------|-------------|
| `system` | Set system parameters |
| `boot-param` | Set parameters for the boot loader |
| `clock` | Set the internal clock |
| `ntp` | Set NTP parameters |
| `console` | Set console parameters |
| `config` | Set parameters for the current configuration file |
| `history` | Set the capacity for command history |
| `license` | Set license parameters |
| `reset-button` | Enable the reset button on the AP chassis |
| `validate_server_cert` | Set the validation of the server certificate |
| `kddr` | Enable/disable the kddr report to HM |
| `pse` | Set PSE (power sourcing equipment) power management parameters |
| `usbmodem` | Set parameters of usbmodem |
| `usbport` | Set the USB port |

### Web & Hotspot

| Command | Description |
|---------|-------------|
| `webui` | Set the WebUI for local administration |
| `web-directory` | Create a web directory for the internal web server |
| `web-security-proxy` | Proxy HTTP/HTTPS traffic to a web security server |
| `hotspot` | Set hotspot parameters |
| `hiveui` | Enable NetConfig UI |
| `bonjour-gateway` | Set Bonjour Gateway parameters |
| `presence` | Set presence profile parameters |

### Application & L7

| Command | Description |
|---------|-------------|
| `application` | Set L7 related parameters |
| `alg` | Set ALG (Application Level Gateway) parameters |
| `forwarding-engine` | Set forwarding engine shaping parameters |

### Misc

| Command | Description |
|---------|-------------|
| `capture` | Set packet capture parameters |
| `filter` | Set packet capture filter parameters |
| `device-location` | Set the device location |
| `designated-server` | Set parameters for a dynamic server |
| `iperf` | Set parameters for Iperf2 |
| `iperf3` | Set parameters for Iperf3 |
| `ftm-policy` | Set FTM (Fine Time Measurement) policy parameters |
| `iot-esl-imagotag` | Set iot-esl-imagotag parameters |
| `net-access` | Set parameters to measure internet availability/latency |
| `os-detection` | Set OS detection parameters |
| `os-version` | Set OS version detection in DHCP packets |
| `probe` | Set probe parameters |
| `reboot` | Set the system to scheduled reboot state |
| `rtts` | Create RTTS (Real Time Trouble Shooting) session |
| `teacher-view` | Set TeacherView parameters |
| `track` | Set parameters to track network device reachability |
| `track-wan` | Set parameters to track WAN reachability |
| `adsp-server` | Set ADSP server IP address |
| `client-tracing` | Test client tracing |

---

## 2. Show Commands

Complete list of `show` subcommands available at the `#` prompt.

### System & Hardware

| Command | Description | Output |
|---------|-------------|--------|
| `show version` | Software/hardware version, uptime | Key-value |
| `show system` | System parameters (multicast-ping, ICMP redirect) | Key-value |
| `show hw-info` | Hardware details (serial, MAC, manufacturing) | Key-value |
| `show boot-param` | Boot loader parameters (region, country, netboot) | Key-value |
| `show memory` | Total/free/used memory statistics | Key-value |
| `show cpu` | CPU utilization (total, user, system) | Key-value |
| `show clock` | Current date/time | Single line |
| `show time-zone` | Configured timezone | Single line |
| `show license` | License status | Single line |
| `show pse` | Power sourcing equipment status | Key-value |
| `show usb-device` | USB hub/device info | Table |
| `show reboot` | Scheduled reboot status | Status |
| `show min-password-length` | Minimum password length setting | Single line |
| `show reset-button` | Reset button state | Status |

### Configuration

| Command | Description | Output |
|---------|-------------|--------|
| `show running-config` | Full running configuration | Multi-line config |
| `show config` | Configuration file parameters | *(requires subcommand)* |
| `show admin` | Admin user accounts | Table |
| `show history` | Command history | List |
| `show console` | Console parameters | Key-value |

### Networking

| Command | Description | Output |
|---------|-------------|--------|
| `show interface` | All interfaces summary | Table |
| `show interface <name>` | Detailed interface info | Key-value |
| `show ip route` | IPv4 routing table | Table |
| `show ip nat-policy` | NAT policy parameters | - |
| `show ip path-mtu-discovery` | Path MTU Discovery status | - |
| `show ip policy-route` | IP policy routing tables | - |
| `show ip session` | IP session status | - |
| `show ip tcp-mss-threshold` | TCP MSS threshold | - |
| `show ipv6 route` | IPv6 routing table | - |
| `show dns` | DNS configuration and operation status | Key-value |
| `show route` | MAC address route table | Table |
| `show routing` | Routing parameters | *(requires subcommand)* |
| `show vlan` | VLAN groups | Table |
| `show arp-cache` | ARP cache table | Table |
| `show ndp-cache` | NDP cache table | Table |
| `show lldp` | LLDP general information | Key-value |
| `show lldp neighbor` | LLDP/CDP neighbor table | Structured |
| `show lldp cdp` | CDP parameters | - |
| `show gre-tunnel` | GRE tunnel information | - |
| `show fabric-attach` | Fabric attach information | - |

### Wireless & Radio

| Command | Description | Output |
|---------|-------------|--------|
| `show radio profile` | All radio profiles summary | Table |
| `show radio profile <name>` | Detailed radio profile | Key-value |
| `show ssid` | SSID profiles summary | Table |
| `show ssid <name>` | Detailed SSID profile | Key-value |
| `show station` | Connected wireless stations | Table (per-SSID) |
| `show acsp` | ACSP channel selection state | Table |
| `show roaming cache` | Roaming cache table | Structured |
| `show band-steering` | Band steering parameters | Key-value |
| `show client-load-balance` | Client load balancing | Key-value |
| `show client-mode` | Client mode settings | Key-value |
| `show high-density` | High-density WLAN optimization | Key-value |
| `show sdr-profile` | SDR profile parameters | - |

### Security & AAA

| Command | Description | Output |
|---------|-------------|--------|
| `show aaa` | AAA parameters summary | Key-value |
| `show aaa radius-server` | Local RADIUS server parameters | Key-value |
| `show aaa radius-server-key` | RADIUS server certificates | - |
| `show auth` | Authentication entities per interface | Structured |
| `show security` | Security parameters | - |
| `show security-object` | Security object names list | Table |
| `show security-object <name>` | Security object details | Key-value |
| `show 802.1x-mac-table` | 802.1X/EAP MAC table | Table |
| `show supplicant` | Supplicant parameters | - |
| `show radsec` | RadSec proxy information | - |
| `show ca-cert` | CA certificates for cURL/server validation | - |
| `show ppsk` | Private-PSK parameters | - |
| `show icsa` | ICSA parameters | - |
| `show idm` | ID Manager information | - |

### User Profiles & Policies

| Command | Description | Output |
|---------|-------------|--------|
| `show user-profile` | User profile table | Table |
| `show user-profile-policy` | User profile mapping policy | - |
| `show user` | All users | - |
| `show user-group` | User group parameters | - |
| `show mac-policy` | MAC policy parameters | - |
| `show ip-policy` | IP policy parameters | - |
| `show network-firewall` | Layer 3 firewall rules | Table |
| `show mobility-policy` | Mobility policy parameters | - |
| `show mobility-threshold` | Mobile user tunneling settings | - |
| `show mobile-device-policy` | Mobile device policy | - |
| `show private-client-group` | Private client group parameters | - |
| `show device-group` | Device group names/settings | - |
| `show domain-object` | Domain object names/settings | - |
| `show mac-object` | MAC object names/settings | - |
| `show os-object` | OS object names/settings | - |
| `show schedule` | Defined schedules | - |
| `show schedule-in-detail` | Detailed schedule information | - |
| `show ssid-schedule` | SSID schedule status | - |
| `show user-profile-schedule` | User profile schedule status | - |
| `show library-sip-policy` | Library SIP policy settings | - |

### QoS

| Command | Description | Output |
|---------|-------------|--------|
| `show qos` | QoS global status | Key-value |
| `show qos classifier-map` | QoS priority-to-class mapping | - |
| `show qos classifier-profile` | QoS classification profiles | - |
| `show qos counter` | QoS statistics counters | - |
| `show qos l3-police` | Layer 3 VoIP QoS policing | - |
| `show qos marker-map` | QoS class-to-priority mapping | - |
| `show qos marker-profile` | QoS marker profiles | - |
| `show qos policy` | QoS policies | - |

### VPN

| Command | Description | Output |
|---------|-------------|--------|
| `show vpn gre-tunnel` | GRE tunnel information | - |
| `show vpn ike` | IKE information | - |
| `show vpn ipsec` | IPSec information | - |
| `show vpn ipsec-tunnel` | IPSec tunnel information | - |
| `show vpn l2l-access_list` | L2L access list configuration | - |
| `show vpn l3-tunnel-exception` | Layer-3 tunnel exception list | - |
| `show vpn layer-3-tunnel` | Layer-3 tunnel information | - |
| `show vpn tunnel-id` | VPN tunnel destination/status | - |
| `show vpn tunnel-policy` | Tunnel policy information | - |

### Cloud & Management

| Command | Description | Output |
|---------|-------------|--------|
| `show capwap client` | CAPWAP client status and settings | Key-value |
| `show hivemanager` | HiveManager connection status | Key-value |
| `show hive` | Hive parameters | Table |
| `show snmp` | SNMP summary | Key-value |
| `show snmp community` | SNMP communities | - |
| `show snmp contact` | SNMP contact info | - |
| `show snmp location` | SNMP location | - |
| `show snmp trap-host` | SNMP trap host | - |
| `show snmp v3-admin` | SNMP v3 admin parameters | - |
| `show ssh-tunnel` | SSH tunnel parameters | - |
| `show telegraf` | Telegraf configurations | - |
| `show ntp` | NTP server settings | Key-value |

### Monitoring & Logging

| Command | Description | Output |
|---------|-------------|--------|
| `show logging` | Logging configuration | Key-value |
| `show logging buffered` | Buffered log messages | Multi-line |
| `show logging debug` | Debug logging state | - |
| `show logging flash` | Flash-stored logs | - |
| `show logging group` | Logging by group (aaa, wifi, system, etc.) | - |
| `show report` | Report parameters | *(requires subcommand)* |
| `show data-collection` | Data collection status | Key-value |
| `show client-monitor` | Client Monitor parameters | - |
| `show track` | IP tracking information | - |
| `show track-wan` | WAN interface tracking | Key-value |
| `show performance-sentinel` | Performance sentinel | - |

### Application & Services

| Command | Description | Output |
|---------|-------------|--------|
| `show application` | L7 application information | - |
| `show application-essentials` | Application Essentials parameters | - |
| `show alg` | ALG information | - |
| `show service` | Service details and counters | - |
| `show forwarding-engine` | Forwarding engine parameters | *(requires subcommand)* |
| `show video` | Streaming video traffic info | - |
| `show sflow` | sFlow parameters | - |
| `show proxy` | Proxy parameters | - |
| `show web-security-proxy` | Web security proxy configuration | - |

### Location & Hotspot

| Command | Description | Output |
|---------|-------------|--------|
| `show location` | Location tracking parameters | - |
| `show hotspot` | Hotspot profiles | - |
| `show bonjour-gateway` | Bonjour gateway settings/status | - |
| `show presence` | Presence profile parameters | - |
| `show wips-essentials` | WIPS Essentials parameters | - |

### Other

| Command | Description | Output |
|---------|-------------|--------|
| `show tech` | Combined output of many show commands | Very large |
| `show cmds` | All CLI commands including derived from optional keywords | - |
| `show capture` | Packet capture parameters | *(requires subcommand)* |
| `show filter` | Capture filter parameters | Empty if none set |
| `show ftm` | FTM neighbor parameters | - |
| `show ftm-policy` | FTM policy parameters | - |
| `show l3 interface` | Layer 3 interfaces | - |
| `show rtts` | RTTS information | - |
| `show wan` | BRD WAN info | - |
| `show web-directory` | Web directory files | - |
| `show web-server-key` | Web server key files | - |
| `show icon-directory` | Icon directories for OSU | - |
| `show hiveui` | NetConfig UI settings | - |
| `show os-detection` | OS detection configuration | - |
| `show teacher-view` | TeacherView parameters | - |
| `show iot-esl-imagotag` | IoT ESL Imagotag settings | - |
| `show client-info-collection` | Client information collection result | - |

### Show Command Output Modifiers

All show commands support:
- `>` — Redirect output to an external server
- `|` — Pipe output and filter by subsequently entered words

---

## 3. Exec Commands

Commands under `exec` that perform immediate operational actions.

| Command | Description |
|---------|-------------|
| `exec aaa` | Set parameters for AAA |
| `exec active-alarms-resending` | Resend all active alarms to HiveManager |
| `exec aerohive-check` | Check mobile device enrollment on Aerohive MDM |
| `exec airwatch-check` | Check mobile device enrollment on AirWatch |
| `exec antenna-alignment` | Align directional/sectional antenna with a peer |
| `exec auth` | Execute an auth module command |
| `exec bypass-wan-hardening` | Disable WAN hardening for SSH/Telnet/sniffer access |
| `exec capture` | Initiate packet capturing |
| `exec client-monitor` | Monitor client activities |
| `exec data-collection` | Perform action on collected device/application data |
| `exec delay-execute` | Delay command execution (excludes show commands) |
| `exec ftm` | Trigger FTM neighbor list update |
| `exec interface` | Execute command through a specific interface |
| `exec jss-check` | Check mobile device enrollment on JSS/JAMF |
| `exec mobile-device-manager` | Set mobile device manager parameters |
| `exec quick-track` | Quick Track |
| `exec ssh-client` | Secure Shell client |
| `exec tcp-service` | Test TCP service status |
| `exec user-group` | Execute a user-group command |

**Note:** Many `exec` subcommands that were expected from prior documentation (dns-query, ping, tracert, save-image, dnxp, radius-test, capwap-test, ntp-test, snmpwalk, iperf, iperf3) returned `unknown keyword or invalid input`. These may be available in different privilege modes or firmware versions. On this platform, `ping` and `tracert` are top-level commands, not under `exec`.

---

## 4. Save Commands

Commands under `save` for persisting configurations and transferring files.

### save (top-level subcommands)

| Command | Description |
|---------|-------------|
| `save ble` | Select the Bluetooth low energy device |
| `save ca-cert` | CA-certificate for server cert validation in cURL |
| `save capture` | Save packet capture file to remote server |
| `save config` | Save configuration (to remote, from remote, DRAM→flash) |
| `save dhcp-fingerprint` | Save DHCP fingerprint file for OS detection |
| `save icon-file` | Save icon file for OSU registration (max 64KB, JPG/PNG/BMP/GIF) |
| `save image` | Save IQ Engine image to the AP |
| `save private-client-group` | Save private client group from external server |
| `save radius-server-key` | Save RADIUS server certificate files |
| `save server-files` | Save cert/key files from DRAM to flash (persistent) |
| `save signature-file` | Remote image for L7 application |
| `save ssid` | Save locally stored SSID file to remote server |
| `save supplicant` | Save WPA supplicant files |
| `save thread` | Select the Thread device |
| `save track-action-cli` | Save CLI file from remote server |
| `save users` | Save private PSK configurations |
| `save vpn` | Save VPN certificate/private key file |
| `save web-page` | Save file for internal web server |
| `save web-server-key` | Save web server certificate files |

### save config subcommands

| Command | Description |
|---------|-------------|
| `save config <location>` | Save to tftp:// or scp:// |
| `save config <url>` | Save via http:// or https:// |
| `save config bootstrap` | Save bootstrap config to remote |
| `save config current` | Save current config to remote or to bootstrap |
| `save config running` | Save from running configuration |
| `save config users` | Save PPSK user accounts |

---

## 5. Debug Commands

| Command | Description |
|---------|-------------|
| `debug console` | Show debug messages on the console |

**Note:** Only `debug console` was accessible. The full debug subsystem may require elevated privileges or specific enable states.

---

## 6. Utility / Navigation Commands

| Command | Description |
|---------|-------------|
| `ping` | Perform a ping |
| `tracert` | Perform a traceroute |
| `exit` | Exit from the current mode |
| `quit` | Quit CLI |
| `no` | Remove a configuration or return to default |
| `load` | Load a configuration file |
| `reset` | Return configuration to defaults or reset web directory |
| `clear` | Clear dynamic system information or web directories |

---

## 7. Hidden / Underscore Commands

Discovered via `?` at the top-level prompt and recursive enumeration:

### `_system` — System Boot OS and TPM Management

| Command | Description |
|---------|-------------|
| `_system boot-os HOS` | Set boot OS to HiveOS (IQ Engine) — the current OS |
| `_system boot-os WiNG` | Set boot OS to WiNG (no restriction) |
| `_system boot-os WiNG-CAMP` | Set boot OS to WiNG Campus only |
| `_system boot-os WiNG-DIST` | Set boot OS to WiNG Distributed only |
| `_system tpm` | TPM (Trusted Platform Module) management |

**OS Conversion Procedure (IQ Engine → WiNG):**
```
_system boot-os WiNG
reboot
```
After the AP reboots into WiNG, use Wing CLI commands such as:
```
operational-mode centralized
```
Note: `operational-mode` is a **Wing CLI command**, not available in IQ Engine.

### `_debug-adspsensor` — ADSP Sensor Debug

| Command | Description |
|---------|-------------|
| `_debug-adspsensor alarm` | Specify log level for ADSP alarm module |
| `_debug-adspsensor apct` | Specify log level for ADSP apct module |
| `_debug-adspsensor aptest` | Specify log level for ADSP aptest module |
| `_debug-adspsensor aptl3` | Specify log level for ADSP aptl3 module |
| `_debug-adspsensor bluth` | Specify log level for ADSP bluth module |
| `_debug-adspsensor cfg` | Specify log level for ADSP cfg module |
| `_debug-adspsensor comms` | Specify log level for ADSP comms module |
| `_debug-adspsensor def` | Specify log level for ADSP def module |
| `_debug-adspsensor enet` | Specify log level for ADSP enet module |
| `_debug-adspsensor evt` | Specify log level for ADSP evt module |
| `_debug-adspsensor fasttm` | Specify log level for ADSP fasttm module |
| `_debug-adspsensor frpro` | Specify log level for ADSP frpro module |
| `_debug-adspsensor httpd` | Specify log level for ADSP httpd module |
| `_debug-adspsensor locn` | Specify log level for ADSP locn module |
| `_debug-adspsensor log` | Specify log level for ADSP log module |
| `_debug-adspsensor lview` | Specify log level for ADSP lview module |
| `_debug-adspsensor mac` | Specify log level for ADSP mac module |
| `_debug-adspsensor mem` | Specify log level for ADSP mem module |
| `_debug-adspsensor radio` | Specify log level for ADSP radio module |
| `_debug-adspsensor rcm` | Specify log level for ADSP rcm module |
| `_debug-adspsensor rfm` | Specify log level for ADSP rfm module |
| `_debug-adspsensor rfs` | Specify log level for ADSP rfs module |
| `_debug-adspsensor scan` | Specify log level for ADSP scan module |
| `_debug-adspsensor snoop` | Specify log level for ADSP snoop module |
| `_debug-adspsensor stats` | Specify log level for ADSP stats module |
| `_debug-adspsensor sys` | Specify log level for ADSP sys module |
| `_debug-adspsensor term` | Specify log level for ADSP term module |
| `_debug-adspsensor wepc` | Specify log level for ADSP wepc module |
| `_debug-adspsensor wipsess` | Specify log level for WIPS essentials module |

### Hidden `_` Prefix Probing Results

Systematic probing of `_a` through `_z` revealed the following:

| Prefix | Response | Interpretation |
|--------|----------|----------------|
| `_a` | Ambiguous input | Multiple hidden commands starting with `_a` |
| `_b` | unknown keyword | No hidden commands |
| `_c` | Ambiguous input | Multiple hidden commands (includes `_capwap_...`?) |
| `_d` | Ambiguous input | Multiple (includes `_debug-adspsensor`) |
| `_e` | (no output) | Possible hidden command executed silently |
| `_f` | Ambiguous input | Multiple hidden commands |
| `_g` | Ambiguous input | Multiple hidden commands |
| `_h` | Ambiguous input | Multiple hidden commands |
| `_i` | Ambiguous input | Multiple hidden commands |
| `_j` | unknown keyword | No hidden commands |
| `_k` | Ambiguous input | Multiple hidden commands |
| `_l` | Ambiguous input | Multiple hidden commands |
| `_m` | Incomplete command | Single hidden command exists |
| `_n` | Incomplete command | Single hidden command exists |
| `_o` | unknown keyword | No hidden commands |
| `_p` | Ambiguous input | Multiple hidden commands |
| `_q` | Incomplete command | Single hidden command exists |
| `_r` | Ambiguous input | Multiple hidden commands |
| `_s` | Ambiguous input | Multiple (includes `_system`) |
| `_t` | Ambiguous input | Multiple hidden commands |
| `_u` | Incomplete command | Single hidden command exists |
| `_v` | Incomplete command | Single hidden command exists |
| `_w` | Ambiguous input | Multiple hidden commands |
| `_x`–`_z` | unknown keyword | No hidden commands |

**Summary:** 19 out of 26 prefixes have hidden commands (Ambiguous or Incomplete). Only `_system` and `_debug-adspsensor` are visible in `?` help. The vast majority of hidden commands are engineering/debug commands not intended for customer use.

---

## 8. Negation Commands (`no` tree)

The `no` prefix removes/unsets configuration. Complete enumeration of `no ?`:

| Command | Description |
|---------|-------------|
| `no 802.1x-mac-table` | Unset 802.1X MAC table parameters |
| `no aaa` | Unset AAA parameters |
| `no access-console` | Unset access console parameters |
| `no acsp` | Unset ACSP parameters |
| `no admin` | Unset administrator parameters |
| `no adsp-server` | Remove ADSP server config |
| `no alg` | Unset ALG parameters |
| `no amrp` | Unset AMRP parameters |
| `no application` | Unset L7 related parameters |
| `no bonjour-gateway` | Unset Bonjour Gateway parameters |
| `no boot-param` | Unset boot loader parameters |
| `no cac` | Unset CAC parameters |
| `no capture` | Unset packet capture parameters |
| `no capwap` | Unset CAPWAP parameters |
| `no client-mode` | Unset wireless client parameters |
| `no client-monitor` | Unset Client Monitor parameters |
| `no clock` | Unset internal clock |
| `no config` | Unset configuration file parameters |
| `no console` | Unset console parameters |
| `no data-collection` | Unset data collection parameters |
| `no debug` | Disable debug messages |
| `no designated-server` | Unset dynamic server parameters |
| `no device-group` | Unset device group (Max: 64) |
| `no device-location` | Unset device location |
| `no dns` | Unset DNS parameters |
| `no domain-object` | Unset domain object (Max: 64) |
| `no exec` | Do not execute a command immediately |
| `no filter` | Unset capture filter parameters |
| `no forwarding-engine` | Unset forwarding engine parameters |
| `no ftm-policy` | Unset FTM policy |
| `no hive` | Remove hive or set hive parameters |
| `no hiveui` | Disable NetConfig UI |
| `no hostname` | Unset hostname |
| `no hotspot` | Unset hotspot parameters |
| `no interface` | Unset interface / EEE parameters |
| `no iot-esl-imagotag` | Unset IoT ESL parameters |
| `no ip` | Unset IP parameters |
| `no ip-policy` | Unset IP policy parameters |
| `no ipv6` | Unset IPv6 parameters |
| `no kddr` | Enable/disable kddr report |
| `no library-sip-policy` | Unset SIP policy |
| `no lldp` | Unset LLDP parameters |
| `no location` | Unset location tracking parameters |
| `no location-essentials` | Unset Location Essentials |
| `no logging` | Unset logging parameters |
| `no login` | Unset CLI login parameters |
| `no mac-object` | Unset MAC object (Max: 128) |
| `no mac-policy` | Unset MAC policy parameters |
| `no management` | Unset management service parameters |
| `no mdm-object` | Unset MDM object |
| `no mobile-device-policy` | Unset mobile device policy |
| `no mobility-policy` | Unset mobility policy |
| `no mobility-threshold` | Unset mobile user tunneling |
| `no net-access` | Unset internet measurement parameters |
| `no network-firewall` | Remove all L3 firewall rules |
| `no ntp` | Unset NTP parameters |
| `no os-detection` | Unset OS detection |
| `no os-object` | Unset OS object (Max: 64) |
| `no os-version` | Unset OS version detection |
| `no performance-sentinel` | Unset performance sentinel |
| `no presence` | Unset presence profile |
| `no qos` | Unset QoS parameters |
| `no radio` | Unset radio profile parameters |
| `no radsec-proxy` | Unset RadSec proxy |
| `no reboot` | Unset scheduled reboot |
| `no report` | Unset traffic statistics reporting |
| `no reset-button` | Disable reset button |
| `no roaming` | Unset roaming parameter |
| `no route` | Unset MAC address route |
| `no routing` | Unset routing parameters |
| `no rtts` | Remove RTTS session |
| `no schedule` | Unset schedule |
| `no sdr-profile` | Unset SDR profile |
| `no security` | Unset security parameters |
| `no security-object` | Unset security object |
| `no service` | Unset custom service |
| `no sflow` | Unset sFlow parameters |
| `no show` | Show settings/parameters |
| `no snmp` | Unset SNMP parameters |
| `no ssh-tunnel` | Unset SSH tunnel parameters |
| `no ssid` | Unset SSID parameters |
| `no supplicant` | Unset supplicant object |
| `no system` | Unset system / GPS parameters |
| `no teacher-view` | Unset TeacherView parameters |
| `no telegraf` | Unset telegraf parameters |
| `no time-object` | Unset time object |
| `no track` | Unset device tracking |
| `no track-wan` | Unset WAN tracking |
| `no usbmodem` | Unset USB modem parameters |
| `no usbport` | Unset USB port |
| `no user` | Remove user or change parameters |
| `no user-group` | Unset user group parameters |
| `no user-profile` | Unset user profile parameters |
| `no user-profile-policy` | Unset user profile mapping policy |
| `no validate_server_cert` | Unset server certificate validation |
| `no vlan-group` | Unset VLAN group |
| `no vpn` | Unset VPN parameters |
| `no web-directory` | Remove web directory |
| `no web-security-proxy` | Unset web security proxy |
| `no web-server-key` | Reset web server key to default |
| `no webui` | Unset WebUI |
| `no wips-essentials` | Unset WIPS Essentials |

---

## 9. Clear Commands

Commands under `clear` that remove dynamic/runtime data.

| Command | Description |
|---------|-------------|
| `clear aaa` | Clear AAA parameters |
| `clear application` | Clear L7 related parameters |
| `clear arp-cache` | Clear the ARP cache |
| `clear auth` | Clear dynamic authentication information |
| `clear ca-cert` | Clear uploaded CA-certificate(s) |
| `clear cac` | Clear CAC statistics |
| `clear capture` | Clear packet capture parameters |
| `clear capwap` | Clear CAPWAP statistics |
| `clear config` | Clear the configuration |
| `clear forwarding-engine` | Clear forwarding engine dynamic data |
| `clear gre-tunnel` | Clear GRE tunnel information |
| `clear hive` | Clear hive info |
| `clear icon-directory` | Remove OSU icon directory files |
| `clear interface` | Clear interface info/counters |
| `clear lldp` | Clear LLDP table |
| `clear location` | Clear location tracking parameters |
| `clear log` | Clear logging messages (buffered/debug/flash/all) |
| `clear mdnsd` | Clear MDNS information |
| `clear ndp-cache` | Clear NDP cache |
| `clear network-firewall` | Clear L3 firewall information |
| `clear qos` | Clear dynamic QoS information |
| `clear service` | Clear service dynamic information |
| `clear ssh` | Clear SSH known hosts |
| `clear ssid` | Clear SSID info/counters |
| `clear supplicant` | Clear supplicant objects |
| `clear user-and-group` | Clear all users and user-groups |
| `clear vpn` | Clear VPN information |
| `clear web-directory` | Remove all web directories |

---

## 10. Config Rollback Commands

| Command | Description |
|---------|-------------|
| `config version <number>` | Set configuration version number |
| `config rollback enable` | Enable configuration rollback |
| `config rollback capwap-disconnect [wait-time <n>]` | Rollback on CAPWAP disconnect |
| `config rollback next-reboot [wait-time <n>]` | Rollback on next reboot |
| `config rollback manual [wait-time <n>]` | Manual rollback with timer |
| `config rollback now` | Execute rollback immediately |
| `show config rollback` | Show rollback status |
| `clear config rollback` | Clear rollback point |
| `show config version` | Show current config version |
| `show config running` | Show running configuration |
| `show config {current\|backup\|bootstrap\|default\|failed}` | Show stored configs |

---

## 11. Output Filter Syntax

All `show` commands support output piping:

| Syntax | Description |
|--------|-------------|
| `show <cmd> \| include <word>` | Show only lines containing `<word>` |
| `show <cmd> \| exclude <word>` | Show only lines NOT containing `<word>` |
| `show <cmd> > <server>` | Redirect output to external server |

---

## 12. Deep Configuration Subcommand Trees (Phase 4)

Captured via recursive `<command> ?` traversal. Key families with subcommand counts:

### CAPWAP Configuration

| Subcommand | Description |
|------------|-------------|
| `capwap client enable` | Enable CAPWAP client |
| `capwap client server [backup] name <string>` | Set CAPWAP server |
| `capwap client server port <number>` | Set CAPWAP port |
| `capwap client dtls enable` | Enable DTLS encryption |
| `capwap client dtls bootstrap-passphrase <string>` | Set bootstrap passphrase |
| `capwap client dtls psk <string>` | Set DTLS pre-shared key |
| `capwap client dtls negotiation enable` | Enable DTLS negotiation |
| `capwap client dtls accept-bootstrap-passphrase` | Accept bootstrap passphrase |
| `capwap client dtls max-retries <number>` | Set max DTLS retries |
| `capwap client dtls handshake-wait-time <number>` | Set DTLS handshake timeout |
| `capwap client dtls session-delete-wait-time <number>` | Set session delete wait |
| `capwap client dtls hm-defined-passphrase <string> key-id <number>` | HM-defined passphrase |
| `capwap client discovery interval <number>` | Set discovery interval |
| `capwap client discovery maximum interval <number>` | Set max discovery interval |
| `capwap client discovery method {broadcast}` | Set discovery method |
| `capwap client default-server-name <string>` | Set default server |
| `capwap client join timeout <number>` | Set join timeout |
| `capwap client neighbor heartbeat interval <number>` | Set heartbeat interval |
| `capwap client neighbor dead interval <number>` | Set dead interval |
| `capwap client silent interval <number>` | Set silent interval |
| `capwap client statistic-info update-interval <number>` | Set stats interval |
| `capwap client vhm-name <string>` | Set VHM name |
| `capwap client pci-alert enable` | Enable PCI compliance alerts |
| `capwap client HTTP proxy name <string> port <number>` | Set HTTP proxy |
| `capwap max-discoveries counter <number>` | Set max discovery count |
| `capwap ping <string> [count <n>] [size <n>]` | CAPWAP ping |
| `capwap exec scp-user` | Execute SCP user setup |

### Interface Configuration (eth0)

| Subcommand | Description |
|------------|-------------|
| `interface <ethx> allowed-vlan {all\|auto\|<n>[-<n>]}` | Set allowed VLANs |
| `interface <ethx> bind <redx\|aggx>` | Bind to redundant/aggregate |
| `interface <ethx> client-monitor-policy <string>` | Assign client monitor policy |
| `interface <ethx> dhcp client` | Enable DHCP client |
| `interface <ethx> duplex {full\|half\|auto}` | Set duplex mode |
| `interface <ethx> eee enable` | Enable Energy Efficient Ethernet |
| `interface <ethx> fabric-attach vlan <n> isid <n>` | Set FA VLAN/ISID |
| `interface <ethx> gratuitous-arp disable` | Disable gratuitous ARP |
| `interface <ethx> inter-station-traffic` | Enable inter-station traffic |
| `interface <ethx> ip <ip_addr/netmask>` | Set IP address |
| `interface <ethx> ipv6 <ipv6_addr/mask>` | Set IPv6 address |
| `interface <ethx> link-discovery {lldp\|cdp}` | Set LLDP/CDP |
| `interface <ethx> mac-learning enable` | Enable MAC learning |
| `interface <ethx> manage {Telnet\|SSH\|SNMP\|ping\|all}` | Set management services |
| `interface <ethx> mode {bridge-802.1q\|backhaul\|wan}` | Set interface mode |
| `interface <ethx> native-vlan <number>` | Set native VLAN |
| `interface <ethx> private-client-group` | Set private client group |
| `interface <ethx> qos-classifier <string>` | Assign QoS classifier |
| `interface <ethx> qos-marker <string>` | Assign QoS marker |
| `interface <ethx> rate-limit {multicast\|broadcast\|unicast} <n>` | Set rate limits |
| `interface <ethx> security-object <string>` | Assign security object |
| `interface <ethx> shutdown` | Disable interface |
| `interface <ethx> speed {1000\|2500\|5000\|auto}` | Set speed |
| `interface <ethx> supplicant <string>` | Set 802.1X supplicant |

### Interface Configuration (wifi)

| Subcommand | Description |
|------------|-------------|
| `interface <wifix> mode {access\|backhaul\|dual\|wan-client\|sensor\|adsp-sensor}` | Set radio mode |
| `interface <wifix> radio channel <string>` | Set radio channel |
| `interface <wifix> radio power <number\|auto>` | Set transmit power |
| `interface <wifix> radio power-mode {lpi\|sp}` | Set power mode (6 GHz) |
| `interface <wifix> radio profile <string>` | Assign radio profile |
| `interface <wifix> radio range <number>` | Set radio range |
| `interface <wifix> radio sensitivity <number>` | Set radio sensitivity |
| `interface <wifix> radio tx-power-control <number\|auto>` | Set Tx power control |
| `interface <wifix> ssid <string>` | Assign SSID to radio |
| `interface <wifix> ssid <string> shutdown` | Disable SSID on radio |
| `interface <wifix> schedule <string>` | Set radio schedule |
| `interface <wifix> sdr-profile <string>` | Assign SDR profile |
| `interface <wifix> application-essentials profile <string>` | Set app essentials |
| `interface <wifix> presence profile <string>` | Set presence profile |
| `interface <wifix> dfs-dynamic-cost enable` | Enable DFS dynamic cost |
| `interface <wifix> link-discovery {lldp\|cdp}` | Set LLDP/CDP |
| `interface <wifix> radio-share mode {inline\|promisc}` | Set radio sharing |

### Interface Configuration (mgt0)

| Subcommand | Description |
|------------|-------------|
| `interface <mgtx> ip <ip_addr> <netmask>` | Set management IP |
| `interface <mgtx> ipv6 <ipv6_addr/mask> [eui-64]` | Set management IPv6 |
| `interface <mgtx> default-ip-prefix <ip_addr>` | Set default IP prefix |
| `interface <mgtx> dhcp client` | Enable DHCP client |
| `interface <mgtx> dhcp-server enable` | Enable DHCP server |
| `interface <mgtx> dhcp-server ip-pool <start> <end>` | Set DHCP pool |
| `interface <mgtx> dhcp-server options lease-time <n>` | Set DHCP lease time |
| `interface <mgtx> dhcp-server options default-gateway <ip>` | Set DHCP gateway |
| `interface <mgtx> dhcp-server options {dns1\|dns2\|dns3} <ip>` | Set DHCP DNS |
| `interface <mgtx> dns-server enable` | Enable DNS server |
| `interface <mgtx> ip-helper address <ip_addr>` | Set DHCP relay |
| `interface <mgtx> hive <string>` | Assign hive profile |
| `interface <mgtx> vlan <number>` | Set management VLAN |
| `interface <mgtx> native-vlan <number>` | Set native VLAN |
| `interface <mgtx> tag-native-vlan` | Enable native VLAN tagging |
| `interface <mgtx> mtu <number>` | Set MTU |

### Interface Configuration (thread/IoT)

| Subcommand | Description |
|------------|-------------|
| `interface <threadx> dataset networkkey <string>` | Set Thread network key |
| `interface <threadx> dataset networkname <string>` | Set Thread network name |
| `interface <threadx> dataset panid <string>` | Set Thread PAN ID |
| `interface <threadx> dataset extpanid <string>` | Set Thread extended PAN ID |
| `interface <threadx> dataset channel <number>` | Set Thread channel |
| `interface <threadx> prefix <ipv6_addr/mask>` | Set Thread prefix |
| `interface <threadx> enable` | Enable Thread interface |
| `interface <threadx> commissioner enable` | Enable Thread commissioner |
| `interface <threadx> nat64 enable` | Enable NAT64 |

### Ping / Tracert Syntax (from `show cmds`)

| Command | Full Syntax |
|---------|-------------|
| `ping` | `ping <ip_addr> [count <n>] [size <n>] [ttl <n>] [timeout <n>]` |
| `ping IPv6` | `ping <ipv6_addr> [interface <string>] [count <n>] [size <n>] [ttl <n>] [timeout <n>]` |
| `ping hostname` | `ping <string> [interface <string>] [count <n>] [size <n>] [ttl <n>] [timeout <n>]` |
| `tracert` | `tracert <ip_addr\|string> [max-hops <n>] [timeout <n>] [no-resolve]` |

### Reboot Syntax (from `show cmds`)

| Command | Full Syntax |
|---------|-------------|
| `reboot` | `reboot` (immediate) |
| `reboot image` | `reboot {backup\|current}` |
| `reboot scheduled` | `reboot date <date> time <time>` |
| `reboot offset` | `reboot offset <time>` |
| `reboot schedule daily` | `reboot schedule daily every <n> day(s) time <time> [variable <n>]` |
| `reboot schedule weekly` | `reboot schedule weekly every <n> week(s) {day} time <time> [variable <n>]` |

---

## CLI Syntax Patterns

### General Patterns
- `<command> ?` — Show available subcommands/parameters
- `<command> <subcommand> ?` — Recurse into help tree
- `Tab` — Command completion
- `no <command>` — Negate/remove configuration
- `<command> | <filter>` — Pipe output through filter
- `<command> > <server>` — Redirect output to external server
- Commands are **case-sensitive**

### Value Placeholders (from help output)
- `<cr>` — Command is complete, press Enter
- `<string>` — Free-form string value
- `<location>` — `tftp://` or `scp://` URI
- `<url>` — `http://` or `https://` URI
- `<IP>` — IPv4 address
- `<number>` — Numeric value (range specified in help)
- `***` — Masked/redacted value (passwords, keys)
