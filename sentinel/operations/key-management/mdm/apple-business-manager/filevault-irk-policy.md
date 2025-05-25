# FileVault Institutional Recovery Key (IRK) – Key Management Policy

## Purpose

This document defines the operational lifecycle, backup, rotation, and storage requirements for the FileVault
Institutional Recovery Key (IRK) used in macOS device encryption.

This policy applies to all systems managed via Apple Business Manager and integrated with MDMs such as Microsoft Intune,
JAMF Pro, or Hexnode.

---

## 1. Key Classification

- **Key Type**: Institutional Recovery Key (IRK)
- **Key Format**: X.509v3, RSA 2048+ bit, Self-signed
- **Use Case**: Enable institutional access to FileVault-encrypted macOS devices

---

## 2. Key Generation Requirements

- Keys must be generated using a secure and documented process (see deployment template)
- Private keys must be protected by:
  - Password (if stored in `.p12`)
  - Vaulted storage (see Section 3)

---

## 3. Key Storage Policy

| Storage Type        | Description                                 | Frequency to Check |
| ------------------- | ------------------------------------------- | ------------------ |
| 🔐 Password Manager | Secure vault (e.g., KeePassXC, 1Password)   | Monthly            |
| 🧊 Offline Storage  | Encrypted USB or printout in fireproof safe | Quarterly          |
| 🗃️ Backup Archive   | Offline backup system (e.g., NAS snapshot)  | After changes      |

- No storage of private keys on general-access file shares
- Private key must **never be deployed to user endpoints**

---

## 4. Backup and Redundancy

- Minimum of **2 redundant secure backups** of the private key are required
- Validate backup integrity every **90 days**
- Perform test decryption every **6 months** on a non-production encrypted image

---

## 5. Rotation Schedule

| Event                             | Rotation Required? | Notes                        |
| --------------------------------- | ------------------ | ---------------------------- |
| Key Compromise or Exposure        | ✅ Yes             | Immediate key revocation     |
| Staff Offboarding (key custodian) | ✅ Yes             | Within 7 days                |
| Certificate Expiry Approaching    | ✅ Yes             | Rotate 90 days before expiry |
| Routine Maintenance               | ❌ Optional        | Every 2–3 years recommended  |

---

## 6. Key Custodianship

- At least **two authorized custodians** must have access to the private IRK
- Custodian list must be reviewed **semi-annually**
- Custodians must use MFA to access storage systems

---

## 7. Logging & Auditing

- All recovery events must be logged with:
  - Date/time
  - Device name/serial
  - Reason for access
  - Custodian name
- Audit logs must be retained for **7 years**

---

## 8. Decommissioning Process

- Upon expiration or rotation:
  - Revoke certificate in MDM profile
  - Remove key from all storage locations
  - Document rotation in key log
- Decommissioned keys must be securely deleted

---

## 9. References

- [NIST SP 800-57 Part 1 Rev. 5 – Key Management](https://csrc.nist.gov/publications/detail/sp/800-57-part-1/rev-5/final)
- Apple Platform Security: [FileVault Key Escrow](https://support.apple.com/guide/security/filevault-key-escrow-sec8ae49c727/web)

---

## Version History

| Version | Date       | Author         | Notes                                           |
| ------- | ---------- | -------------- | ----------------------------------------------- |
| 1.0     | 2025-05-25 | Joshua Porrata | Initial key management policy for FileVault IRK |
