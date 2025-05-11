# Firewall Configuration

## Introduction  

This table lists the key-value pairs required to set up firewall rules for a bridge in RouterOS 7. Firewall rules help
control traffic flow and secure the bridge from unauthorized access.

## Order

1. Bridge Creation and Basic Configuration
2. Bridge Port Configuration
3. VLAN Configuration on the Bridge
4. IP Address and DHCP Configuration
5. Firewall Configuration
6. Spanning Tree Protocol (STP) Configuration
7. Monitoring and Maintenance

## Link to MikroTik Wiki

[RouterOS Firewall Configuration](https://wiki.mikrotik.com/wiki/Manual:IP/Firewall)

## Firewall Configuration Table

---

| Key           | Value | Description                              |
| :------------ | :---- | :--------------------------------------- |
| chain         |       | Firewall chain (input, output, forward)  |
| action        |       | Action to perform (accept, drop, reject) |
| in-interface  |       | Incoming interface for the rule          |
| out-interface |       | Outgoing interface for the rule          |
| src-address   |       | Source IP address range                  |
| dst-address   |       | Destination IP address range             |
| protocol      |       | Protocol to match (tcp, udp, icmp)       |
| log           |       | Enable logging for the rule (yes/no)     |
| log-prefix    |       | Custom prefix for logged messages        |
| comment       |       | Description or notes for firewall rule   |

---
