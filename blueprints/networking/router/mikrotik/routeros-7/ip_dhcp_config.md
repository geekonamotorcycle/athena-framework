# IP Address and DHCP Configuration

## Introduction

This table lists the key-value pairs required to assign IP addresses and configure DHCP on a bridge in RouterOS 7.
Assigning IP addresses and configuring DHCP is necessary to enable dynamic IP allocation within the bridge network.

## Order

1. Bridge Creation and Basic Configuration
2. Bridge Port Configuration
3. VLAN Configuration on the Bridge
4. IP Address and DHCP Configuration
5. Firewall Configuration
6. Spanning Tree Protocol (STP) Configuration
7. Monitoring and Maintenance

## Link to MikroTik Wiki

[RouterOS IP Address Configuration](https://wiki.mikrotik.com/wiki/Manual:IP/Address)

## IP Address and DHCP Configuration Table

---

| Key         | Value | Description                                        |
| :---------- | :---- | :------------------------------------------------- |
| address     |       | IP address to assign to the bridge                 |
| netmask     |       | Subnet mask of the bridge                          |
| gateway     |       | Gateway IP for the bridge                          |
| dhcp-server |       | Enable DHCP server on the bridge (yes/no)          |
| lease-time  |       | Lease time for DHCP clients                        |
| dns-server  |       | DNS server for DHCP clients                        |
| pool        |       | Address pool for DHCP                              |
| dhcp-relay  |       | Enable DHCP relay (yes/no)                         |
| comment     |       | Description or notes for IP and DHCP configuration |

---
