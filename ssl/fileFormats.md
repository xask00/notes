# Certificate Containers
Way to store multiple certificates

## PEM 
Privacy enhanced mail, a failed to secure email but container format lives on.

Contianer format to store -
1. public certificate
2. multiple certificates public, provate, root certificate (entire chain)
x509 ASN.1 keys --> base64

## DER
ASN.1 keys in binary format, above PEM is in base64 format

## PKCS12
Microsoft format, became an RFC,
like PEM, but better
can contain private key

## PKCS7
open standard by java, does not contain private key

# Java
## Truststore vs keystore