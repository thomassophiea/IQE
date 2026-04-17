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

## USB Devices

| Bus | Device | ID |
|-----|--------|-----|
| 001 | 001 | 1d6b:0002 |
| 001 | 002 | 0483:5740 |
| 002 | 001 | 1d6b:0003 |
