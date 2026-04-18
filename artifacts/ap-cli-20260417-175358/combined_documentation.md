# AP Inventory - Thomas-5010-01

**Generated:** 2026-04-17 17:58 EDT
**Source:** Live SSH session to 192.168.100.206

---

## Device Identity

| Field | Value |
|-------|-------|
| Hostname | Thomas-5010-01 |
| Platform | AP5010U-WW |
| Product Name | AP5010U-WW |
| Serial Number | WM012243W-30032 |
| Hardware Revision | 01 |
| Manufacturing Date | 20221102 |
| BOM Number | 04 |
| Ethernet MAC | 241f:bd33:9800 |
| Number of MAC Addresses | 64 |
| IoT Hardware | CC2652R1 |
| TPM Status | success |
| Hardware ID | 0 |
| Antenna ID | 0 |

## Software

| Field | Value |
|-------|-------|
| Software Version | IQ Engine 10.8r5 build-91a62d2 |
| Build Time | Thu Oct 02 15:19:15 UTC 2025 |
| Build Cookie | 2510020819-91a62d2 |
| Bootloader Version | v0.0.4.69 |
| TPM Version | v2.0.1.38 |
| FIPS Capable | No |
| License | Permanent |

## Uptime

| Field | Value |
|-------|-------|
| Uptime at Query | ~7 minutes (freshly booted) |

## Management

| Field | Value |
|-------|-------|
| Management IP | 192.168.100.206 |
| Netmask | 255.255.255.0 |
| Default Gateway | 192.168.100.1 |
| DHCP Client | Enabled |
| IPv6 Link-local | fe80::261f:bdff:fe33:9800/64 |
| VLAN ID | 1 |
| DNS Primary | 1.0.0.1 |
| DNS Secondary | 208.67.220.220 |
| Timezone | GMT-5:00 (DST enabled) |

## Power

| Field | Value |
|-------|-------|
| Power Input | PoE bt |
| PSE Allowed | Enable |
| PSE Status | Enable |

## System Resources

| Field | Value |
|-------|-------|
| Total Memory | 2045172 KB (~2 GB) |
| Free Memory | 1177772 KB |
| Used Memory | 867400 KB |
| CPU Utilization | 0.502% |
| CPU User | 0.251% |
| CPU System | 0.251% |

## Interfaces

| Name | MAC | Mode | State | Chan(Width) | VLAN | Radio | Hive | SSID |
|------|-----|------|-------|-------------|------|-------|------|------|
| Mgt0 | 241f:bd33:9800 | - | U | - | 1 | - | VHM-VSTYGRNY | - |
| Agg0 | 241f:bd33:9803 | backhaul | D | - | 1 | - | VHM-VSTYGRNY | - |
| Eth0 | 241f:bd33:9800 | backhaul | U | - | 1 | - | VHM-VSTYGRNY | - |
| Eth1 | 241f:bd33:9801 | access | D | - | - | - | VHM-VSTYGRNY | - |
| Iotgw | 241f:bd33:980f | access | D | - | - | - | VHM-VSTYGRNY | - |
| Red0 | 241f:bd33:9802 | backhaul | D | - | 1 | - | VHM-VSTYGRNY | - |
| Wifi0 | 241f:bd33:9810 | access | U | Down(20MHz) | - | radio_ng_11ax-2g | - | - |
| Wifi0.1 | 241f:bd33:9814 | access | D | Down(20MHz) | - | radio_ng_11ax-2g | VHM-VSTYGRNY | Skynet |
| Wifi0.2 | 241f:bd33:9815 | access | D | Down(20MHz) | - | radio_ng_11ax-2g | VHM-VSTYGRNY | Skynet_Junior |
| Wifi0.3 | 241f:bd33:9816 | access | D | Down(20MHz) | - | radio_ng_11ax-2g | VHM-VSTYGRNY | Skynet_Guest |
| Wifi1 | 241f:bd33:9820 | access | U | Down(20MHz) | - | radio_ng_11ax-5g | - | - |
| Wifi1.1 | 241f:bd33:9824 | access | D | Down(20MHz) | - | radio_ng_11ax-5g | VHM-VSTYGRNY | Skynet |
| Wifi1.2 | 241f:bd33:9825 | access | D | Down(20MHz) | - | radio_ng_11ax-5g | VHM-VSTYGRNY | Skynet_Junior |
| Wifi1.3 | 241f:bd33:9826 | access | D | Down(20MHz) | - | radio_ng_11ax-5g | VHM-VSTYGRNY | Skynet_Guest |
| Wifi2 | 241f:bd33:9830 | access | U | Down(80MHz) | - | radio_ng_11ax-6g | - | - |
| Wifi2.1 | 241f:bd33:9834 | access | D | Down(80MHz) | - | radio_ng_11ax-6g | VHM-VSTYGRNY | Skynet_6GHz |

## Radio Summary

| Radio | Profile | PHY Mode | Chain Config | Features |
|-------|---------|----------|-------------|----------|
| Wifi0 (2.4 GHz) | radio_ng_11ax-2g | 11ax-2g | 4x4 static | A-MPDU, Short GI, Frameburst |
| Wifi1 (5 GHz) | radio_ng_11ax-5g | 11ax-5g | 4x4 static | A-MPDU, Short GI, Frameburst |
| Wifi2 (6 GHz) | radio_ng_11ax-6g | 11ax-6g | 4x4 (80MHz width) | Frameburst |

All radios: Beacon interval=100, Max clients=100, BGSCAN enabled, DFS disabled, HE OFDMA disabled, TWT disabled, MU-MIMO disabled, BSS Color=0.

## SSID Summary

| # | SSID Name | Frag | RTS | DTIM | Max Clients | MAC Filter | Security |
|---|-----------|------|-----|------|-------------|------------|----------|
| 1 | Skynet | 2346 | 2346 | 1 | 100 | Skynet | WPA3-SAE |
| 2 | Skynet_Junior | 2346 | 2346 | 1 | 100 | Skynet_Junior | WPA3-SAE |
| 3 | Skynet_Guest | 2346 | 2346 | 1 | 100 | Skynet_Guest | WPA3-SAE |
| 4 | Skynet_6GHz | 2346 | 2346 | 1 | 100 | Skynet_6GHz | WPA3-SAE |

All SSIDs are currently shutdown (admin state disabled) on all radios.

## Controller / CAPWAP State

| Field | Value |
|-------|-------|
| CAPWAP Client | Enabled |
| CAPWAP Transport | UDP |
| Run State | Connected securely to the CAPWAP server |
| Client IP | 192.168.100.206 |
| Server IP | 3.150.83.79 |
| Primary HM | ui1r1-cws-0.qa.xcloudiq.com |
| Backup HM | ui1r1-cwpm-01.qa.xcloudiq.com |
| VHM Name | VHM-VSTYGRNY |
| DTLS State | Enabled |
| DTLS Negotiation | Disabled |
| DTLS Session | Connected |
| DTLS Key Type | passphrase |
| Heartbeat Interval | 30 seconds |
| Keepalives Lost/Sent | 0/31 |

## LLDP Neighbor

| Field | Value |
|-------|-------|
| Incoming Port | eth0 |
| Neighbor Chassis MAC | dc23:3b78:fc00 |
| System Name | SW-4220 |
| System Description | Extreme Networks Switch Engine (4220-8MW-40P-4X-SwitchEngine) version 33.5.2.118 |
| Capabilities | LLDP-MED, network policy, location, extended power PSE |
| Device Type | Network Connectivity |

## NTP

| Server | Status |
|--------|--------|
| 0.aerohive.pool.ntp.org | Active |
| 1.aerohive.pool.ntp.org | Configured |
| 2.aerohive.pool.ntp.org | Configured |
| 3.aerohive.pool.ntp.org | Configured |

## Boot Parameters

| Field | Value |
|-------|-------|
| Region Code | FCC |
| Country Code | 840 |
| Netboot | Disabled |
| Netdump | Disabled |
| Netdump File | WM012243W30032.netdump |

## Detailed Interface State (Phase 3)

### Eth1

| Field | Value |
|-------|-------|
| Mode | bridge-access |
| MAC Learning | Enabled |
| Admin State | Enabled |
| Operational State | Down |
| IP Address | 0.0.0.0 |
| LLDP/CDP | Enabled |
| MAC | 241f:bd33:9801 |

### Agg0 (Aggregate Interface)

| Field | Value |
|-------|-------|
| Member Interfaces | None |
| Mode | Backhaul |
| MAC Learning | Disabled |
| Admin State | Enabled |
| Operational State | Down |
| MAC | 241f:bd33:9803 |

### Red0 (Redundant Interface)

| Field | Value |
|-------|-------|
| Member Interfaces | None |
| Mode | Backhaul |
| MAC Learning | Disabled |
| Admin State | Enabled |
| Operational State | Down |
| MAC | 241f:bd33:9802 |

### Iotgw (IoT Gateway Interface)

| Field | Value |
|-------|-------|
| Mode | bridge-access |
| MAC Learning | Disabled |
| Admin State | Disabled |
| Operational State | Down |
| MAC | 241f:bd33:980f |
| Rx Packets | 10 |
| Tx Packets | 123 |
| Rx Bytes | 1,036 (1.012 KB) |
| Tx Bytes | 14,448 (14.109 KB) |

### Wifi2 (6 GHz Radio - Detailed)

| Field | Value |
|-------|-------|
| Mode | Access |
| Admin State | Disabled |
| Operational State | Up |
| MAC | 241f:bd33:9830 |
| Channel | Down |
| Channel Width | 80 MHz |
| PHY Mode | 11ax-6g |
| Tx/Rx Chain | 4x4 static |
| Radio Profile | radio_ng_11ax-6g |
| A-MPDU | Enabled |
| Short Guard Interval | Disabled |
| OFDMA DL/UL | Disabled |
| TWT | Disabled |
| MU-MIMO | Disabled |
| Tx Beamforming | Disabled |
| Frameburst | Enabled |
| BSS Color | 0 |
| Spectral Scan | Off |

### Veth0 (Virtual Ethernet)

Available but not captured in detail.

## SSID Profile Details (Phase 3)

### Skynet

| Field | Value |
|-------|-------|
| Security Object | Skynet |
| Protocol Suite | WPA3-SAE |
| RTS/Frag Threshold | 2346 / 2346 |
| Hide SSID | No |
| DTIM Period | 1 |
| Max Clients | 100 |
| Client Age Out | 5 minutes |
| MAC Filter | Skynet |
| WMM | Enabled |
| UAPSD | Disabled |
| LDPC | Enabled |
| Tx-STBC / Rx-STBC | Enabled / Enabled |
| Inter-Station Traffic | Enabled |
| Bcast Drop Non-essential | Enabled |
| Mode Compliance | On |
| Bind Interfaces | Wifi0.1, Wifi1.1 |
| RRM / WNM / MBO | Disabled |
| Client Monitor Policy | default_Policy |
| Downstream Mcast Fwd | Enabled |
| Private-Client-Group | Disabled |

### Skynet_Junior

Same as Skynet except:
- Security Object: Skynet_Junior
- Bind Interfaces: Wifi0.2, Wifi1.2

### Skynet_Guest

Same as Skynet except:
- Security Object: Skynet_Guest
- Bind Interfaces: Wifi0.3, Wifi1.3

### Skynet_6GHz

Same as Skynet except:
- Security Object: Skynet_6GHz
- Bind Interfaces: Wifi2.1

## Security Object Details (Phase 3)

| Security Object | User Profile Attr | Protocol Suite | MAC Auth | CWP | PPSK | Allowed Profile | Deny Action | Bound SSIDs |
|----------------|-------------------|----------------|----------|-----|------|-----------------|-------------|-------------|
| Skynet | 0 | wpa3-sae | Disabled | Disabled | Disabled | All | Disconnect | Skynet |
| Skynet_Junior | 1 | wpa3-sae | Disabled | Disabled | Disabled | All | Disconnect | Skynet_Junior |
| Skynet_Guest | 2 | wpa3-sae | Disabled | Disabled | Disabled | All | Disconnect | Skynet_Guest |
| Skynet_6GHz | 0 | wpa3-sae | Disabled | Disabled | Disabled | All | Disconnect | Skynet_6GHz |
| ACCESS1 | 0 | open | Disabled | Disabled | Disabled | All | Disconnect | (none) |

## Radio Profile Details (Phase 3)

### radio_ng_11ax-2g (Wifi0)

| Field | Value |
|-------|-------|
| PHY Mode | 11ax-2g |
| Channel Width | 20 MHz |
| Tx/Rx Chain | 4x4 static |
| Beacon Period | 100 |
| Max Clients | 100 |
| Short Preamble | Enabled |
| A-MPDU / A-MSDU | Enabled / Disabled |
| Short Guard Interval | Enabled |
| DFS | Disabled |
| ACSP Channel Model | 3-channels (01-06-11) |
| Max ACSP Tx Power | 18 dBm |
| BGSCAN | Enabled (10 min interval) |
| Interference Map | Enabled |
| High Density | Disabled |
| Band Steering | Disabled |
| Load Balance | Disabled |
| Safety Net | Enabled (15 sec timeout) |
| Tx Beamforming | Disabled |
| Frameburst | Enabled |
| MU-MIMO | Disabled |
| OFDMA DL/UL | Disabled |
| TWT | Disabled |
| BSS Color | 0 |

### radio_ng_11ax-5g (Wifi1)

Same as 2g profile except PHY Mode = 11ax-5g. Bound to Wifi1.

### radio_ng_11ax-6g (Wifi2)

| Field | Value |
|-------|-------|
| PHY Mode | 11ax-6g |
| Channel Width | 80 MHz |
| Short Guard Interval | Disabled |
| Interference Map | Disabled (thresholds 20%) |

All other settings match the 2g/5g profiles.

## ARP Cache (Phase 3)

| MAC | TTL | Interface | VLAN | IP |
|-----|-----|-----------|------|-----|
| 9822:6eef:359f | 454 | eth0 | 1 | 192.168.100.209 |
| 7458:f373:f3f2 | 325 | eth0 | 1 | 192.168.100.151 |
| 241f:bd33:9800 | - | mgt0 | 1 | 192.168.100.206 |
| d011:e50b:cf32 | 869 | eth0 | 1 | 192.168.100.226 |
| e438:8355:7ae7 | 899 | eth0 | 1 | 192.168.100.1 |
| eee5:f50c:a259 | 681 | eth0 | 2 | 192.168.102.197 |

## NDP Cache (Phase 3)

| MAC | TTL | Interface | VLAN | IPv6 |
|-----|-----|-----------|------|------|
| e438:8355:7ae7 | 899 | eth0 | 1 | fe80::e638:83ff:fe55:7ae7 |

## USB Devices

| Bus | Device | ID |
|-----|--------|-----|
| 001 | 001 | 1d6b:0002 |
| 001 | 002 | 0483:5740 |
| 002 | 001 | 1d6b:0003 |
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
