# FileVault Institutional Recovery Key (IRK) – Key Management Policy

## Purpose

This document defines the operational lifecycle, backup strategy, rotation schedule, and custodianship procedures for
the Institutional Recovery Key (IRK) used with macOS FileVault encryption. The IRK allows authorized personnel to unlock
encrypted systems in cases such as user loss of credentials, staff transitions, or forensic investigation.

This policy applies to all macOS systems enrolled through **Apple Business Manager** and managed via Mobile
Device Management (MDM) platforms, including but not limited to:

- Microsoft Intune
- JAMF Pro
- Hexnode

### Fill in the Blanks – Purpose

- [ ] List of active MDM platforms: ********\*\*\*\*********\_\_********\*\*\*\*********
- [ ] Target audience or team responsible for compliance: ****\*\*****\_****\*\*****

---

## 1. Key Classification

| Parameter  | Value                               |
| ---------- | ----------------------------------- |
| Key Type   | Institutional Recovery Key (IRK)    |
| Key Format | X.509v3, RSA 2048-bit or greater    |
| Use Case   | Secure recovery access to FileVault |

**Explanation:**  
The IRK is a cryptographic certificate that enables recovery access to FileVault-encrypted macOS devices. It is
distinct from user-specific recovery keys and is designed for enterprise-scale, institution-controlled recovery
workflows. Using an X.509 certificate standard ensures compatibility with Apple’s MDM
escrow systems.

### Fill in the Blanks – Key Classification

- [ ] Current certificate bit length: ****\*\*****\_\_****\*\*****
- [ ] Certificate serial number: ****\*\*\*\*****\_\_\_****\*\*\*\*****
- [ ] Expiration date: ******\*\*\*\*******\_\_\_\_******\*\*\*\*******

---

## 2. Key Generation Requirements

- Keys must be generated using a documented, secure, and repeatable process
- The private key must:
  - Be exported using strong encryption (e.g., password-protected `.p12`)
  - Never reside on unsecured or unmanaged systems
  - Be generated on a trusted, isolated machine if possible

**Why this matters:**  
Improperly generated or stored keys may be intercepted, reused by unauthorized personnel, or fail during critical
recovery. Secure generation ensures the IRK's trustworthiness and protects against malicious injection or tampering.

### Fill in the Blanks – Key Generation

- [ ] Link or location of SOP for key generation: ******\*\*******\_\_\_\_******\*\*******
- [ ] Name of system or machine used for generation: ******\*\*******\_******\*\*******
- [ ] Custodian responsible for generation: ********\*\*********\_********\*\*********

---

## 3. Key Storage Policy

| Storage Method   | Description                                            | Validation Frequency |
| ---------------- | ------------------------------------------------------ | -------------------- |
| Password Manager | Stored in an encrypted, MFA-protected password vault   | Monthly              |
| Offline Storage  | Saved to encrypted USB or printed and stored in a safe | Quarterly            |
| Backup Archive   | Snapshot stored on immutable or offline backup storage | After any changes    |

**Why this matters:**  
Redundant and segmented storage prevents single points of failure. Use of a password manager enables secure access
control, offline storage ensures protection from cyberattacks, and backup archives provide recovery options in case
of accidental deletion or vault corruption.

### Fill in the Blanks – Storage Inventory

- [ ] Vault Name or Software: ********\*\*\*\*********\_\_\_********\*\*\*\*********
- [ ] Storage Type (e.g., USB, NAS): ******\*\*\*\*******\_\_\_\_******\*\*\*\*******
- [ ] Physical Storage Location (e.g., Safe ID or Room): **\*\*\*\***\_**\*\*\*\***
- [ ] Custodian Name: **********\*\*\*\***********\_**********\*\*\*\***********
- [ ] Last Validation Date: ********\*\*\*\*********\_\_\_\_********\*\*\*\*********

---

## 4. Backup and Redundancy

- Maintain **at least two** secure, geographically or logically separate backups of the private key
- Perform **integrity verification** of all IRK backups every 90 days
- Conduct a **test decryption** of a non-production FileVault-encrypted volume every 6 months

**Why this matters:**  
Backups may become corrupted, deleted, or outdated. Routine integrity verification ensures the IRK remains usable. Test
decryption ensures procedural confidence in key application and toolchain readiness.

### Fill in the Blanks – Backup Schedule

- [ ] Number of distinct backup copies maintained: ****\*\*****\_\_\_****\*\*****
- [ ] Last backup validation date: ********\*\*********\_\_********\*\*********
- [ ] Last successful test decryption (date and device): **\*\*\*\***\_**\*\*\*\***

---

## 5. Rotation Schedule

| Trigger Event                   | Rotation Required? | Description                                 |
| ------------------------------- | ------------------ | ------------------------------------------- |
| Suspected or Confirmed Exposure | Yes                | Immediate revocation and rekeying           |
| Custodian Departure             | Yes                | Must rotate within 7 days                   |
| Certificate Nearing Expiry      | Yes                | Rotate 90 days before expiration            |
| Routine Lifecycle Maintenance   | Optional           | Recommended every 2–3 years if no incidents |

**Why this matters:**  
Cryptographic hygiene includes rotating keys when personnel leave, when certificates near expiry, or if compromise is
even suspected. This reduces risk of unauthorized use and limits the operational lifetime of any one key.

### Fill in the Blanks – Key Rotation

- [ ] Date of last key rotation: ********\*\*********\_\_********\*\*********
- [ ] Triggering event (if applicable): ******\*\*******\_\_\_\_******\*\*******
- [ ] Next planned rotation date: ********\*\*********\_********\*\*********
- [ ] Assigned custodian for upcoming rotation: ****\*\*****\_\_\_\_****\*\*****

---

## 6. Key Custodianship

- Assign **at least two custodians** with documented responsibilities
- Custodians must:
  - Use multi-factor authentication to access any IRK storage system
  - Not share credentials or allow unauthorized access
- Custodian list must be reviewed **every 6 months**

**Why this matters:**  
Having multiple custodians ensures redundancy while reducing the likelihood of a single point of compromise. MFA ensures
access is attributable and secured against phishing or credential reuse.

### Fill in the Blanks – Custodian Registry

- [ ] Custodian 1 – Name: **\*\*\*\***\_\_\_\_**\*\*\*\*** Email: **\*\*\*\***\_\_\_\_**\*\*\*\***
- [ ] Custodian 2 – Name: **\*\*\*\***\_\_\_\_**\*\*\*\*** Email: **\*\*\*\***\_\_\_\_**\*\*\*\***
- [ ] Additional Custodians (optional): ******\*\*\*\*******\_******\*\*\*\*******
- [ ] Date of last custodian list review: ******\*\*******\_\_\_******\*\*******

---

## 7. Logging and Auditing

All IRK usage must be logged in a system that captures:

- Date and time of access
- Device name and serial number
- Reason for access (e.g., user forgot password, incident response)
- Name of custodian performing the recovery

Logs must be stored for **no less than 7 years** to ensure availability for audits or legal requests.

**Why this matters:**  
Key usage must be accountable. Long-term auditability ensures compliance with data protection laws and internal infosec
standards.

### Fill in the Blanks – Logging and Audit Setup

- [ ] Logging system used (e.g., Splunk, Graylog): ****\*\*****\_\_\_****\*\*****
- [ ] Log retention policy duration: ******\*\*\*\*******\_\_\_\_******\*\*\*\*******
- [ ] Responsible team for log review: ******\*\*\*\*******\_******\*\*\*\*******

---

## 8. Decommissioning Process

Upon IRK expiration, exposure, or replacement:

1. **Revoke** the associated certificate from the MDM escrow profile
2. **Remove** all active storage instances (vaults, USBs, safes)
3. **Update** the IRK log to reflect the decommission event
4. **Securely destroy** all digital and physical instances

**Why this matters:**  
Expired or retired keys are a liability if improperly disposed of. Secure revocation ensures the IRK cannot be used on
future devices, and proper logging maintains traceability of key retirement actions.

### Fill in the Blanks – Decommission Record

- [ ] Decommissioned IRK serial number: ******\*\*\*\*******\_******\*\*\*\*******
- [ ] Date of revocation and removal: ******\*\*\*\*******\_\_\_******\*\*\*\*******
- [ ] Storage location(s) cleared: ********\*\*********\_\_********\*\*********
- [ ] Witness or verifying party: ********\*\*********\_\_\_********\*\*********

---

## 9. References

- [NIST SP 800-57 Part 1 Rev. 5 – Key Management Guidelines](https://csrc.nist.gov/publications/detail/sp/800-57-part-1/rev-5/final)
- [Apple Platform Security – FileVault Key Escrow](https://support.apple.com/guide/security/filevault-key-escrow-sec8ae49c727/web)

---

## Version History

| Version | Date       | Author         | Notes                                     |
| ------- | ---------- | -------------- | ----------------------------------------- |
| 1.0     | 2025-05-25 | Joshua Porrata | Initial baseline policy for FileVault IRK |
