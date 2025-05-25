# FileVault IRK Creation Using XCA

## Steps

1. Open XCA and create a new RSA private key (2048+ bit).
2. Create a self-signed certificate with:
   - Key Usage: Digital Signature, Key Encipherment
   - Extended Key Usage (optional): 1.2.840.113635.100.6.1.13
3. Export:
   - Public cert as .crt or .cer for MDM
   - Private key as .p12 and store securely

To Be Completed
