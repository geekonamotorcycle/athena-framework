# FileVault IRK Creation Using macOS Keychain Access

## Steps

1. Open Keychain Access > Certificate Assistant > Create a Certificate
2. Identity Type: Self-signed Root
3. Certificate Type: Code Signing or Custom
4. Key Usage: Digital Signature, Key Encipherment
5. Export:
   - Public cert for MDM
   - Private key (.p12) stored securely
