# Spanning Tree Protocol (STP) Configuration

## Introduction:
This table lists the key-value pairs required to configure Spanning Tree Protocol (STP) in RouterOS 7. STP is essential for preventing loops in a network with redundant paths.

## Order:
1. Bridge Creation and Basic Configuration
2. Bridge Port Configuration
3. VLAN Configuration on the Bridge
4. IP Address and DHCP Configuration
5. Firewall Configuration
6. Spanning Tree Protocol (STP) Configuration
7. Monitoring and Maintenance

## Link to MikroTik Wiki:
[RouterOS STP Configuration](https://wiki.mikrotik.com/wiki/Manual:STP)

## Spanning Tree Protocol Configuration Table:

| Key             | Value   | Description                                              |
|:----------------|:--------|:---------------------------------------------------------|
| protocol-mode   |         | STP mode (none, rstp, mstp)                              |
| priority        |         | Bridge priority (lower is better)                        |
| forward-delay   |         | Delay before forwarding (seconds)                        |
| max-message-age |         | Maximum age of bridge messages                           |
| hello-time      |         | Interval between hello packets (seconds)                 |
| ageing-time     |         | Time to keep MAC addresses in the bridge table (seconds) |
| comment         |         | Description or notes for STP configuration               |