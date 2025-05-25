# FileVault Institutional Recovery Key (IRK)

This directory contains documentation and templates for generating and deploying a FileVault Institutional Recovery Key
 (IRK) certificate for macOS devices managed via Apple Business Manager (ABM).

## Purpose

The IRK allows organizations to maintain secure institutional access to encrypted macOS devices, as an alternative or
backup to personal recovery keys (PRKs). It is a critical part of MDM-based macOS deployment and recovery workflows.

## Contents

- `filevault-irk-template.md` — Full guide for generating the most compatible IRK certificate using XCA,
  Keychain Access, and OpenSSL.
- `filevault-irk.xca.md` — Step-by-step instructions for creating the certificate using XCA.
- `filevault-irk.keychainaccess.md` — GUI method using macOS Keychain Access.
- `filevault-irk.openssl.md` — Command-line method using OpenSSL.
- `filevault-irk.mobileconfig` — Sample configuration profile for deploying the IRK via MDM.

## Compatibility

Tested with:

- Apple Business Manager (ABM)
- Microsoft Intune
- JAMF Pro
- Hexnode

## Location

This file resides in:

```bash
sentinel/system-administration/mdm/apple-business-manager/filevault-irk/
```
