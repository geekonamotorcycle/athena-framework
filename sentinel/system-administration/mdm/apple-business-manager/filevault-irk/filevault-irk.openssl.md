# FileVault IRK Creation Using OpenSSL

## Commands

```bash
openssl genrsa -out filevault-private.key 2048
openssl req -new -key filevault-private.key -out filevault.csr \
  -subj "/CN=FileVault Institutional/O=YourCompany/C=US"
openssl x509 -req -days 1825 -in filevault.csr -signkey filevault-private.key \
  -out filevault-public.crt
openssl pkcs12 -export -inkey filevault-private.key \
  -in filevault-public.crt -out filevault-irk.p12
```
