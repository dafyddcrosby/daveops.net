---
title: OpenSSL
---

## RSA key processing

```bash
# Generate a private key
openssl genrsa -out private_key.pem 2048
# Make a new public key
openssl rsa -pubout -in private_key.pem -out public_key.pem
# Get info on private key
openssl rsa -text -in private_key.pem
```

## Generate Certificate Signing Request

```bash
openssl req -new -key private_key.pem -out cert.csr
```

## Self-sign a certificate

```bash
openssl req -x509 -key private_key.pem -in cert.csr -out cert.crt
```

## Get certificate details

```bash
openssl x509 -in certificate.crt -text -noout
```

## Create a CA

```bash
# Create a root CA key
openssl genrsa -out rootCA.key 2048
# Create a self-signed CA certificate
openssl req -x509 -new -nodes -key rootCA.key -sha256 -days 365 -out rootCA.pem
# Sign a request
openssl x509 -req -in request.csr -CA rootCA.pem -CAkey rootCA.key -CAcreateserial -out requested.crt -days 500 -sha256
```

## Cross-signing certs with multiple CA's

* subject field must be identical
* keys must be identical




Testing an SNI certificate
--------------------------
	openssl s_client -servername example.com -connect example.com:443

