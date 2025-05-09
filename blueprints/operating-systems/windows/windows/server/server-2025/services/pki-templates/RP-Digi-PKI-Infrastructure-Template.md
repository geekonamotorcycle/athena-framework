# RP Digi PKI Infrastructure

## Root Authority Management

### Ownership and Administrative Contacts

#### Root Owner

- **Name:** TBD *(Person ultimately responsible for the PKI infrastructure.)*
- **Day Phone:** TBD *(Primary daytime contact phone number.)*
- **Emergency Phone:** TBD *(Emergency contact number for urgent issues.)*
- **Email:** TBD *(Primary contact email.)*

#### Primary Administrator

- **Name:** TBD *(Day-to-day administrator for the Root Authority.)*
- **Day Phone:** TBD *(Primary daytime contact phone number.)*
- **Emergency Phone:** TBD *(Emergency contact number for urgent issues.)*
- **Email:** TBD *(Primary contact email.)*

#### Backup Administrator

- **Name:** TBD *(Backup administrator who manages PKI when primary admin is unavailable.)*
- **Day Phone:** TBD *(Primary daytime contact phone number.)*
- **Emergency Phone:** TBD *(Emergency contact number for urgent issues.)*
- **Email:** TBD *(Primary contact email.)*

*[Appendix A: Microsoft PKI Best Practices](#appendix-a-pki-best-practices)*

---

## Root Certificate Authority Details

### Root Key Information

- **Key Name:** TBD *(Descriptive name of the Root key.)*
- **Cipher:** TBD *(Cryptographic algorithm used, e.g., RSA 4096.)*
- **Serial Number:** TBD *(Serial number of the Root CA.)*
- **Creation Date:** TBD *(Initial creation date of Root CA.)*
- **Expiration Date:** TBD *(Expiration date of Root CA.)*

### Certificate Storage and Access

- **Root CA Server Name:** TBD *(Server name hosting the Root CA.)*
- **Domain Joined:** TBD *(True/False; indicates if the server is domain joined.)*
- **Offline Status:** TBD *(True/False; indicates if the server is offline for security.)*
- **Server MAC Address:** TBD *(MAC address of primary network interface.)*
- **Static IPv4 Address:** TBD *(Static IPv4 assigned to the server.)*
- **Static IPv6 Address:** TBD *(Static IPv6 assigned to the server.)*
- **Physical Location:** TBD *(Physical location of the server including rack and room.)*
- **Other Roles:** TBD *(Any other services or roles running on this server.)*

### Hardware Security Module (HSM)

- **Module Type:** TBD *(Type of HSM used, e.g., TPM, smartcard, USB token.)*
- **Module Location:** TBD *(Secure physical storage location of HSM.)*
- **Vault Access Coordinator:** TBD *(Person responsible for providing access to the HSM.)*

*[Appendix B: Microsoft Root CA Best Practices](#appendix-b-root-ca-best-practices)*

---

## Intermediate Certificate Authorities

### Intermediate CA 1

#### Intermediate Key Information

- **Key Name:** TBD *(Descriptive name of the intermediate key.)*
- **Cipher:** TBD *(Cryptographic algorithm used.)*
- **Serial Number:** TBD *(Intermediate CA serial number.)*
- **Common Name (CN):** TBD *(Common name for identification.)*
- **Subject Alternative Name (SAN):** TBD *(SAN associated with the CA.)*
- **Public Key:** TBD *(Public key information in readable format.)*
- **Passphrase Storage Location:** TBD *(Physical location of passphrase storage.)*
- **Certificate Expiration Date:** TBD *(Intermediate certificate expiration date.)*

#### Intermediate Server Details

- **Windows Server FQDN:** TBD *(Fully qualified domain name for Windows.)*
- **Linux Server FQDN:** TBD *(Fully qualified domain name for Linux.)*
- **Server MAC Address:** TBD *(MAC address of primary interface.)*
- **Static IPv4 Address:** TBD *(Assigned static IPv4 address.)*
- **Static IPv6 Address:** TBD *(Assigned static IPv6 address.)*
- **Other Roles:** TBD *(Other roles/services this server provides.)*
- **Certificate Usage:** TBD *(Specific certificate usages, e.g., email, SSL, user authentication.)*

*[Appendix C: Microsoft Intermediate CA Best Practices](#appendix-c-intermediate-ca-best-practices)*

---

## Operational Procedures

### Certificate Lifecycle Management

- **Issuance Procedures:** TBD *(Brief description with link to detailed documentation.)*
- **Renewal Procedures:** TBD *(Brief description with link to detailed documentation.)*
- **Revocation Procedures:** TBD *(Brief description with link to detailed documentation.)*

### Disaster Recovery and Backup

- **Backup Frequency:** TBD *(How often backups are taken.)*
- **Backup Storage Location:** TBD *(Physical or network location of backups.)*
- **Restoration Procedures:** TBD *(Link to detailed restoration instructions.)*

*[Appendix D: Microsoft Certificate Lifecycle Management](#appendix-d-certificate-lifecycle-management)*

---

## Logging, Monitoring, and Auditing

- **Log Location and Retention:** TBD *(Directory paths and retention periods.)*
- **Monitoring Tools:** TBD *(Tools or systems used for real-time monitoring.)*
- **Audit Frequency and Procedures:** TBD *(How often audits occur and basic procedure.)*

*[Appendix E: Microsoft Auditing Best Practices](#appendix-e-auditing-best-practices)*

---

## Appendix

### Appendix A: PKI Best Practices

- [Microsoft PKI Design Best Practices](https://learn.microsoft.com/en-us/windows-server/networking/core-network-guide/cncg/server-certs/overview-of-ad-certificate-services)

### Appendix B: Root CA Best Practices

- [Securing Offline Root CA](https://learn.microsoft.com/en-us/windows-server/networking/core-network-guide/cncg/server-certs/securing-root-ca)

### Appendix C: Intermediate CA Best Practices

- [Intermediate CA Design](https://learn.microsoft.com/en-us/windows-server/networking/core-network-guide/cncg/server-certs/ca-hierarchy)

### Appendix D: Certificate Lifecycle Management

- [Microsoft Certificate Management](https://learn.microsoft.com/en-us/windows-server/networking/core-network-guide/cncg/server-certs/manage-certificates)

### Appendix E: Auditing Best Practices

- [Auditing and Monitoring CA Activity](https://learn.microsoft.com/en-us/windows-server/networking/core-network-guide/cncg/server-certs/auditing-and-monitoring)

---
