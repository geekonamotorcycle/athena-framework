# Bridge Creation and Basic Configuration

## Introduction:
This table outlines the key-value pairs for creating and configuring a bridge in RouterOS 7. Bridge creation is the first step in setting up a Layer 2 network using MikroTik devices. The bridge acts as a virtual switch, aggregating multiple physical and virtual interfaces.

## Order:
1. Bridge Creation and Basic Configuration
2. Bridge Port Configuration
3. VLAN Configuration on the Bridge
4. IP Address and DHCP Configuration
5. Firewall Configuration
6. Spanning Tree Protocol (STP) Configuration
7. Monitoring and Maintenance

## Link to MikroTik Wiki:
[RouterOS Bridge Interface](https://wiki.mikrotik.com/wiki/Manual:Bridge)

## Bridge Creation and Basic Configuration Table:

| Key             | Value   | Description                                         |
|:----------------|:--------|:----------------------------------------------------|
| name            |         | Name of the bridge interface                        |
| comment         |         | Description or notes about the bridge               |
| mtu             |         | Maximum Transmission Unit (MTU)                     |
| arp             |         | ARP mode (enabled, proxy-arp, reply-only, disabled) |
| disabled        |         | Whether the bridge is enabled or disabled (yes/no)  |
| vlan-filtering  |         | Enable or disable VLAN filtering (yes/no)           |
| auto-mac        |         | Automatically set MAC address (yes/no)              |
| admin-mac       |         | Manually assign MAC address                         |
| fast-forward    |         | Enable hardware acceleration (yes/no)               |
| use-ip-firewall |         | Use IP firewall for bridge traffic (yes/no)         |
| igmp-snooping   |         | Enable IGMP snooping for multicast (yes/no)         |