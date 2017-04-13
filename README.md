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