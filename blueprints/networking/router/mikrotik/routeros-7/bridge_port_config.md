# Bridge Port Configuration

## Introduction:
This table lists the key-value pairs required to add ports to a bridge in RouterOS 7. Ports must be added to a bridge to aggregate physical interfaces and virtual ports into a single broadcast domain.

## Order:
1. Bridge Creation and Basic Configuration
2. Bridge Port Configuration
3. VLAN Configuration on the Bridge
4. IP Address and DHCP Configuration
5. Firewall Configuration
6. Spanning Tree Protocol (STP) Configuration
7. Monitoring and Maintenance

## Link to MikroTik Wiki:
[RouterOS Bridge Port Interface](https://wiki.mikrotik.com/wiki/Manual:Bridge)

## Bridge Port Configuration Table:

| Key            | Value   | Description                                    |
|:---------------|:--------|:-----------------------------------------------|
| interface      |         | Name of the interface to include in the bridge |
| bridge         |         | Name of the bridge the port belongs to         |
| priority       |         | Port priority within the bridge                |
| path-cost      |         | STP path cost                                  |
| horizon        |         | Isolation horizon for loop prevention          |
| edge           |         | Mark port as edge (yes/no)                     |
| point-to-point |         | Treat port as point-to-point link (yes/no)     |
| comment        |         | Description or notes for the bridge port       |