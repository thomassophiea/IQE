# Aerohive/Extreme Networks IQ Engine - Complete CLI Reference
## Device: AP5050D-WW | Software: IQ Engine 10.8r5

**Generated:** December 22, 2025
**Purpose:** Comprehensive CLI command reference including hidden commands

---

## Table of Contents
1. [Overview](#overview)
2. [Configuration Commands (Root Level)](#configuration-commands-root-level)
3. [Show Commands](#show-commands)
4. [Exec Commands](#exec-commands)
5. [Save Commands](#save-commands)
6. [Hidden/Debug Commands](#hiddendebug-commands)
7. [Common Utility Commands](#common-utility-commands)
8. [Tips and Best Practices](#tips-and-best-practices)

---

## Overview

This document provides a complete reference of all CLI commands available on Aerohive (now Extreme Networks) Access Points running IQ Engine 10.8r5. This includes:
- Standard configuration commands
- Monitoring and show commands
- Executive/action commands
- File save/load commands
- Hidden debugging commands (starting with `_`)

### CLI Access
- **Default Username:** admin
- **Default Password:** (varies by deployment)
- **Access Method:** SSH, Telnet (if enabled), Console

### Command Syntax
- Use `?` after any command to see available sub-commands and options
- Use `Tab` for command completion
- Use `no` before most commands to negate/remove configuration
- Commands are case-sensitive

---

## Configuration Commands (Root Level)

These commands are used to configure various aspects of the AP. Enter these at the root CLI prompt (`AFC-Outdoor-AP1#`).

### Network & Interface Configuration

#### `802.1x-mac-table`
Set parameters for the client MAC address table that is used to track the status of authenticated clients and those attempting authentication through 802.1X/EAP

#### `aaa`
Set parameters for AAA (authentication, authorization, accounting)

#### `access-console`
Set access console parameters

#### `alg`
Set ALG (Application Level Gateway) parameters

#### `interface`
Set interface parameters / Set Energy Efficient Ethernet

#### `ip`
Set IP parameters

#### `ipv6`
Set IPv6 parameters

#### `dns`
Set DNS (Domain Name System) parameters

#### `routing`
Set routing parameters

#### `route`
Set a MAC address route

#### `lldp`
Set LLDP (Link Layer Discovery Protocol) parameters

### Wireless & Radio Configuration

#### `acsp`
Set parameters for ACSP (Advanced Channel Selection Protocol)

#### `radio`
Set radio profile parameters

#### `ssid`
Set SSID (Service Set Identifier) parameters

#### `client-mode`
Set wireless client parameters for the local device so that it can associate with an access point

#### `client-load-balance`
Client load balancing parameters

#### `band-steering`
Band steering parameters in the WLAN

#### `high-density`
Parameters for optimizing performance in a high-density WLAN

#### `roaming`
Set roaming parameter

#### `amrp`
Set AMRP (Advanced Mobility Routing Protocol) parameters

### Security Configuration

#### `security`
Set the security parameters

#### `security-object`
Set parameters for a security object controlling network access through the SSIDs and Ethernet interfaces to which it is applied

#### `supplicant`
Set parameters for a supplicant object for HiveOS

#### `network-firewall`
Set a Layer 3 firewall policy (Max: 1024 rules per Aerohive device)

#### `wips-essentials`
WIPS Essentials feature

### User & Authentication

#### `admin`
Set the administrator parameters

#### `user`
Add one user or change user parameters

#### `user-group`
Set user group parameters

#### `user-profile`
Set parameters for a user profile

#### `user-profile-policy`
Set the user profile mapping policy

#### `login`
Set parameters for the CLI login

### Management & Monitoring

#### `hive`
Create a hive or set hive parameters

#### `hiveui`
Enable the NetConfig UI for defining network settings, configuring settings to connect to HiveManager, and uploading a new HiveOS image

#### `hivemanager`
HiveManager parameters

#### `hostname`
Set the hostname of the AP

#### `management`
Set management service parameters

#### `snmp`
Set SNMP (Simple Network Management Protocol) parameters

#### `logging`
Set logging parameters

#### `report`
Set the parameters for gathering traffic statistics and reporting them to HiveManager

#### `telegraf`
Set telegraf configuration parameters

### QoS & Performance

#### `qos`
Set QoS (Quality of Service) parameters

#### `cac`
Set CAC (Call Admission Control) parameters for regulating the admission of new VoIP calls

#### `performance-sentinel`
Set performance sentinel parameters to moderate client throughput

#### `forwarding-engine`
Set parameters to shape the behavior of the forwarding engine

### Application & Service Configuration

#### `application`
Set L7 related parameters

#### `service`
Set a custom service

#### `bonjour-gateway`
Set parameters for the device to act as a Bonjour Gateway, collecting, filtering, and sharing Bonjour services across subnets/VLANs

#### `hotspot`
Set hotspot parameters

#### `library-sip-policy`
Set a SIP (Standard Interchange Protocol) policy to apply a user profile, VLAN, and session length to library patrons accessing the wireless network

### Client & Device Management

#### `client-monitor`
Set parameters for Client Monitor

#### `client-tracing`
Test client tracing

#### `device-group`
Set a device group containing various objects that the HiveAP can use to classify client devices (Max: 64 groups)

#### `device-location`
Set the device location

#### `domain-object`
Set parameters for a domain object that the HiveAP can use to assign a client that belongs to a matching device domain to a user profile (Max: 64 domain objects per HiveAP)

#### `mac-object`
Set parameters for an MAC object that the HiveAP can use to assign a client with a matching MAC address to a user profile (Max: 128 MAC objects per HiveAP)

#### `os-object`
Set parameters for an OS object that the HiveAP can use to assign a client running a matching OS to a user profile (Max: 64 OS objects per HiveAP)

#### `os-detection`
Set the OS (Operating System) detection parameters

#### `os-version`
Set the OS (operating system) version you want to detect in the DHCP packets

#### `mdm-object`
Set the MDM (mobile device management) object

#### `mobile-device-policy`
Set a policy that assigns a user profile to traffic from a client based on the originally assigned user profile or the MAC address, device domain, and OS of the user's client

### Policy Configuration

#### `ip-policy`
Set IP policy parameters

#### `mac-policy`
Set MAC policy parameters

#### `mobility-policy`
Set parameters for a mobility policy

#### `mobility-threshold`
Set parameters for tunneling mobile user traffic

#### `filter`
Set packet capture filter parameters

### VPN & Tunneling

#### `vpn`
Set parameters for VPN (virtual private network) tunneling

#### `capwap`
Set parameters for CAPWAP (Control and Provisioning of Wireless Access Points)

#### `gre-tunnel`
GRE (Generic Routing Encapsulation) tunnel parameters

#### `ssh-tunnel`
Set SSH (Secure Shell) tunnel parameters so that Extreme Technical Support can access the AP remotely

#### `radsec-proxy`
Set parameters for RadSec proxy servers which communicate with ID Manager over a secure TLS tunnel

### Data Collection & Analytics

#### `data-collection`
Set parameters for collecting data about the types and capabilities of devices on the network and the types of applications and IP protocols they use

#### `location`
Set parameters for location tracking

#### `location-essentials`
Location Essentials feature

#### `presence`
Set presence profile parameters

#### `ftm-policy`
Set parameters for FTM (Fine Time Measurement) policy

### Network Services

#### `ntp`
Set NTP (Network Time Protocol) parameters

#### `clock`
Set the internal clock

#### `dhcp`
DHCP parameters

#### `web-directory`
Create a web directory for the internal web server

#### `web-security-proxy`
Proxy HTTP and HTTPS traffic bound for the Internet to a web security server for filtering / Set web security proxy service

#### `webui`
Set the WebUI on the HiveAP for local hive administration

### Advanced Features

#### `iot-esl-imagotag`
Set iot-esl-imagotag parameters

#### `sdr-profile`
Set SDR (Software Defined Radio) profile parameters

#### `teacher-view`
Set parameters for TeacherView, a tool for controlling student access to the network and monitoring their activity

#### `probe`
Set the probe parameters

#### `sflow`
Set sflow related parameters

### System Configuration

#### `system`
Set system parameters

#### `boot-param`
Set parameters for the boot loader

#### `config`
Set parameters for the current configuration file, which is a flash file containing default and admin-defined settings

#### `console`
Set console parameters

#### `license`
Set license parameters

#### `reset-button`
Enable the reset button on the AP chassis to reset the AP config

#### `validate_server_cert`
Set the validation of the server certificate parameter

### Scheduling

#### `schedule`
Set a schedule to control the application of user profiles and the availability of SSIDs

#### `time-object`
Set a time object

### USB & Hardware

#### `usbmodem`
Set parameters of usbmodem

#### `usbport`
Set the USB port

#### `pse`
Set PSE (power sourcing equipment) power management parameters

### Testing & Diagnostics

#### `capture`
Set packet capture parameters

#### `iperf`
Set parameters for Iperf2, a tool for testing and measuring network performance

#### `iperf3`
Set parameters for Iperf3, a tool for testing and measuring network performance

#### `track`
Set parameters to track the reachability of one or more devices on the network

#### `track-wan`
Set parameters to track the reachability of one or more devices through the WAN interface

#### `net-access`
Set parameters to measure the internet available and latency

#### `rtts`
Create RTTS (Real Time Trouble Shooting) session

### Miscellaneous

#### `adsp-server`
Set ADSP server ip address

#### `designated-server`
Set parameters for a dynamic server

#### `history`
Set the capacity for command history

#### `vlan-group`
Set a VLAN group

#### `kddr`
Enable/disable the kddr report to HM

#### `debug`
Enable debug messages

#### `reboot`
Set the system to scheduled reboot state

#### `reset`
Return the configuration to its default settings or the files in a web directory to the default file set

#### `fabric-attach`
Fabric attach configuration

### Control Commands

#### `exec`
Execute a command to initiate a task immediately

#### `show`
Show settings, parameters, or dynamically generated information

#### `save`
Save a configuration, HiveOS image, RADIUS database, or files

#### `load`
Load a configuration file

#### `clear`
Clear dynamic system information or remove all web directories

#### `no`
Remove a configuration or return to a default setting

#### `exit`
Exit from the current mode

#### `quit`
Quit CLI (Command Line Interface)

---

## Show Commands

Display system information, status, and configuration. All commands start with `show`.

### Authentication & Security

#### `show 802.1x-mac-table`
Show the MAC table used for 802.1X/EAP user authentication on an Ethernet interface

#### `show aaa`
Show parameters for AAA (authentication, authorization, accounting)

#### `show auth`
Show authentication parameters per interface

#### `show ca-cert`
Show all CA certificates that the local AP uses to validate the server certificate in cURL command, or specific certificate content and expiration/start time

#### `show security`
Show security parameters

#### `show security-object`
Show security object names and individual parameters

#### `show supplicant`
Show supplicant parameters

#### `show idm`
Show ID Manager information

#### `show icsa`
Show ICSA (International Computer Security Association) parameters

### System Information

#### `show system`
Show system information

#### `show version`
Show information about the current and backup IQ Engine versions on the HiveAP and the HiveAP platform type

#### `show hw-info`
Show hardware information

#### `show clock`
Show the date, time of the internal clock

#### `show cpu`
Show the percentage of the CPU used in total, for system operations, and for processing user traffic

#### `show memory`
Show total, free, and used system memory statistics

#### `show boot-param`
Show boot parameter information

#### `show license`
Show license information

### Configuration & Running State

#### `show running-config`
Show currently running configurations

#### `show config`
Show parameters for the current configuration file

#### `show cmds`
Show CLI (Command Line Interface) commands including ones derived from optional keywords

#### `show history`
Show command history

### Network & Interfaces

#### `show interface`
Show interface and subinterface parameters

#### `show ip`
Show IP parameters

#### `show ipv6`
Show IPV6 parameters

#### `show dns`
Show DNS (Domain Name System) parameters

#### `show route`
Show route parameters

#### `show routing`
Show routing parameters

#### `show arp-cache`
Show arp cache table

#### `show ndp-cache`
Show ndp cache table

#### `show lldp`
Show LLDP (Link Layer Discovery Protocol) parameters

#### `show l3`
Show Layer 3 information

### Wireless & Radio

#### `show radio`
Show radio profile parameters

#### `show ssid`
Show SSID (Service Set Identifier) profile names and individual profile parameters

#### `show client-mode`
Show client mode settings

#### `show acsp`
Show parameters for ACSP (Advanced Channel Selection Protocol)

#### `show roaming`
Show the roaming cache and neighbors

#### `show band-steering`
Show parameters for band steering in the WLAN

#### `show high-density`
Show parameters for optimizing performance in a high-density WLAN

#### `show client-load-balance`
Show parameters for client load balancing in the WLAN

### Client & Station Information

#### `show station`
Show information about all stations or about the ongoing wireless activity of a specific station

#### `show client-monitor`
Show Client Monitor parameters

#### `show client-info-collection`
Show client information collection result

#### `show private-client-group`
Show parameters for private client groups

#### `show ppsk`
Show parameters of private-PSK

### Management

#### `show admin`
Show admin parameters

#### `show hive`
Show hive parameters

#### `show hivemanager`
Show HiveManager parameters

#### `show hiveui`
Show settings of the NetConfig UI

#### `show management`
Show management service parameters

#### `show access-console`
Show access console status and parameters

#### `show console`
Show console parameter

#### `show snmp`
Show SNMP (Simple Network Management Protocol) parameters

#### `show logging`
Show logging information

#### `show report`
Show report parameters for traffic statistics

#### `show telegraf`
Show all telegraf configurations

### Application & Services

#### `show application`
Show L7 information

#### `show application-essentials`
Show Application Essentials parameters

#### `show service`
Show details or counters about predefined and custom services

#### `show bonjour-gateway`
Show the settings and status of the Bonjour gateway

#### `show mdnsd`
Show MDNS daemon information

#### `show hotspot`
Show a list of hotspot profiles or information about a specific hotspot profile

### QoS & Performance

#### `show qos`
Show QoS (Quality of Service) parameters

#### `show cac`
Show CAC (Call Admission Control) parameters

#### `show performance-sentinel`
Show performance sentinel parameters

#### `show forwarding-engine`
Show forwarding engine parameters

#### `show alg`
Show ALG (Application Level Gateway) information

#### `show amrp`
Show AMRP (Advanced Mobility Routing Protocol) parameters

### VPN & Tunneling

#### `show vpn`
Show VPN information and VPN objects

#### `show capwap`
Show the settings and current status for CAPWAP

#### `show gre-tunnel`
Show GRE (Generic Routing Encapsulation) tunnel information

#### `show ssh-tunnel`
Show SSH (Secure Shell) tunnel parameters

#### `show radsec`
Show RadSec proxy information

### Security & Firewall

#### `show network-firewall`
Show all rules in the Layer 3 firewall policy

#### `show wips-essentials`
Show WIPS Essentials parameters

#### `show web-security-proxy`
Show the web security proxy configuration

### Users & Policies

#### `show user`
Show all user

#### `show user-group`
Show a user group parameters

#### `show user-profile`
Show parameters for a user profile

#### `show user-profile-policy`
Show parameters for a user profile mapping policy

#### `show user-profile-schedule`
Show the status of all user profile schedules

#### `show min-password-length`
Show the minimum password length

#### `show device-group`
Show all device group names or the settings of an individual device group

#### `show domain-object`
Show all domain object names or the device domains assigned to an individual domain object

#### `show mac-object`
Show all MAC object names or the parameters of an individual MAC object

#### `show os-object`
Show all OS object names or the operating systems assigned to an individual OS object

#### `show os-detection`
Display the OS (Operating System) detection configuration

#### `show mdm-object`
Show MDM object information

#### `show mobile-device-policy`
Show all mobile device policy names or the settings of an individual policy

### Policies

#### `show ip-policy`
Show parameters for IP policy

#### `show mac-policy`
Show parameters for MAC policy

#### `show mobility-policy`
Show the parameters of all mobility policies

#### `show mobility-threshold`
Show the settings for tunneling mobile user traffic

#### `show library-sip-policy`
Display library SIP policy settings

### Monitoring & Diagnostics

#### `show capture`
Show packet capture parameters

#### `show filter`
Show capture filter parameters

#### `show data-collection`
Show parameters for collecting data about the types and capabilities of devices on the network and their network usage

#### `show track`
Show IP tracking information

#### `show track-wan`
Show Wan interface IP tracking information

#### `show proxy`
Show proxy parameters

#### `show sflow`
Show sflow related parameters

### Location & Presence

#### `show location`
Show parameters for location tracking

#### `show location-essentials`
Location Essentials information

#### `show presence`
Show presence profile parameters

#### `show ftm`
Show the parameters for FTM neighbors

#### `show ftm-policy`
Show the parameters of all FTM (Fine Time Measurement) policies or one specified policy

### Scheduling

#### `show schedule`
Show information about previously defined schedules

#### `show schedule-in-detail`
Show detailed information about all previously defined schedules

#### `show ssid-schedule`
Show the status of all SSID schedules

#### `show time-zone`
Show time zone

### NTP & Time

#### `show ntp`
Show NTP (Network Time Protocol) parameters

### Web & Files

#### `show web-directory`
Show the files in a web directory

#### `show web-server-key`
Show web server key files information

#### `show icon-directory`
Show a list of icon directories or the contents of a single directory

### IoT & Special Features

#### `show iot-esl-imagotag`
Show iot-esl-imagotag setting parameters

#### `show sdr-profile`
Show SDR (Software Defined Radio) profile parameters

#### `show teacher-view`
Show parameters for TeacherView

#### `show fabric-attach`
Show fabric attach information

### USB & Hardware

#### `show usb-device`
Show information about the internal USB hub and any device connected to the USB port

#### `show usbmodem`
Show parameters of usbmodem

#### `show pse`
Show PSE (power sourcing equipment) power management parameters

### Reboot & Status

#### `show reboot`
Show if the system is scheduled to reboot

#### `show reset-button`
Show the state of reset button to reset the AP

### Advanced/Other

#### `show rtts`
Show RTTS information

#### `show video`
Show information about streaming video traffic

#### `show vlan-group`
Show the settings and status of VLAN groups

#### `show wan`
Show brd wan info

#### `show adsp-server`
Show information about ADSP Server

#### `show tech`
Show the output of many "show" commands that display all the important settings and runtime data

---

## Exec Commands

Execute immediate actions and tasks. All commands start with `exec`.

### AAA & Authentication

#### `exec aaa`
Set parameters for AAA (authentication, authorization, accounting)

#### `exec auth`
Execute an auth module command

### Testing & Monitoring

#### `exec antenna-alignment`
Set parameters for aligning a directional or sectional antenna connected to a radio in backhaul or dual mode with a specified peer

#### `exec client-monitor`
Monitor the activities of a client

#### `exec tcp-service`
Test TCP service status

#### `exec quick-track`
Quick Track

### Mobile Device Management

#### `exec aerohive-check`
Check the enrollment status of a mobile device on the Aerohive MDM server

#### `exec airwatch-check`
Check the enrollment status of a mobile device on the AirWatch

#### `exec jss-check`
Check the enrollment status of a mobile device on the JSS (JAMF software server)

#### `exec mobile-device-manager`
Set the mobile device manager parameters

### Data Collection

#### `exec data-collection`
Perform an action on the data collected about the types and capabilities of devices on the network

### Packet Capture

#### `exec capture`
Initiate packet capturing

### Network Tools

#### `exec interface`
Execute the command through a specific interface

#### `exec ssh-client`
Secure Shell client

### Security & Access

#### `exec bypass-wan-hardening`
Disable WAN hardening to allow SSH, Telnet, and the remote sniffer tool to access the device over the WAN interface (Note: To restore WAN hardening, enter "no exec bypass-wan-hardening" or reboot)

### System Operations

#### `exec delay-execute`
Delay the execution of commands for a period of time (Note: This does not affect "show" commands)

#### `exec active-alarms-resending`
Make device resend all active alarms to HiveManager

#### `exec ftm`
Trigger an FTM neighbor list update

### User Groups

#### `exec user-group`
Execute a user-group command

---

## Save Commands

Save configurations and files. All commands start with `save`.

### Configuration Files

#### `save config`
Save a configuration from the HiveAP to a remote server, from a remote server to the HiveAP, or from DRAM to flash as the current or bootstrap config

### Certificates & Keys

#### `save ca-cert`
CA-certificate for validating the server certificate in cURL command during HTTPS session

#### `save radius-server-key`
Save certificate files for the local Aerohive RADIUS server to use

#### `save server-files`
Save certificate and private key files used by the internal web and RADIUS servers and VPN from DRAM to flash memory for persistent storage after reboots (Note: For security reasons, these files are saved only in DRAM by default)

#### `save vpn`
Save a VPN certificate or private key file

#### `save web-server-key`
Save certificate files for the internal web server to use

#### `save supplicant`
Save files for wpa supplicant

### Images & Software

#### `save image`
Save a IQ Engine image to the HiveAP

#### `save signature-file`
Remote image used for L7 application

### Files & Content

#### `save capture`
Save a packet capture file stored locally to a remote server

#### `save dhcp-fingerprint`
Save a fingerprint file of DHCP options for client OS detection

#### `save icon-file`
Save an icon file for an OSU (Online Signup) registration server (Max file size: 64 KB, formats: JPG, PNG, BMP, GIF)

#### `save ssid`
Save a locally stored file to a remote server

#### `save web-page`
Save a file for use with the internal web server

#### `save track-action-cli`
Save an admin-defined CLI file from a remote server to the local device

### User & Client Data

#### `save users`
Save private PSK (preshared key) configurations

#### `save private-client-group`
Save private client group information from an external server to the local device

### IoT Devices

#### `save ble`
Select the Bluetooth low energy device

#### `save thread`
Select the Thread device

---

## Hidden/Debug Commands

These commands are not displayed in standard help output and are intended for debugging and advanced troubleshooting.

### `_debug-adspsensor`
Enable debug feature for adsp sensor

**⚠️ WARNING:** Hidden commands are typically used by support personnel and developers. Use with caution as they may affect system stability or produce unexpected results.

---

## Common Utility Commands

### Navigation & Help

- **`?`** - Display context-sensitive help
- **`Tab`** - Auto-complete commands and parameters
- **`history`** - View command history
- **`exit`** - Exit current mode or CLI
- **`quit`** - Quit the CLI session

### Network Testing

#### `ping`
Perform a ping test to check network connectivity

**Usage:**
```
ping <ip-address|hostname>
```

#### `tracert` / `traceroute`
Perform a traceroute to trace the path packets take to a destination

**Usage:**
```
tracert <ip-address|hostname>
```

### Configuration Management

#### `load`
Load a configuration file

#### `clear`
Clear dynamic system information or remove all web directories

**Common uses:**
- `clear arp-cache`
- `clear session`

#### `reset`
Return the configuration to its default settings or reset files in a web directory

**⚠️ WARNING:** This will erase custom configurations!

#### `reboot`
Reboot the Access Point

**Usage:**
```
reboot
```

Or schedule a reboot:
```
reboot <time>
```

### Configuration Modifier

#### `no`
Negate or remove a configuration setting

**Usage:**
```
no <command>
```

**Examples:**
```
no interface mgt0 ip 192.168.1.1
no ssid "Guest-WiFi"
```

---

## Tips and Best Practices

### 1. Always Save Your Configuration
After making changes, remember to save:
```
save config
```

### 2. Use Tab Completion
Press `Tab` to auto-complete commands and see available options.

### 3. Context-Sensitive Help
Type `?` at any point to see available commands or parameters:
```
AFC-Outdoor-AP1# ?
AFC-Outdoor-AP1# interface ?
AFC-Outdoor-AP1# interface mgt0 ?
```

### 4. Verify Before Applying
Use `show` commands to verify current configuration before making changes:
```
show running-config
show interface
show ssid
```

### 5. Use "show tech" for Troubleshooting
When working with support, use:
```
show tech
```
This displays comprehensive system information.

### 6. Configuration Backup
Regularly backup your configuration:
```
save config <remote-server-details>
```

### 7. Review Changes Before Saving
The system will prompt you to save changes when exiting. Review what changed:
```
show running-config
```

### 8. Hidden Commands Caution
Hidden commands (starting with `_`) should only be used when:
- Directed by support personnel
- You fully understand the implications
- In a lab/test environment

### 9. Command Abbreviation
The CLI accepts abbreviated commands as long as they're unambiguous:
```
sh ver          (instead of: show version)
conf t          (instead of: config)
```

### 10. Schedule Maintenance Windows
For production APs, schedule reboots and major changes during maintenance windows:
```
reboot <date-time>
```

---

## Quick Reference Card

### Most Common Commands

| Task | Command |
|------|---------|
| View system info | `show system` |
| View software version | `show version` |
| View running config | `show running-config` |
| View SSID list | `show ssid` |
| View connected clients | `show station` |
| View interface status | `show interface` |
| Ping test | `ping <ip>` |
| Trace route | `tracert <ip>` |
| Save configuration | `save config` |
| Reboot AP | `reboot` |
| View CPU usage | `show cpu` |
| View memory usage | `show memory` |
| Get all system info | `show tech` |

### Common Configuration Tasks

| Task | Command |
|------|---------|
| Set hostname | `hostname <name>` |
| Set IP address | `interface mgt0 ip <ip> netmask <mask>` |
| Create SSID | `ssid <name>` |
| Set admin password | `admin <username> password <password>` |
| Enable NTP | `ntp server <ip>` |
| Remove config | `no <command>` |

---

## Support & Resources

For additional help:
- **Extreme Networks Documentation**: https://www.extremenetworks.com/support/documentation/
- **Support Portal**: https://extremeportal.force.com/
- **Community Forums**: https://community.extremenetworks.com/

---

*This documentation was generated from an AP5050D-WW running IQ Engine 10.8r5 build-be10b29*

*For the most up-to-date information, always refer to the official Extreme Networks documentation for your specific software version.*

**Document Version:** 1.0
**Last Updated:** December 22, 2025
