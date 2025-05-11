# VLAN Configuration on the Bridge

## Introduction

This table lists the key-value pairs required to configure VLANs on a bridge in RouterOS 7. VLAN configuration is
essential when segregating traffic within a single bridge. Tagged and untagged VLANs can be configured to manage
network segmentation.

## Order

1. Bridge Creation and Basic Configuration
2. Bridge Port Configuration
3. VLAN Configuration on the Bridge
4. IP Address and DHCP Configuration
5. Firewall Configuration
6. Spanning Tree Protocol (STP) Configuration
7. Monitoring and Maintenance

## Link to MikroTik Wiki

[RouterOS VLAN Configuration](https://wiki.mikrotik.com/wiki/Manual:Bridge_VLAN_Table)

## VLAN Configuration Table

---

| Key               | Value | Description                                                |
| :---------------- | :---- | :--------------------------------------------------------- |
| vlan-ids          |       | List of VLAN IDs the bridge will manage                    |
| tagged            |       | Interfaces that will be tagged                             |
| untagged          |       | Interfaces that will be untagged                           |
| pvid              |       | Default VLAN ID for untagged packets                       |
| ingress-filtering |       | Apply VLAN filtering on ingress (yes/no)                   |
| frame-types       |       | Frame admission policy (admit-all, admit-only-vlan-tagged) |
| comment           |       | Description or notes for the VLAN configuration            |

---
