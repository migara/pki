# README #


### What is this repository for? ###

* Quick PKI setup

### Dependencies ###

* OpenSSL

### Folder Structure ###


```
#!python

.
├── certs
│   └── ca.cert.pem
├── crl
├── index.txt
├── intermediate
│   ├── certs
│   │   ├── ca-chain.cert.pem
│   │   ├── client1.cert.pem
│   │   └── www.example.com.cert.pem
│   ├── crl
│   │   └── intermediate.crl.pem
│   ├── csr
│   │   ├── client1.csr.pem
│   │   └── www.example.com.csr.pem
│   ├── index.txt
│   ├── newcerts
│   │   ├── 1000.pem
│   ├── openssl.cnf
│   ├── private
│   │   ├── client1.key.pem
│   │   └── www.example.com.key.pem
│   ├── serial
├── newcerts
│   └── 1000.pem
├── openssl.cnf
├── private
│   └── ca.key.pem
├── serial
```

### How to genrate a client certificate ###


```
#!python

cd intermediate

openssl genrsa -aes256 -out ./private/client-test-1.key.pem 2048

chmod 400 ./private/client-test-1.key.pem

openssl req -config ./openssl.cnf -key ./private/client-test-1.key.pem -new -sha256 -out ./csr/client-test-1.csr.pem

openssl ca -config ./openssl.cnf -extensions usr_cert -days 375 -notext -md sha256 -in ./csr/client-test-1.csr.pem -out ./certs/client-test-1.cert.pem

chmod 444 ./certs/client-test-1.cert.pem

openssl pkcs12 -export -inkey private/client-test-1.key.pem  -in certs/client-test-1.cert.pem -name client5 -out client5.pfx
```

### For more information ###
https://jamielinux.com/docs/openssl-certificate-authority/introduction.html